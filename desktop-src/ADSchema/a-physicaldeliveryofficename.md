---
title: Physical-delivery-Office-Name-Attribut
description: Enthält den Bürostandort am Ort des Benutzers.
ms.assetid: a6be61bf-9a9a-4b97-bdf8-894c173efadd
ms.tgt_platform: multiple
keywords:
- Physical-delivery-Office-Name-Attribut AD-Schema
- physicalDeliveryOfficeName-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Physical-Delivery-Office-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6633ff902ba50cfce12aca54cc092ca4760e665c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957332"
---
# <a name="physical-delivery-office-name-attribute"></a>Physical-delivery-Office-Name-Attribut

Enthält den Bürostandort am Ort des Benutzers.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| CN                | Physical-delivery-Office-Name                                                       |
| LDAP-Display-Name | physicalDeliveryOfficeName                                                          |
| Size              | \-                                                                                  |
| Berechtigung aktualisieren  | Domänen Administrator oder Konto Besitzer.                                              |
| Aktualisierungshäufigkeit  | Wenn der Benutzerdaten Satz erstellt wird und wenn sich der Bürostandort ändern muss. |
| Attribute-Id      | 2.5.4.19                                                                            |
| System-ID-GUID    | bf9679f7-0de6-11d0-a285-00aa003049e2                                                |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                         |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x3a19                                                                                                                                                                                                                                                                                                          |
| System-Only            | False                                                                                                                                                                                                                                                                                                           |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                            |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                             |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3a19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                    |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                    |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                               |
| MAPI-Id                | 0x3a19                                                                                                           |
| System-Only            | False                                                                                                            |
| Ist-einwertig       | Richtig                                                                                                             |
| Ist indiziert             | Richtig                                                                                                             |
| Im globalen Katalog      | False                                                                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 128                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3a19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                    |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                    |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3a19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                    |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                    |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3a19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                    |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                    |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3a19                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                    |
| Ist indiziert             | Richtig                                                                                                                                                                                                                                                                                                                                                                    |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





