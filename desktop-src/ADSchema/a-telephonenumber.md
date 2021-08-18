---
title: Telephone-Number-Attribut
description: Die primäre Telefonnummer.
ms.assetid: 6a7faad4-9d86-4821-9b00-67adbf1b05f2
ms.tgt_platform: multiple
keywords:
- Telephone-Number AD-Schema
- telephoneNumber-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Telephone-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d86054b50ae511b3f519c1c289fb529eaa8a2e7279adb7b66cbfc2df32c3758
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923120"
---
# <a name="telephone-number-attribute"></a>Telephone-Number-Attribut

Die primäre Telefonnummer.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Telephone-Number                                                                 |
| Ldap-Anzeigename | telephoneNumber                                                                  |
| Size              | \-                                                                               |
| Aktualisieren von Berechtigungen  | Jeder kann dieses Objekt basierend auf der Sicherheit des zu erstellenden Objekts aktualisieren. |
| Updatehäufigkeit  | \-                                                                               |
| Attribute-Id      | 2.5.4.20                                                                         |
| System-Id-Guid    | bf967a49-0de6-11d0-a285-00aa003049e2                                             |
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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                     |
| System-Only            | Falsch                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**documentSeries**](c-documentseries.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Zimmer**](c-room.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                               |
| MAPI-Id                | 0x3A08                                                                                                           |
| System-Only            | Falsch                                                                                                            |
| Is-Single-Valued       | Richtig                                                                                                             |
| Ist indiziert             | Falsch                                                                                                            |
| Im globalen Katalog      | Richtig                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 64                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| In verwendete Klassen        | [**Organization**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**documentSeries**](c-documentseries.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Zimmer**](c-room.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**documentSeries**](c-documentseries.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Zimmer**](c-room.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**documentSeries**](c-documentseries.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Zimmer**](c-room.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3A08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**documentSeries**](c-documentseries.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organization**](c-organization.md)<br/> [**Organisationsrolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Zimmer**](c-room.md)<br/> |



 

 





