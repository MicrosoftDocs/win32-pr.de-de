---
title: Telephone-Number-Attribut
description: Die primäre Telefonnummer.
ms.assetid: 6a7faad4-9d86-4821-9b00-67adbf1b05f2
ms.tgt_platform: multiple
keywords:
- AD-Schema für Telephone-Number-Attribut
- "\"telefonienumber\"-Attribut AD-Schema"
topic_type:
- apiref
api_name:
- Telephone-Number
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba099342222fcae24871730f16624fcf6336221d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107499"
---
# <a name="telephone-number-attribute"></a>Telephone-Number-Attribut

Die primäre Telefonnummer.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------|
| CN                | Telephone-Number                                                                 |
| LDAP-Display-Name | telephoneNumber                                                                  |
| Size              | \-                                                                               |
| Berechtigung aktualisieren  | Jeder kann dieses Objekt basierend auf der Sicherheit des Objekts, das erstellt wird, aktualisieren. |
| Aktualisierungshäufigkeit  | \-                                                                               |
| Attribute-Id      | 2.5.4.20                                                                         |
| System-ID-GUID    | bf967a49-0de6-11d0-a285-00aa003049e2                                             |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                      |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3a08                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3a08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**documentseries**](c-documentseries.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Versand**](c-room.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                               |
| MAPI-Id                | 0x3a08                                                                                                           |
| System-Only            | False                                                                                                            |
| Ist-einwertig       | Richtig                                                                                                             |
| Ist indiziert             | False                                                                                                            |
| Im globalen Katalog      | Richtig                                                                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                     |
| Range-Lower            | 1                                                                                                                |
| Range-Upper            | 64                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                       |
| System-Flags           | 0x00000010                                                                                                       |
| In verwendete Klassen        | [**Organisation**](c-organization.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3a08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**documentseries**](c-documentseries.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Versand**](c-room.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3a08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**documentseries**](c-documentseries.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Versand**](c-room.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3a08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**documentseries**](c-documentseries.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Versand**](c-room.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                                                                                                                                                                         |
| MAPI-Id                | 0x3a08                                                                                                                                                                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Ist indiziert             | False                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Im globalen Katalog      | Richtig                                                                                                                                                                                                                                                                                                                                                                                                                       |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                                                                                                                                                               |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Range-Upper            | 64                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                 |
| In verwendete Klassen        | [**documentseries**](c-documentseries.md)<br/> [**E-Mail-Empfänger**](c-mailrecipient.md)<br/> [**Organisation**](c-organization.md)<br/> [**Organisations Rolle**](c-organizationalrole.md)<br/> [**Organisationseinheit**](c-organizationalunit.md)<br/> [**Person**](c-person.md)<br/> [**rFC822LocalPart**](c-rfc822localpart.md)<br/> [**Versand**](c-room.md)<br/> |



 

 





