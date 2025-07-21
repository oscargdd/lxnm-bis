---
title: "An Update of Network Service Yang models"
abbrev: "Network Service models update"
"
category: info

docname: draft-bg-onions-update-network-service-models-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
area: AREA
workgroup: WG Working Group
keyword:
 - next generation
 - unicorn
 - sparkling distributed ledger
venue:
  group: ONIONS
  type: Working Group
  mail: WG@example.com
  arch: https://example.com/WG
  github: USER/REPO
  latest: https://example.com/LATEST

author:
 -
    fullname: Oscar Gonzalez de Dios
    organization: Your Organization Here
    email: oscar.gonzalezdedios@telefonica.com
-
    fullname: Samier Barguil
    organization: Nokia
    email: samier.barguil_giraldo@nokia.com

normative:


informative:

...

--- abstract

The L2NM and L3NM Network Yang models have been implemented in recent years to facilate the deployment of Operator services. This document reports the findings from the implementations, deriving the functionalities required to update the Network Service Yang models. 


--- middle

# Introduction

The L2NM and L3NM Network Yang models have been implemented in recent years to facilate the deployment of Operator services. This document reports the findings from the implementations, deriving the functionalities required to update the Network Service Yang models. 


# Conventions and Definitions

{::boilerplate bcp14-tagged}

# Observations and new requirements

## Missing Features
Implementations of LxNM models in controllers required new functionalities which were not covered in the RFCxxx yang models to deploy all the functionality required in the Operator services. This section compiles the functions that were reported by those implementations. 
* BFD parametrization of static routes:
  * The L3NM Yang data model allows to manage static routes in a VPN. That is, for a particular VPN service, new Pv4 and IPv6 static routes can be added, modified or deleted. The data model allows to specify wether BFD is desired in the static route. Whenever a controller derives the device configuration of the static route it will need to decide a particular BFD configuration, typically from a pre-defined template. Operators required, for different services, to customize the main BFD parameters to allow, for example, faster detection for critical services. The new requirement is the ability to specify BFD intented configuration in the IPv4 and IPv6 static routes, including a required-min-rx-interval and multiplier.
## Status of the intented Network Service. 
The Network Service Yang models represents an intent of the realization of VPN service. A controller, after an instance of the network service yang intent has been created, will derive the necessary device level configurations and apply them to the necessary devices. However, the implementations reported a set of open issues. Those issues been solved by propietary means as they were not covered by the standard mechanism and left to implementations.  

* Issue #5: Is the Service running on the Network? 
  * How can the northbound system be assured with 100% certainty that a configuration has been successfully installed on the network device?
  * What mechanisms or feedback loops exist to confirm successful configuration deployment beyond simple acknowledgment?
  * How does the system can handle transient errors or partial configuration applications from the model perspective?
  * Are there specific operational attributes that can be used to reflect the real-time status of the configuration?
  * Does the network element provide any operational state parameters or notifications that indicate whether the configuration is active, pending, or has failed?
  * If a configuration is manually removed via CLI at the network device, is there a mechanism to reflect this change northbound?



# Security Considerations

TODO Security


# IANA Considerations

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
