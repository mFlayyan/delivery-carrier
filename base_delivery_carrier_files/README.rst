.. image:: https://img.shields.io/badge/licence-AGPL--3-blue.svg
    :target: https://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3

===========================
base_delivery_carrier_files
===========================

This module was written to extend the functionality of picking to support generating one or more files according to carrier_file configuration for all pickings
and writes this file to a configurable location on your computer eg. /opt/data/carrier_files

Discription:
Base module for creation of carrier files (La Poste, TNT Express Shipper, ...).
Files are exported as text (csv, ...).
It contains :
- the base structure to handle the export of files on Delivery Orders
- an API to ease the generation of the files for the developers in sub-modules.

The delivery orders can be grouped in one files
or be exported each one in a separate file.
The files can be generated automatically
on the shipment of a Delivery Order or from a manual action.
They are exported to a defined path or
in a document directory of your choice if the "document" module is installed.

A generic carrier file is included in the module.
It can also be used as a basis to create your own sub-module.

Sub-modules already exist to generate file according to specs of :
 - La Poste (France) : delivery_carrier_file_laposte
 - TNT Express Shipper (France) : delivery_carrier_file_tnt
 - Make your own ! Look at the code of the modules above,
   it's trivial to create a sub-module for a carrier.
