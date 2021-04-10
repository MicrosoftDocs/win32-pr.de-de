---
title: MS-DFS-Link-Path-v2-Attribut
description: Der DFS-Linkpfad relativ zur DFS-Stamm Ziel Freigabe (also ohne die Komponenten Server/Domäne und DFS-Namespace Name). Verwenden Sie Schrägstriche (/) anstelle von umgekehrten Schrägstrichen ( \) , damit LDAP-Suchvorgänge ausgeführt werden können, ohne dass Escapezeichen verwendet werden müssen.
ms.assetid: 98fd6e99-0d7e-4ffa-b8ec-d26ca03ffead
ms.tgt_platform: multiple
keywords:
- MS-DFS-Link-Path-v2-Attribut AD-Schema
- Schema für msdfs-LinkPathv2-Attribut
topic_type:
- apiref
api_name:
- ms-DFS-Link-Path-v2
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 892cee6a5e6f423a0ed750858e19e1accccbe45f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104123019"
---
# <a name="ms-dfs-link-path-v2-attribute"></a>MS-DFS-Link-Path-v2-Attribut

Der DFS-Linkpfad relativ zur DFS-Stamm Ziel Freigabe (also ohne die Komponenten Server/Domäne und DFS-Namespace Name). Verwenden Sie Schrägstriche (/) anstelle von umgekehrten Schrägstrichen ( \) , damit LDAP-Suchvorgänge ausgeführt werden können, ohne dass Escapezeichen verwendet werden müssen.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | MS-DFS-Link-Path-v2                         |
| LDAP-Display-Name | msdfs-LinkPathv2                            |
| Size              | \-                                          |
| Berechtigung aktualisieren  | \-                                          |
| Aktualisierungshäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.2039                     |
| System-ID-GUID    | 86b021f 6-10ab-40A2-A252-1dc0cc3be6a9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                     |
| MAPI-Id                | \-                                                                                                                     |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | False                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | 0                                                                                                                      |
| Range-Upper            | 32766                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**MS-DFS-Deleted-Link-v2**](c-msdfs-deletedlinkv2.md)<br/> [**MS-DFS-Link-v2**](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                     |
| MAPI-Id                | \-                                                                                                                     |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | False                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | 0                                                                                                                      |
| Range-Upper            | 32766                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**MS-DFS-Deleted-Link-v2**](c-msdfs-deletedlinkv2.md)<br/> [**MS-DFS-Link-v2**](c-msdfs-linkv2.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                     |
| MAPI-Id                | \-                                                                                                                     |
| System-Only            | False                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                   |
| Ist indiziert             | False                                                                                                                  |
| Im globalen Katalog      | False                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                           |
| Range-Lower            | 0                                                                                                                      |
| Range-Upper            | 32766                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                             |
| System-Flags           | 0x00000010                                                                                                             |
| In verwendete Klassen        | [**MS-DFS-Deleted-Link-v2**](c-msdfs-deletedlinkv2.md)<br/> [**MS-DFS-Link-v2**](c-msdfs-linkv2.md)<br/> |



 

 





