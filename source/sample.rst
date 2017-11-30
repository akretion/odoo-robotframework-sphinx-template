Partner
=======

Partner Creation
----------------

.. code:: robotframework
    :class: hidden

    *** Settings ***

    Resource       resource.robot
    Suite Setup    set library search order   extendedselenium2library   selenium2library

    *** Test Cases ***

    Valid Login
      Login

    Creating a new quotation
      MainMenuText    Sales
      SubMenuText    Sales Orders
      Button	model=sale.order	button_name=oe_list_add
      Many2OneSelect    sale.order	partner_id	Agrolait
      Close Browser

.. figure:: _screenshots/partner.png

.. code:: robotframework
    :class: hidden

      Capture viewport screenshot  _screenshots/partner.png


