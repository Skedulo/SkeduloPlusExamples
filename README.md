# Skedulo Plus Examples

A set of example Skedulo Plus Mobile Extensions, to be deployed with the [Skedulo CLI](#Usage).

## Extensions

The following example extensions are available: Hello World, Job Products, Kitchen Sink. These extensions are detailed below

### Hello World

A simple example with the bare minimum, displays some example text.

This form doesn't require any customisation within Skedulo, and should be used as a base for creating new mobile extensions.

#### Example

<img src="/images/hello-world.jpg" width="200">

### Add Products

A practical example, allows the user to add Product records for use in the Job Products extension below. 

#### Example

<img src="/images/hello-world.jpg" width="200">


### Job Products

A practical example, allowing the user to create and update Job Product records, and attach images.

Requires Product records to be created using the "Add Products" extension detailed above.

#### Example

<img src="/images/hello-world.jpg" width="200">

### Kitchen Sink

An example containing all available components, intented only as a showcase.

#### Example

TBC

## Usage

These extensions are intended to be deployed with the Skedulo CLI.

In order to deploy them, you will need to log in to a tentant, this can be done with the following command

`sked tenant login web` or `sked tenant login token` if you wish to use an access token.

You will be prompted for your tenant name, and be asked if you wish to generate a long lived token.

### Deployment

Run the following command to deploy the `HelloWorld` example to your tenant for the first time. Replace with value in `-f` with the appropriate folder if you wish to deploy a different extension.

`sked artifacts mobile-extension create -f ./HelloWorld`

### Retrival

Run the following command to retireve the `HelloWorld` example from your tenant. Replace with value in `-o` with the folder you wish to store the extension in. Change the value of `--defId` to retrieve a different extension.

`sked artifacts mobile-extension get -o ./HelloWorld --defId HelloWorld`

### Modifications

Run the following command to update the `HelloWorld` mobile extension after you've made changes locally. Replace with value in `-f` and `--defId` with the appropriate folder and Definition ID if you wish to deploy a different extension.

`sked artifacts mobile-extension update --defId HelloWorld -f ./HelloWorld`

### Deletion

Run the following command to delete the `HelloWorld`. Replace with value in `--defId` with the appropriate Definition Id if you wish to delete a different extension.

`sked artifacts mobile-extension delete --defId HelloWorld`

