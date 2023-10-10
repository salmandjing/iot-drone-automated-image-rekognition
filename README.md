# Right of Way Inspection Using Computer Vision on AWS

[](https://github.com/salmandjing/iot-drone-automated-image-rekognition/blob/master/architecture.PNG)

## Right of Way Inspection 

Right of way (ROW) is the legal right to pass along a specific route through property belonging to another. A similar right of access also exists on land held by a government, lands that are typically called public land, state land, or Crown land. Utility companies routinely utilize this to build infrastructure such as
transmission lines and pipelines. Prior to building this infrastructure, an inspection needs to be completed. These inspections help make ROW projects safer and more accessible by asses spots that need to be cleared, providing visibility into hard to reach places, and enabling detailed planning. Traditionally these 
inspection are done with helicopter but the industry is shifting towards drones. 

## Innovating using Computer Vision on AWS

Manual inspection are:
 - Time intensive as they required trained proffesionals to comb hundreds or thousands of picture or hours of video footage
 - Prone to human error and depedent on the quality of the inspector
 - Inneficient for larger inspections

This process can be improved using:
- AWS Iot Greengrass to automatically ingest photos into AWS
- AWS KMS to encrypt the data and AWS IAM to secure access to your data
- AWS IoT Core to process these images
- Amazon Rekognition to analyze the images or video for different objects. Custom models can be trained to identify specific objects
- Amazon S3 for durable long term storage
- AWS Lambda for automated email notifications to responsible parties. Amazon SNS can also be used as a replacement here
- Amazon CloudTrail and Cloudwatch to provide granular visiblity, logs, metrics


  ## Instructions
- Train an Amazon Custom Labels Model. If you want step check [this video](https://www.youtube.com/watch?v=QwHbReDwdxQ&t=722s) Step by Step instruction can be found at 12:00 - 19:00
- Install Greengrass on compute module (ex: Raspberry Pi) and connect it to an S3 bucket and replace the name in the CFN tempate
- Deploy the template

  ## Clean up
- Delete CFN Stack
 
    
