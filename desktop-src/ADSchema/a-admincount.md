---
title: Admin-Count-Attribut
description: Gibt an, dass die ACLs eines bestimmten Objekts vom System in einen sichereren Wert geändert wurden, da es Mitglied einer der administrativen Gruppen war (direkt oder transitiv).
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- Admin-Count AD-Attributschema
- AD-Schema für adminCount-Attribut
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d652d53627643e1028ee73cc67678119c689e46d8f4ec289c92ca32127e098dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022848"
---
# <a name="admin-count-attribute"></a>Admin-Count-Attribut

Gibt an, dass die ACLs eines bestimmten Objekts vom System in einen sichereren Wert geändert wurden, da es Mitglied einer der administrativen Gruppen war (direkt oder transitiv).



| Eingabe | Wert |
|-------------------|-----------------------------------------------------|
| CN                | Admin-Count                                         |
| Ldap-Anzeigename | adminCount                                          |
| Size              | 4 Bytes                                             |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.                    |
| Updatehäufigkeit  | Wenn ein Objekt einer administrativen Gruppe hinzugefügt wird. |
| Attribute-Id      | 1.2.840.113556.1.4.150                              |
| System-ID-GUID    | bf967918-0de6-11d0-a285-00aa003049e2                |
| Syntax            | [**Enumeration**](s-enumeration.md)                |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------|
| Link-ID                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falsch                                                                 |
| Ist einwertig       | Richtig                                                                  |
| Ist indiziert             | Falsch                                                                 |
| Im globalen Katalog      | Falsch                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------|
| Link-ID                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falsch                                                                 |
| Ist einwertig       | Richtig                                                                  |
| Ist indiziert             | Falsch                                                                 |
| Im globalen Katalog      | Falsch                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------|
| Link-ID                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falsch                                                                 |
| Ist einwertig       | Richtig                                                                  |
| Ist indiziert             | Falsch                                                                 |
| Im globalen Katalog      | Falsch                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------|
| Link-ID                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falsch                                                                 |
| Is-Single-Valued       | Richtig                                                                  |
| Ist indiziert             | Falsch                                                                 |
| Im globalen Katalog      | Falsch                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------|
| Link-ID                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falsch                                                                 |
| Is-Single-Valued       | Richtig                                                                  |
| Ist indiziert             | Falsch                                                                 |
| Im globalen Katalog      | Falsch                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------|
| Link-ID                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | Falsch                                                                 |
| Is-Single-Valued       | Richtig                                                                  |
| Ist indiziert             | Falsch                                                                 |
| Im globalen Katalog      | Falsch                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





