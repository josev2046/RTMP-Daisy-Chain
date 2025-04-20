# RTMP Daisy Chaining

### User Story: 
As a content provider, I want to be able to multicast a single stream to multiple users with different authentication methods (SSO, password, and public) 

The process could be implemented as follows:

![image](https://github.com/user-attachments/assets/dc377505-3a3a-4656-958b-2345560812bd)

Figure 1. An RTMP daisy chaining sequence diagram.


### Encoder Initiation

The encoder generates an RTMP stream from the content source (e.g., live video). This initial stream is directed to the first player in the chain.

### Player 1 (SSO Authentication)

* Player 1 receives the initial RTMP stream.
* This player employs Single Sign-On (SSO) for user verification. Access typically requires authentication via a central identity provider.
* The diagram above illustrates an alternative flow for SSO authentication, wherein Player 1 performs user authentication, likely involving redirection to the SSO provider for credential validation and authorisation confirmation.

### Player 2 (Password Authentication)

* Player 2 receives the multicast stream.
* This player utilises password-based authentication, requiring users to input credentials for access.
* Similar to Player 1, the diagram shows an alternative flow for password authentication, where Player 2 authenticates users by verifying their credentials against its designated system.

### Player 3 (Public Access)

* Player 3 receives the multicast stream.
* Designated as "Public," this player typically does not require authentication. Access to the stream is generally open.

