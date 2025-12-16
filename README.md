# insomnia-template-api-calls
Repository to track changes &amp; version control for Insomnia UNTP API Calls using built-in Insomnia Git Integration tool.


## Getting Started

Follow the steps below to clone the repository in Insomnia:

1. Create a new project in Insomnia and name it appropriately.
2. Select **Git Sync** as the project type.
3. Set the repository to `pyx-industries/insomnia-template-api-calls` and the branch to `master`.
4. Clone the repository.

## Development Workflow

1. The `master` branch is currently used as the main branch for tracking changes.
2. Before making any updates, ensure the repository is up to date by pulling the latest changes.
3. Insomnia will automatically detect any modifications and display them in the bottom-left corner.
4. Once you are satisfied with your changes, commit and push them to the remote repository.

## Issuing credentials
1. Select the environment accordingly at the top left corner based on the render templates.
2. Then, depending on credential you want to issue, choose the corresponding folder (DPP/DFR/DCC/DTE).
3. Click on the 002 - Issue Credential HTTP request and replace the value of “credentialSubject” with the JSON Instance that you have prepared.
4. Issue the Insomnia calls:
  - 001 - Issue Revocation Token - This is so that we can activate / revoke the VC - More details in https://uncefact.github.io/project-vckit/docs/get-started/api-server-get-started/basic-operations#issuing-a-status-vc
  - 002 - Issue Credential - This is the API call that will issue the VC. The result won’t be human readable.
  - 003 - Verify Credential - This is the API call to verify that the VC has been issued.
  - 004 - Store Credential - This is to store the issued VC to the storage.
  - 004.1 - View Credential - You don’t need to run this API call, it will just show a blank page in the Insomnia preview. This is to get the link to view the VC. You can get it by clicking on the arrow next to the Send button and click on “Generate Client Code”. Then, another window will show up with the full URL to view the VC.
  - 005 - Register in Resolver. This is the API call to link your issued VC to a IDR. For the IDR path, it will be using the following value from your issued VC as identificationKey.
  - 006 - Validate Resolve Registry. This API call is to validate that the VC has been successfully registered with the IDR link and is resolvable.
