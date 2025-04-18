## 📄 KJHK – Zetta Live Metadata Export

> This repository contains the RDS exports for Zetta used by KJHK 90.7 FM.

The Invonics Model 732 RDS Encoder recieves the metadata sent from Zetta via TCP.

### Tools used

-   [Zetta RCS](https://www.rcsworks.com/zetta/)
-   [Inovonics Model 732 RDS Encoder](https://www.inovonicsbroadcast.com/product/732)

### Usage

#### Creating a new Live Metadata source in Zetta

1. Login to Zetta using a Supervisor account.
2. Go to the `Configuration` > `System` > `Live Metadata` tab.
3. Create a new `Live Metadata` source (using the `+` button).

#### Using the RDS Encoder Template

4. Scroll to the `Advanced` section and create a new format using the `+` button.
5. In the `XSLT to apply` field, paste the contents of `RDSEncoderTemplate.xml`, then click the save button.

#### Sending the metadata to the RDS Encoder

6. Scroll down to the `Delivery Method` and ensure the following settings are selected:

    - Device: `TCP`
    - IP Address: `YOUR_IP_ADDRESS`
    - Port: `YOUR_PORT`
    - Connection Style: `Keep connection open`

7. Save the Live Metadata source and ensure the `Active` checkbox is checked.

### Future Improvements

Currently, the RDS Encoder template filters out non `SONG` metadata. In the future, we may want to add support for other metadata types such as `SPOT` and `BREAK`.

### License

Distributed under the GPL 3.0 License. See `LICENSE` for more information.
