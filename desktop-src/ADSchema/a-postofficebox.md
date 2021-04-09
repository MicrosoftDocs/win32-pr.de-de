---
title: Post-Office-Box-Attribut
description: Die Post-Box-Nummer für dieses Objekt.
ms.assetid: e782271a-2f79-42af-9c62-5723917a6f47
ms.tgt_platform: multiple
keywords:
- Post-Office-Feld Attribut AD-Schema
- PostOfficeBox-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Post-Office-Box
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8dc8edd327a8b7577e7a8256a8e2f082aad13c8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957596"
---
# <a name="post-office-box-attribute"></a>Post-Office-Box-Attribut

Die Post-Box-Nummer für dieses Objekt.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Post-Office-Box                                                             |
| LDAP-Display-Name | postOfficeBox                                                               |
| Size              | \-                                                                          |
| Berechtigung aktualisieren  | Domänen Administrator oder Konto Besitzer.                                      |
| Aktualisierungshäufigkeit  | Wenn der Benutzerdaten Satz erstellt und die Adresse geändert werden muss. |
| Attribute-Id      | 2.5.4.18                                                                    |
| System-ID-GUID    | bf9679fb-0de6-11d0-a285-00aa003049e2                                        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                 |



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
| MAPI-Id                | 0x3a2b                                                                                                                                                                                                                                                                                                          |
| System-Only            | False                                                                                                                                                                                                                                                                                                           |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                           |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                           |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3a2b                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                               |
| MAPI-Id                | 0x3a2b                                                                                                           |
| System-Only            | False                                                                                                            |
| Ist-einwertig       | False                                                                                                            |
| Ist indiziert             | False                                                                                                            |
| Im globalen Katalog      | False                                                                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 40                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3a2b                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3a2b                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3a2b                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3a2b                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist-einwertig       | False                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Privat Person**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





