---
title: Token-Groups-Attribut
description: Ein berechnetes Attribut, das die Liste der SIDs aufgrund einer transitiven Erweiterung der Gruppenmitgliedschaft auf einem bestimmten Benutzer oder Computer enthält. Tokengruppen können nicht abgerufen werden, wenn kein globaler Katalog vorhanden ist, um die transitiven umgekehrten Mitgliedschaften abzurufen.
ms.assetid: bb430c9f-20b7-4f21-804d-fbd4864b6505
ms.tgt_platform: multiple
keywords:
- Token-Groups AD-Schema
- tokenGroups-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Token-Groups
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b8971f9ba5baead73b7704760dcc86430f5ce1a318ac6bcbd9dfaf4125a21af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022068"
---
# <a name="token-groups-attribute"></a>Token-Groups-Attribut

Ein berechnetes Attribut, das die Liste der SIDs aufgrund einer transitiven Erweiterung der Gruppenmitgliedschaft auf einem bestimmten Benutzer oder Computer enthält. Tokengruppen können nicht abgerufen werden, wenn kein globaler Katalog vorhanden ist, um die transitiven umgekehrten Mitgliedschaften abzurufen.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Token-Groups                         |
| Ldap-Anzeigename | tokenGroups                          |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.     |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1301              |
| System-Id-Guid    | b7c69e6d-2cc7-11d2-854e-00a0c983f608 |
| Syntax            | [**String(Sid)**](s-string-sid.md)  |



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
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falsch                                                        |
| Is-Single-Valued       | Falsch                                                        |
| Ist indiziert             | Falsch                                                        |
| Im globalen Katalog      | Falsch                                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x08000014                                                   |
| In verwendete Klassen        | [**Sicherheitsprinzipal**](c-securityprincipal.md)<br/> |



 

 





