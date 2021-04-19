---
title: MS-DFSR-FileFilter-Attribut
description: Enthält die Filter Zeichenfolge, die zum Filtern von Dateien verwendet wird.
ms.assetid: e9c57328-e7c0-4149-aa1d-64603844e001
ms.tgt_platform: multiple
keywords:
- MS-DFSR-FileFilter-Attribut, AD-Schema
- msdfsr-FileFilter-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- ms-DFSR-FileFilter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 597a5e722cd38213d0c668c0afdfc6094288ae80
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344540"
---
# <a name="ms-dfsr-filefilter-attribute"></a>MS-DFSR-FileFilter-Attribut

Enthält die Filter Zeichenfolge, die zum Filtern von Dateien verwendet wird.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | MS-DFSR-FileFilter                          |
| LDAP-Display-Name | msdfsr-FileFilter                           |
| Size              | \-                                          |
| Berechtigung aktualisieren  | \-                                          |
| Aktualisierungshäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.6.13.3.12                  |
| System-ID-GUID    | d68270ac-a5dc-4841-a6ac-cd68be38c181        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------------------|
| Link-ID                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | False                                                        |
| Ist-einwertig       | Richtig                                                         |
| Ist indiziert             | False                                                        |
| Im globalen Katalog      | False                                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                 |
| Range-Lower            | 0                                                            |
| Range-Upper            | 32767                                                        |
| Search-Flags           | 0x00000000                                                   |
| System-Flags           | 0x00000000                                                   |
| In verwendete Klassen        | [**MS-DFSR-contentset**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | False                                                                                                                                 |
| Ist-einwertig       | Richtig                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                          |
| Range-Lower            | 0                                                                                                                                     |
| Range-Upper            | 32767                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| In verwendete Klassen        | [**MS-DFSR-replicationgroup**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-contentset**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | False                                                                                                                                 |
| Ist-einwertig       | Richtig                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                          |
| Range-Lower            | 0                                                                                                                                     |
| Range-Upper            | 32767                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| In verwendete Klassen        | [**MS-DFSR-replicationgroup**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-contentset**](c-msdfsr-contentset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | False                                                                                                                                 |
| Ist-einwertig       | Richtig                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                          |
| Range-Lower            | 0                                                                                                                                     |
| Range-Upper            | 32767                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| In verwendete Klassen        | [**MS-DFSR-replicationgroup**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-contentset**](c-msdfsr-contentset.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Das **MS-DFSR-FileFilter-** Attribut ist ein Teil der Unterstützung für den verteiltes Dateisystem (DFS)-Replikations Dienst.

 

 





