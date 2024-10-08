# Skedulo Plus Examples

A set of example Skedulo Plus Mobile Extensions, to be deployed with the [Skedulo CLI](#Usage). 

These are currenrly for early access customers only.

## Extensions

The following example extensions are available: Hello World, Job Products, Kitchen Sink. These extensions are detailed below

### Hello World

A simple example with the bare minimum, displays some example text.

This form doesn't require any customisation within Skedulo, and should be used as a base for creating new mobile extensions.

### Account Details 

A practical example, allows the user to view the attributes of an account related to a Job. This form can be easily extended to expose custom account fields as well as the `readonly` page flag can be removed to allow users to update the account fields displayed. 

### Add Products

A practical example, allows the user to view, edit and create Product records for use in the Job Products extension below. 

### Job Products

A practical example, allowing the user to view, edit and create Job Product records, and attach images.

Requires Product records to be created using the "Add Products" or "Single Submission" extension detailed above.

### Account Contacts

A practical example, allowing a user to view, edit and create Contacts related to an Account for a given job. 

### Conditional Rendering

A version of the "Add Products" Extension with conditional rendering and dependant picklists. 

Requires the following fields to be created:

| Field Name | Type | Values |
|------------|-----|---------|
| ProductType | Picklist | Audio, Video, Lighting, Hardware |
| ProductSubType | Picklist | Ring Light, Panel Light, Green Screen, Lectern, Digital Still Camera, Digital Video Camera, Speaker, Headphones, Microphone |
| CameraType | Picklist | Mirrorless, DSLR |
| CameraLensSystem | Text | |
| Wattage | Integer | |
| LightingPowerConnector | Picklist | IEC-C13, IEC-C7, USB-C, MicroUSB, Barrel |

### UI Component Showcase

An example containing all available components, intented only as a showcase.

### Read Only Extension

A simple extension to display a read-only list of Product records. 

### Single Submission Extension

A simple extension to create Product records, does not allow for editing or listing.

### Single Job Product Extension

A simple extension to create a single Job Product per job, allows the record to be edited.


## Usage

These extensions are intended to be deployed with the Skedulo CLI.

In order to deploy them, you will need to log in to a tentant, this can be done with the following command

`sked tenant login web` or `sked tenant login token` if you wish to use an access token.

You will be prompted for your tenant name, and be asked if you wish to generate a long lived token.

### Deployment (create)

Run the following command to deploy the `HelloWorld` example to your tenant for the first time. Replace with value in `-f` with the appropriate folder if you wish to deploy a different extension.

`sked artifacts mobile-extension create -f HelloWorld.MobileExtension.json`

### Retrival (get)

Run the following command to retireve the `HelloWorld` example from your tenant. Replace with value in `-o` with the folder you wish to store the extension in. Change the value of `--defId` to retrieve a different extension.

`sked artifacts mobile-extension get -o . --defId HelloWorld`

### Modifications (update)

Run the following command to update the `HelloWorld` mobile extension after you've made changes locally. Replace with value in `-f` and `--defId` with the appropriate folder and Definition ID if you wish to deploy a different extension.

`sked artifacts mobile-extension update --defId HelloWorld -f HelloWorld.MobileExtension.json`

### Deletion (delete)

Run the following command to delete the `HelloWorld`. Replace with value in `--defId` with the appropriate Definition Id if you wish to delete a different extension.

`sked artifacts mobile-extension delete --defId HelloWorld`

### Getting Help

Please see the [Mobile Extension documation](https://mex-beta.docs.skedulo.com/developer-guides/customize-and-extend-mobile/skedulo-plus-extensions/mex-intro/), and if you still expirence issues please contact your Customer Success Manager.

