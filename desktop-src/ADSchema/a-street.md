---
title: Street-Address-Attribut
description: Die Adresse der Straße.
ms.assetid: 09a94b72-14cb-4d4d-b885-4015f65db139
ms.tgt_platform: multiple
keywords:
- Street-Address AD-Attributschema
- AD-Schema für Straßenattribut
topic_type:
- apiref
api_name:
- Street-Address
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a44cf03e89ee4f969d12e435f1fd3f31f535e9050bd667f220b5c6852a1bd092
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645620"
---
# <a name="street-address-attribute"></a>Street-Address-Attribut

Die Adresse der Straße.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Street-Address                                                                   |
| Ldap-Anzeigename | street                                                                           |
| Size              | \-                                                                               |
| Aktualisieren von Berechtigungen  | Jeder kann dieses Objekt basierend auf der Sicherheit des erstellten Objekts aktualisieren. |
| Updatehäufigkeit  | \-                                                                               |
| Attribute-Id      | 2.5.4.9                                                                          |
| System-ID-GUID    | bf967a3a-0de6-11d0-a285-00aa003049e2                                             |
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
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                    |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                     |
| Ist einwertig       | True                                                                                                                                                                                                                                                                                                                                                      |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                     |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                              |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                         |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                |
| In verwendete Klassen        | [**Lokalität**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ist einwertig       | True                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| In verwendete Klassen        | [**Lokalität**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                         |
| MAPI-Id                | 0x813A                                                                                                                                                     |
| System-Only            | False                                                                                                                                                      |
| Ist einwertig       | True                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                      |
| Im globalen Katalog      | True                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                          |
| Range-Upper            | 1024                                                                                                                                                       |
| Search-Flags           | 0x00000010                                                                                                                                                 |
| System-Flags           | 0x00000012                                                                                                                                                 |
| In verwendete Klassen        | [**Lokalität**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ist einwertig       | True                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| In verwendete Klassen        | [**Lokalität**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ist einwertig       | True                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| In verwendete Klassen        | [**Lokalität**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Ist einwertig       | True                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| In verwendete Klassen        | [**Lokalität**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                |
| MAPI-Id                | 0x813A                                                                                                                                                                                                                                                                                                                                                                                                            |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Is-Single-Valued       | True                                                                                                                                                                                                                                                                                                                                                                                                              |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                             |
| Im globalen Katalog      | True                                                                                                                                                                                                                                                                                                                                                                                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                      |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                        |
| System-Flags           | 0x00000012                                                                                                                                                                                                                                                                                                                                                                                                        |
| In verwendete Klassen        | [**Lokalität**](c-locality.md)<br/> [**Organisation**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Besennungsperson**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





