---
title: Token-Groups-Attribut
description: Ein berechnetes Attribut, das die Liste der SIDs aufgrund eines transitiven Gruppen Mitgliedschafts Erweiterungs Vorgangs für einen bestimmten Benutzer oder Computer enthält. Tokengruppen können nicht abgerufen werden, wenn kein globaler Katalog vorhanden ist, um die transitiven umgekehrten Mitgliedschaften abzurufen.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- AD-Schema für Token-Groups-Attribut
- Schema Gruppen-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5342d1ff2bf549796340532b0514d5c5b060c2c1
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344287"
---
# <a name="token-groups-attribute"></a>Token-Groups-Attribut

Ein berechnetes Attribut, das die Liste der SIDs aufgrund eines transitiven Gruppen Mitgliedschafts Erweiterungs Vorgangs für einen bestimmten Benutzer oder Computer enthält. Tokengruppen können nicht abgerufen werden, wenn kein globaler Katalog vorhanden ist, um die transitiven umgekehrten Mitgliedschaften abzurufen.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Token-Groups                         |
| LDAP-Display-Name | tokenGroups                          |
| Size              | \-                                   |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.     |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1301              |
| System-ID-GUID    | b7c69e6d-2cc7-11d2-854e-00a0c983f608 |
| Syntax            | [**Zeichenfolge (SID)**](s-string-sid.md)  |



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
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | False                                                        |
| Im globalen Katalog      | False                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | False                                                        |
| Im globalen Katalog      | False                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | False                                                        |
| Im globalen Katalog      | False                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | False                                                        |
| Im globalen Katalog      | False                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | False                                                        |
| Im globalen Katalog      | False                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | False                                                        |
| Im globalen Katalog      | False                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | False                                                        |
| Ist indiziert             | False                                                        |
| Im globalen Katalog      | False                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheits Prinzipal**](c-securityprincipal.md)<br/> |



 

 





