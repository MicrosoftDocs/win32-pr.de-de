---
title: Postal-Address-Attribut
description: Die Adressenadresse für das -Objekt.
ms.assetid: 85e96b88-8e58-4916-a333-59e3d4ed8025
ms.tgt_platform: multiple
keywords:
- Postal-Address AD-Schema
- postalAddress-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Postal-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfc8aa9b3dbdd1a91ed8a55f55a295c10353f88e6e7e01a852481ddb68163b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118682393"
---
# <a name="postal-address-attribute"></a>Postal-Address-Attribut

Die Adressenadresse für das -Objekt.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Postal-Address                                                              |
| Ldap-Anzeigename | postalAddress                                                               |
| Size              | \-                                                                          |
| Aktualisieren von Berechtigungen  | Domänenadministrator oder Kontobesitzer.                                      |
| Updatehäufigkeit  | Wenn der Datensatz des Benutzers erstellt wird und wann immer die Adresse geändert werden muss. |
| Attribute-Id      | 2.5.4.16                                                                    |
| System-Id-Guid    | bf9679fc-0de6-11d0-a285-00aa003049e2                                        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                 |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                              |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                          |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                           |
| Is-Single-Valued       | Falsch                                                                                                                                                                                                                                                                                                           |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                           |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                            |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                               |
| MAPI-Id                | 0x810C                                                                                                           |
| System-Only            | Falsch                                                                                                            |
| Is-Single-Valued       | Falsch                                                                                                            |
| Ist indiziert             | Falsch                                                                                                            |
| Im globalen Katalog      | Falsch                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 4096                                                                                                             |
| Search-Flags           | 0x00000010                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x810C                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 4096                                                                                                                                                                                                                                                                                                                                                                    |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





