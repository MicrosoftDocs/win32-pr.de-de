---
title: Builtin-Creation-Time-Attribut
description: Das Builtin-Creation-Time-Attribut wird verwendet, um die Replikation in Windows NT 4.0-Domänen zu unterstützen.
ms.assetid: b3da9913-8c7b-481b-ae47-6b124544f1e2
ms.tgt_platform: multiple
keywords:
- Ad-Schema für integriertes Erstellungszeitattribut
- builtinCreationTime-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Builtin-Creation-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f49db533ad85dc9531a1274687ebe70e728dba6f5c27e952a443344be3d02f12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442740"
---
# <a name="builtin-creation-time-attribute"></a>Builtin-Creation-Time-Attribut

Das **Builtin-Creation-Time-Attribut** wird verwendet, um die Replikation in Windows NT 4.0-Domänen zu unterstützen.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Builtin-Creation-Time                |
| Ldap-Anzeigename | builtinCreationTime                  |
| Size              | 8 Bytes                              |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.     |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.13                |
| System-Id-Guid    | bf96792f-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Intervall**](s-interval.md)       |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Is-Single-Valued       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Is-Single-Valued       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Is-Single-Valued       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | Falsch                                        |
| Ist einwertig       | Richtig                                         |
| Ist indiziert             | Falsch                                        |
| Im globalen Katalog      | Falsch                                        |
| NT-Security-Descriptor | O:BAG:BAD:S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domain**](c-samdomain.md)<br/> |



 

 





