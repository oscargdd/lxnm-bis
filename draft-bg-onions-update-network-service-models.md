---
###
# Internet-Draft Markdown Template
#
# Rename this file from draft-todo-yourname-protocol.md to get started.
# Draft name format is "draft-<yourname>-<workgroup>-<name>.md".
#
# For initial setup, you only need to edit the first block of fields.
# Only "title" needs to be changed; delete "abbrev" if your title is short.
# Any other content can be edited, but be careful not to introduce errors.
# Some fields will be set automatically during setup if they are unchanged.
#
# Don't include "-00" or "-latest" in the filename.
# Labels in the form draft-<yourname>-<workgroup>-<name>-latest are used by
# the tools to refer to the current version; see "docname" for example.
#
# This template uses kramdown-rfc: https://github.com/cabo/kramdown-rfc
# You can replace the entire file if you prefer a different format.
# Change the file extension to match the format (.xml for XML, etc...)
#
###
title: "TODO - Your title"
abbrev: "Update of Network Service Yang models"
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
  group: WG
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
    email: oscar.gonzalezdedios@telefonica.com

normative:

informative:

...

--- abstract

TODO Abstract


--- middle

# Introduction

TODO Introduction


# Conventions and Definitions

{::boilerplate bcp14-tagged}

# Observations and new requirements

## Missing Features
Implementations of LxNM models in controllers required new functionalities which were not covered in the RFCxxx yang models to deploy all the functionality required in the Operator services. This section compiles the functions that were reported by those implementations. 
* BFD parametrization of static routes:
  * The L3NM Yang data model allows to manage static routes in a VPN. The new requirement is the ability to specify BFD intented configuration in the IPv4 and IPv6 static routes.



# Security Considerations

TODO Security


# IANA Considerations

This document has no IANA actions.


--- back

# Acknowledgments
{:numbered="false"}

TODO acknowledge.
