---
title: Script-Path-Attribut
description: Dieses Attribut gibt den Pfad für das Anmeldeskript des Benutzers an. Die Zeichenfolge kann NULL sein.
ms.assetid: 356f2ba0-ceca-4805-a536-286c6a8b54fc
ms.tgt_platform: multiple
keywords:
- Script-Path AD-Schema
- scriptPath-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Script-Path
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbb015b627da90bab453f45dda0a46449f3362b3313e288e2a0f56bb59d0e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923210"
---
# <a name="script-path-attribute"></a>Script-Path-Attribut

Dieses Attribut gibt den Pfad für das Anmeldeskript des Benutzers an. Die Zeichenfolge kann NULL sein.



| Eingabe | Wert |
|-------------------|------------------------------------------------------------------------|
| CN                | Script-Path                                                            |
| Ldap-Anzeigename | scriptPath                                                             |
| Size              | \-                                                                     |
| Aktualisieren von Berechtigungen  | Domänenadministrator oder Kontobesitzer.                                 |
| Updatehäufigkeit  | Wenn der Benutzerdatensatz erstellt wird und wann immer der Pfad geändert werden muss. |
| Attribute-Id      | 1.2.840.113556.1.4.62                                                  |
| System-Id-Guid    | bf9679a8-0de6-11d0-a285-00aa003049e2                                   |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                            |



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
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
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
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
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
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
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
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
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
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
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
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| In verwendete Klassen        | [**Benutzer**](c-user.md)<br/> |



 

 





