---
title: Bevorzugtes Zustellungs Methoden Attribut
description: Die X. 500-bevorzugte Methode für die Bereitstellung an den Adressaten.
ms.assetid: 53e704bf-0562-48c0-89d7-5871c388027c
ms.tgt_platform: multiple
keywords:
- Bevorzugtes Zustellungs Methoden Attribut AD-Schema
- Attribut "PreferredDeliveryMethod" AD Schema
topic_type:
- apiref
api_name:
- Preferred-Delivery-Method
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e9233b4c5332c47e8ae28a146e2c1e1c90de79c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106343898"
---
# <a name="preferred-delivery-method-attribute"></a>Bevorzugtes Zustellungs Methoden Attribut

Die X. 500-bevorzugte Methode für die Bereitstellung an den Adressaten.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Bevorzugte Übermittlungs Methode            |
| LDAP-Display-Name | PreferredDeliveryMethod              |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 2.5.4.28                             |
| System-ID-GUID    | bf9679fe-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



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
| MAPI-Id                | 0x810d                                                                                                                                                                                                                                                                                                          |
| System-Only            | False                                                                                                                                                                                                                                                                                                           |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                           |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | \-                                                                                                                                                                                                                                                                                                              |
| Range-Upper            | \-                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810d                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | \-                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Upper            | \-                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                               |
| MAPI-Id                | 0x810d                                                                                                           |
| System-Only            | False                                                                                                            |
| Ist-einwertig       | False                                                                                                            |
| Ist indiziert             | False                                                                                                            |
| Im globalen Katalog      | False                                                                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                     |
| Range-Lower            | \-                                                                                                               |
| Range-Upper            | \-                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810d                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | \-                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Upper            | \-                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810d                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | \-                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Upper            | \-                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810d                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | \-                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Upper            | \-                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810d                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | \-                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Upper            | \-                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





