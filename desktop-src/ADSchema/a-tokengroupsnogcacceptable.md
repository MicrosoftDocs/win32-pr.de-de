---
title: Token-Groups-No-GC-Acceptable-Attribut
description: Dieses Attribut enthält die Liste der SIDs aufgrund eines transitiven Vorgangs zur Erweiterung der Gruppenmitgliedschaft auf einem bestimmten Benutzer oder Computer. Tokengruppen können nicht abgerufen werden, wenn kein globaler Katalog vorhanden ist, um die transitiven umgekehrten Mitgliedschaften abzurufen.
ms.assetid: 08718c69-6339-40dc-8486-a7cd72028ed1
ms.tgt_platform: multiple
keywords:
- Ad-Schema des Attributs "Token-Groups-No-GC-Acceptable"
- tokenGroupsNoGCAcceptable-Attribut-AD-Schema
topic_type:
- apiref
api_name:
- Token-Groups-No-GC-Acceptable
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cc625d75409e266c90efa9a5a4cea5d7d3cf741c6e14f00faa8aa263ef88853
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119835830"
---
# <a name="token-groups-no-gc-acceptable-attribute"></a>Token-Groups-No-GC-Acceptable-Attribut

Dieses Attribut enthält die Liste der SIDs aufgrund eines transitiven Vorgangs zur Erweiterung der Gruppenmitgliedschaft auf einem bestimmten Benutzer oder Computer. Tokengruppen können nicht abgerufen werden, wenn kein globaler Katalog vorhanden ist, um die transitiven umgekehrten Mitgliedschaften abzurufen.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Tokengruppen– keine GC-akzeptabel        |
| Ldap-Anzeigename | tokenGroupsNoGCAcceptable            |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | Das System legt diesen Wert fest.          |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1303              |
| System-ID-GUID    | 040fc392-33df-11d2-98b2-0000f87a57d4 |
| Syntax            | [**String(Sid)**](s-string-sid.md)  |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Ist einwertig       | Falsch                                                        |
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
| Ist einwertig       | Falsch                                                        |
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
| Ist einwertig       | Falsch                                                        |
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



 

 





