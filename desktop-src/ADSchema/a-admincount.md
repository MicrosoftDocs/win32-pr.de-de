---
title: Admin-Count-Attribut
description: Gibt an, dass die ACLs für ein bestimmtes Objekt vom System in einen sichereren Wert geändert wurden, weil es Mitglied einer der administrativen Gruppen (direkt oder transitiv) war.
ms.assetid: b2384ada-a792-42fa-be64-291d23e00887
ms.tgt_platform: multiple
keywords:
- AD-Schema für Admin-Count-Attribut
- adminCount-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Admin-Count
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95b953aebaa39bb3fc3e4c9cf96632f32a37850
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103745305"
---
# <a name="admin-count-attribute"></a>Admin-Count-Attribut

Gibt an, dass die ACLs für ein bestimmtes Objekt vom System in einen sichereren Wert geändert wurden, weil es Mitglied einer der administrativen Gruppen (direkt oder transitiv) war.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------|
| CN                | Admin-Count                                         |
| LDAP-Display-Name | adminCount                                          |
| Size              | 4 Bytes                                             |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.                    |
| Aktualisierungshäufigkeit  | Wenn ein Objekt einer administrativen Gruppe hinzugefügt wird. |
| Attribute-Id      | 1.2.840.113556.1.4.150                              |
| System-ID-GUID    | bf967918-0de6-11d0-a285-00aa003049e2                |
| Syntax            | [**Enumeration**](s-enumeration.md)                |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------|
| Link-ID                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | False                                                                 |
| Ist-einwertig       | Richtig                                                                  |
| Ist indiziert             | False                                                                 |
| Im globalen Katalog      | False                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Benutzer**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------------------|
| Link-ID                | \-                                                                    |
| MAPI-Id                | \-                                                                    |
| System-Only            | False                                                                 |
| Ist-einwertig       | Richtig                                                                  |
| Ist indiziert             | False                                                                 |
| Im globalen Katalog      | False                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                          |
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
| System-Only            | False                                                                 |
| Ist-einwertig       | Richtig                                                                  |
| Ist indiziert             | False                                                                 |
| Im globalen Katalog      | False                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                          |
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
| System-Only            | False                                                                 |
| Ist-einwertig       | Richtig                                                                  |
| Ist indiziert             | False                                                                 |
| Im globalen Katalog      | False                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                          |
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
| System-Only            | False                                                                 |
| Ist-einwertig       | Richtig                                                                  |
| Ist indiziert             | False                                                                 |
| Im globalen Katalog      | False                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                          |
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
| System-Only            | False                                                                 |
| Ist-einwertig       | Richtig                                                                  |
| Ist indiziert             | False                                                                 |
| Im globalen Katalog      | False                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                          |
| Range-Lower            | \-                                                                    |
| Range-Upper            | \-                                                                    |
| Search-Flags           | 0x00000000                                                            |
| System-Flags           | 0x00000010                                                            |
| In verwendete Klassen        | [**Gruppe**](c-group.md)<br/> [**Benutzer**](c-user.md)<br/> |



 

 





