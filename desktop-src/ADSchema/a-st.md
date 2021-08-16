---
title: State-Or-Province-Name-Attribut
description: Der Name des Bundesstaats oder der Provinz eines Benutzers.
ms.assetid: 2096318e-29bf-4021-a422-371835f3a62b
ms.tgt_platform: multiple
keywords:
- Ad-Schema des State-Or-Province-Name-Attributs
- st-Attribut AD-Schema
topic_type:
- apiref
api_name:
- State-Or-Province-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c818eb0a885d598edc10b5857aee23e336095c301d3b1059b25ba7b2f9fd986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959989"
---
# <a name="state-or-province-name-attribute"></a>State-Or-Province-Name-Attribut

Der Name des Bundesstaats oder der Provinz eines Benutzers.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------|
| CN                | State-Or-Province-Name                                                           |
| Ldap-Anzeigename | st                                                                               |
| Size              | \-                                                                               |
| Aktualisieren von Berechtigungen  | Jeder kann dieses Objekt basierend auf der Sicherheit des zu erstellenden Objekts aktualisieren. |
| Updatehäufigkeit  | \-                                                                               |
| Attribute-Id      | 2.5.4.8                                                                          |
| System-Id-Guid    | bf967a39-0de6-11d0-a285-00aa003049e2                                             |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                      |



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
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Is-Single-Valued       | True                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Is-Single-Valued       | True                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                         |
| MAPI-Id                | 0x3A28                                                                                                                                                     |
| System-Only            | False                                                                                                                                                      |
| Ist einwertig       | True                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                      |
| Im globalen Katalog      | True                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                          |
| Range-Upper            | 128                                                                                                                                                        |
| Search-Flags           | 0x00000010                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                 |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist einwertig       | True                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist einwertig       | True                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist einwertig       | True                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                        |
| MAPI-Id                | 0x3A28                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist einwertig       | True                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 128                                                                                                                                                                                                                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Ort**](c-locality.md)<br/> [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



 

 





