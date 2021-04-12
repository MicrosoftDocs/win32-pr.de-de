---
title: MS-DFSR-Schedule-Attribut
description: Enthält den Replikations Zeitplan für den verteiltes Dateisystem (DFS)-Replikations Dienst.
ms.assetid: 6dfcce16-44a4-4f7a-93ba-0c0d50605682
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-DFSR-Schedule-Attribut
- "\"msdfsr-Schedule\"-Attribut AD-Schema"
topic_type:
- apiref
api_name:
- ms-DFSR-Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118ab92c656899d8275f0ff63ae43b412cf9742e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104480130"
---
# <a name="ms-dfsr-schedule-attribute"></a>MS-DFSR-Schedule-Attribut

Enthält den Replikations Zeitplan für den verteiltes Dateisystem (DFS)-Replikations Dienst.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | MS-DFSR-Zeitplan                                      |
| LDAP-Display-Name | msdfsr-Zeitplan                                       |
| Size              | \-                                                    |
| Berechtigung aktualisieren  | \-                                                    |
| Aktualisierungshäufigkeit  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.6.13.3.14                            |
| System-ID-GUID    | 4699f15f-a71f-48e2-9ff5-5897c0759205                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                    |
| System-Only            | False                                                                                                                                 |
| Ist-einwertig       | Richtig                                                                                                                                  |
| Ist indiziert             | False                                                                                                                                 |
| Im globalen Katalog      | False                                                                                                                                 |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                          |
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| In verwendete Klassen        | [**MS-DFSR-replicationgroup**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-Verbindung**](c-msdfsr-connection.md)<br/> |



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
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| In verwendete Klassen        | [**MS-DFSR-replicationgroup**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-Verbindung**](c-msdfsr-connection.md)<br/> |



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
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| In verwendete Klassen        | [**MS-DFSR-replicationgroup**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-Verbindung**](c-msdfsr-connection.md)<br/> |



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
| Range-Lower            | 336                                                                                                                                   |
| Range-Upper            | 336                                                                                                                                   |
| Search-Flags           | 0x00000000                                                                                                                            |
| System-Flags           | 0x00000000                                                                                                                            |
| In verwendete Klassen        | [**MS-DFSR-replicationgroup**](c-msdfsr-replicationgroup.md)<br/> [**MS-DFSR-Verbindung**](c-msdfsr-connection.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Das-Attribut ist ein Teil der Unterstützung für den verteiltes Dateisystem (DFS)-Replikations Dienst.

 

 





