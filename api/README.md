# HYF Api

We use `express` together with `aws-serverless-express` proxy.

## Supported functionalities
- **Student Apply**

  Send an Email to the ***Organization*** with the details of the ***Student to be***.
  And to the ***Student to be*** an email with the details of the next step.

- **Mentor Apply**

  Send an email to the ***Organization***.
  
- **Contact us**

  Send an email to the ***Organization***.
  
- **Donate**
  
## Structure

- **Emails Templates**
  They can be parse with `lodash.template` or can be just plain text.
  They can be found under `./email_templates`

- **Routes**
  You can add them under `./src/app`. Follow the `express-ion` :-)

## Development
If you want to start development you can run `npm dev`.
This would:
- Start a fake `ses` provider
- Start nodemon from the `dev.js`
- `webpack --watch`

## Publish 
```make publish-api```

## Cloud Services and deploys
We currently use `terraform.io` to access to `aws` resorces, we wanna mantain
our cloud environment under control and we choose to host the 
[infrastructure](https://github.com/HackYourFuture/infrastucture) in code.

### Currently aws used resources.
- Simple Email Service
- Lambda
- API Gateway
- Cloud Watch log
