---
title: User-Parameters-Attribut
description: Parameter des Benutzers.
ms.assetid: e3d6d22d-5112-4dfe-af55-a17a63e5f2e4
ms.tgt_platform: multiple
keywords:
- User-Parameters AD-Schema
- userParameters-Attribut AD-Schema
topic_type:
- apiref
api_name:
- User-Parameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f26907015ee1c17bc4e809b3b5c2a52adf79ffb20d497e34ff094b620936436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922930"
---
# <a name="user-parameters-attribute"></a>User-Parameters-Attribut

Parameter des Benutzers. Zeigt auf eine Unicode-Zeichenfolge, die für die Verwendung durch Anwendungen vorgesehen ist. Diese Zeichenfolge kann eine NULL-Zeichenfolge sein oder eine beliebige Anzahl von Zeichen vor dem beendenden NULL-Zeichen enthalten. Microsoft-Produkte verwenden dieses Mitglied zum Speichern von Benutzerdaten, die für das einzelne Programm spezifisch sind.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | User-Parameters                             |
| Ldap-Anzeigename | userParameters                              |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | Geändert von Anwendungen.                   |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.138                      |
| System-Id-Guid    | bf967a6d-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------|
| Link-ID                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | False                             |
| Is-Single-Valued       | True                              |
| Ist indiziert             | False                             |
| Im globalen Katalog      | False                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

 





