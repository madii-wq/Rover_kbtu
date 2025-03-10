<h1>Motor drive system</h1>

<h2>Requirements</h2>
<h3>Functional requirements</h3>
<ol>
    <li>Drive motor using API endpoints</li>
    <li>API endpoints must regulate speed, direction, angular of motor</li>
    <li>Communicate with motor controller (optional)</li>
</ol>
<h3>Non-functional requirements</h3>
<ol>
    <li>Motor controller commercial ready solution</li>
    <li>Servos controller commercial ready solution</li>
    <li>Motor controller costs < 100$</li>
    <li>Motor controller support PWM, data communication (optional)</li>
    <li>Servos also support PWM and data communication (optional)</li>
    <li><a href="https://www.amazon.com/Cytron-30A-Motor-Driver-MD30C/dp/B07L6HGFWY">Link to product</a></li>
</ol>

<h2>Architecture design</h2>
<p>Architecture design is relationship between functional components affected by non-functional requirenements that describe how our system is organized. First step is identidy functional components that we used</p>
<h3>Architecture diagramm</h3>

```mermaid
    flowchart TD
        Sensors[Sensors]
        Sensors --Data-->Master
        Master[Master controller]
        Servos1[Servo 1]
        Servos2[Servo 2]
        Servos3[Servo 3]
        Servos4[Servo 4]
        Servos5[Servo 5]
        Servos6[Servo 6]
        MotorController1[Motor controller 1]
        MotorController2[Motor controller 2]
        MotorController3[Motor controller 3]
        MotorController4[Motor controller 4]
        MotorController5[Motor controller 5]
        MotorController6[Motor controller 6]
        Master --PWM-->Servos1-->MotorController1-->Motor1[Motor 1]
        Master --PWM-->Servos2-->MotorController2-->Motor2[Motor 2]
        Master --PWM-->Servos3-->MotorController3-->Motor3[Motor 3]
        Master--PWM-->Servos4-->MotorController4-->Motor4[Motor 4]
        Master --PWM-->Servos5-->MotorController5-->Motor5[Motor 5]
        Master --PWM-->Servos6-->MotorController6-->Motor6[Motor 6]
```

<h3>API design</h3>
<p>API defines how computer systems interact with each other. In our case computer systems are Master controller and Motor controller</p>

