---
title: RID-Previous-Allocation-Pool-Attribut
description: Enthält den Pool mit relativen Bezeichnern (RIDs), aus denen ein Domänencontroller zuteilen ist.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- RID-Previous-Allocation-Pool-Attribut AD-Schema
- rIDPreviousAllocationPool-Attribut AD-Schema
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5199d9fd0f91b94ed6625a8759f3a5acd76a892460c44e3315911350f0ff59f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837360"
---
# <a name="rid-previous-allocation-pool-attribute"></a>RID-Previous-Allocation-Pool-Attribut

Das **RID-Previous-Allocation-Pool-Attribut** enthält den Pool mit relativen Bezeichnern (RIDs), aus denen ein Domänencontroller zuteilen ist. Dieses Attribut ist ein Acht-Byte-Wert, der ein Paar aus ganzen Zahlen mit vier Byte enthält, die die Start- und Endwerte des RID-Pools darstellen. Der Startwert liegt in den unteren vier Bytes und der Endwert in den oberen vier Bytes.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | RID-Previous-Allocation-Pool         |
| Ldap-Anzeigename | rIDPreviousAllocationPool            |
| Size              | \-                                   |
| Aktualisieren von Berechtigungen  | \-                                   |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.372               |
| System-Id-Guid    | 6617188a-8f3c-11d0-afda-00c04fd930c9 |
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
|------------------------|----------------------------------------|
| Link-ID                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Richtig                                   |
| Is-Single-Valued       | Richtig                                   |
| Ist indiziert             | Falsch                                  |
| Im globalen Katalog      | Falsch                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------|
| Link-ID                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Richtig                                   |
| Is-Single-Valued       | Richtig                                   |
| Ist indiziert             | Falsch                                  |
| Im globalen Katalog      | Falsch                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------|
| Link-ID                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Richtig                                   |
| Is-Single-Valued       | Richtig                                   |
| Ist indiziert             | Falsch                                  |
| Im globalen Katalog      | Falsch                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------|
| Link-ID                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Richtig                                   |
| Is-Single-Valued       | Richtig                                   |
| Ist indiziert             | Falsch                                  |
| Im globalen Katalog      | Falsch                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------|
| Link-ID                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Richtig                                   |
| Is-Single-Valued       | Richtig                                   |
| Ist indiziert             | Falsch                                  |
| Im globalen Katalog      | Falsch                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**RID-Set**](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------|
| Link-ID                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Richtig                                   |
| Is-Single-Valued       | Richtig                                   |
| Ist indiziert             | Falsch                                  |
| Im globalen Katalog      | Falsch                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**RID-Set**](c-ridset.md)<br/> |



 

 





