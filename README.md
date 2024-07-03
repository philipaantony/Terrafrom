**Terraform Documentation**

**Project Overview**

This project is an application built using Node.js and TypeScript, deployed to AWS Lambda, and managed with Terraform.

**Prerequisites**

Detail the software and tools required before setting up the project. Include versions where applicable.

- **Node.js** (v14.x or later)
- **npm** (v6.x or later) or **yarn** (v1.x or later)
- **TypeScript** (v4.x or later)
- **Git** (latest version)
- AWS Account and appropriate IAM permissions
- **AWS CLI** (v2.x or later) or follow terraform installation below
- **Terraform** (v1.x or later) or follow terraform installation below

**Install Terraform**

1. Download Terraform  
   download link: [Install | Terraform | HashiCorp Developer](https://developer.hashicorp.com/terraform/install)

   Choose 

- Windows OS
  Under Binary download select 386(for 32 bit) and AMD64(for 64 bit)
- Mac OS

`            `Under Binary download select AMD64

1. Install Terraform(windows)

Steps

1. Unzip the download file
1. Create a folder named Terraform inside “***C:\Program Files***”
1. Copy the exe file inside unzipped file to “***C:\Program Files\Terraform***”
1. Edit System environment variable for terraform and attach the path in system variables
1. Open CMD and check “***terraform --version***”




**Install AWS** 

- **Download AWS CLI**: Visit [AWS CLI Installer](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) and download the Windows installer.
- **Run Installer**: Open the downloaded .msi file and follow the on-screen instructions to complete the installation.
- **Verify Installation**: Open Command Prompt and type “*aws **–**version*” to check the installed version.
- **Configure AWS CLI**: Type “*aws configure*” in Command Prompt.
- **Enter Credentials**: Provide your AWS Access Key ID, Secret Access Key, region (e.g., us-east-1), and output format (e.g., json).

**


**TypeScript Lambda with Terraform Integration**

1. **Create and Navigate to the Project Folder**

   mkdir my-lambda-terraform-project

   cd my-lambda-terraform-project

1. **Initialize npm and Install TypeScript**

   npm init -y

   npm install typescript --save-dev

1. **Initialize TypeScript Configuration**

   npx tsc –init

1. **Modify tsconfig.json**

   Edit the tsconfig.json file to specify the output and root directories.

   { 

   ` `"compilerOptions": 

   `   `{ 

   `      `"outDir": "./dist", 

   `      `"rootDir": "./src", 

   `      `"types": ["node", "aws-lambda"] 

   `    `} 

   }



1. **Install AWS Lambda Dependencies**

   npm install aws-lambda

   npm install --save-dev @types/aws-lambda @types/node

1. **Write Your Lambda Function**

`        	`Create the Source Directory

`          `create src folder follow the below folder structure 

src/

│   ├── controller/

│   │   └── todoController.ts 

│   │

│   ├── service/

│   │   └── todoService.ts    

│   │

│   ├── repository/

│   │   └── todoRepository.ts 

1. **Compile TypeScript to JavaScript**
   npx tsc


1. **Set Up Terraform**

   mkdir terraform

   cd terraform
