---
title: Post-Office-Box-Attribut
description: Die Postfachnummer für dieses Objekt.
ms.assetid: e782271a-2f79-42af-9c62-5723917a6f47
ms.tgt_platform: multiple
keywords:
- AD-Schema für Post-Office-Box-Attribut
- postOfficeBox-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Post-Office-Box
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f86bd2f1ae357485c00af2da52cf26fa4b5d8f67d1020fe9fa3e204a48a9e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065976"
---
# <a name="post-office-box-attribute"></a>Post-Office-Box-Attribut

Die Postfachnummer für dieses Objekt.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------------------|
| CN                | Post-Office-Box                                                             |
| Ldap-Anzeigename | postOfficeBox                                                               |
| Size              | \-                                                                          |
| Aktualisieren von Berechtigungen  | Domänenadministrator oder Kontobesitzer.                                      |
| Updatehäufigkeit  | Wenn der Datensatz des Benutzers erstellt wird und wann immer die Adresse geändert werden muss. |
| Attribute-Id      | 2.5.4.18                                                                    |
| System-ID-GUID    | bf9679fb-0de6-11d0-a285-00aa003049e2                                        |
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
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                          |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                           |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                           |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                           |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                    |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                               |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                      |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                               |
| MAPI-Id                | 0x3A2B                                                                                                           |
| System-Only            | Falsch                                                                                                            |
| Ist einwertig       | Falsch                                                                                                            |
| Ist indiziert             | Falsch                                                                                                            |
| Im globalen Katalog      | Falsch                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 40                                                                                                               |
| Search-Flags           | 0x00000010                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | 0x3A2B                                                                                                                                                                                                                                                                                                                                                                  |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist einwertig       | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                                                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 40                                                                                                                                                                                                                                                                                                                                                                      |
| Search-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                              |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Unternehmensperson**](c-organizationalperson.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**1600-000-**](c-residentialperson.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> |



 

 





