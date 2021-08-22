---
title: X121-Address-Attribut
description: Die X.121-Adresse für ein Objekt.
ms.assetid: 3fe3cb04-6a76-4b5b-af4e-c73afd7e0412
ms.tgt_platform: multiple
keywords:
- X121-Address AD-Attributschema
- x121Address-Attribut AD-Schema
topic_type:
- apiref
api_name:
- X121-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c16831af773869649ed663ebef34e70d9a9e8f4ed329fa14bc41938a253f16d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959939"
---
# <a name="x121-address-attribute"></a>X121-Address-Attribut

Die X.121-Adresse für ein Objekt.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | X121-Address                                |
| Ldap-Anzeigename | x121Address                                 |
| Size              | 15 Bytes                                    |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 2.5.4.24                                    |
| System-ID-GUID    | bf967a7b-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Numeric)**](s-string-numeric.md) |



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
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                          |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                           |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                           |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                           |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                               |
| MAPI-Id                | 0x8158                                                                                                           |
| System-Only            | Falsch                                                                                                            |
| Ist einwertig       | Falsch                                                                                                            |
| Ist indiziert             | Falsch                                                                                                            |
| Im globalen Katalog      | Falsch                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 15                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Is-Single-Valued       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x8158                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 15                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





