---
title: ms-DFS-Link-Path-v2-Attribut
description: DFS-Linkpfad relativ zur DFS-Stammzielfreigabe (d. h. ohne die Server-/Domänen- und DFS-Namespacenamenkomponenten). Verwenden Sie Schrägstriche (/) anstelle umgekehrter Schrägstriche ( \) , damit LDAP-Suchvorgänge ohne Escapevorgänge durchgeführt werden können.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- MS-DFS-Link-Path-v2-Attribut AD-Schema
- MSDFS-LinkPathv2-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4659dbf00c6a53c77a23e98836ea1af4eeb4c38a
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386859"
---
# <a name="ms-dfs-link-path-v2-attribute"></a>ms-DFS-Link-Path-v2-Attribut

DFS-Linkpfad relativ zur DFS-Stammzielfreigabe (d. h. ohne die Server-/Domänen- und DFS-Namespacenamenkomponenten). Verwenden Sie Schrägstriche (/) anstelle umgekehrter Schrägstriche \\ (), damit LDAP-Suchvorgänge ohne Escapevorgänge durchgeführt werden können.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | ms-DFS-Link-Path-v2                         |
| Ldap-Anzeigename | msDFS-LinkPathv2                            |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.2039                     |
| System-Id-Guid    | 86b021f6-10ab-40a2-a252-1dc0cc3be6a9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**WindowsServer 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>WindowsServer 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                     |
| MAPI-Id                | \-                                                                                                                     |
| System-Only            | Falsch                                                                                                                  |
| Ist einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                  |
| Im globalen Katalog      | Falsch                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 0                                                                                                                      |
| Range-Upper            | 32766                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**ms-DFS-Deleted-Link-v2**](c-msdfs-deletedlinkv2.md)<br/> [**ms-DFS-Link-v2**](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                     |
| MAPI-Id                | \-                                                                                                                     |
| System-Only            | Falsch                                                                                                                  |
| Ist einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                  |
| Im globalen Katalog      | Falsch                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 0                                                                                                                      |
| Range-Upper            | 32766                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**ms-DFS-Deleted-Link-v2**](c-msdfs-deletedlinkv2.md)<br/> [**ms-DFS-Link-v2**](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                     |
| MAPI-Id                | \-                                                                                                                     |
| System-Only            | Falsch                                                                                                                  |
| Ist einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | Falsch                                                                                                                  |
| Im globalen Katalog      | Falsch                                                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                           |
| Range-Lower            | 0                                                                                                                      |
| Range-Upper            | 32766                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**ms-DFS-Deleted-Link-v2**](c-msdfs-deletedlinkv2.md)<br/> [**ms-DFS-Link-v2**](c-msdfs-linkv2.md)<br/> |



 

 





