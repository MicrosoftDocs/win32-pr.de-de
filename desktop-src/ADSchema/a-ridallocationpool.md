---
title: RID-Allocation-Pool-Attribut
description: Ein Pool, der vorab für die Verwendung durch den RID-Manager abgerufen wurde, wenn RID-Previous-Allocation-Pool aufbeutet wurde.
ms.assetid: 6d49b497-322f-424c-badc-4801f51481f3
ms.tgt_platform: multiple
keywords:
- AD-Schema des RID-Allocation-Pool-Attributs
- AD-Schema des rIDAllocationPool-Attributs
topic_type:
- apiref
api_name:
- RID-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce6ff101ca49e8d2ffafdb31f2d05cf1cb2371ee3336525ab31318925d349805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837380"
---
# <a name="rid-allocation-pool-attribute"></a>RID-Allocation-Pool-Attribut

Ein Pool, der vorab für die Verwendung durch den RID-Manager abgerufen wurde, wenn RID-Previous-Allocation-Pool aufbeutet wurde.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | RID-Allocation-Pool                  |
| Ldap-Anzeigename | rIDAllocationPool                    |
| Size              | 8 Bytes                              |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.     |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.371               |
| System-Id-Guid    | 66171889-8f3c-11d0-afda-00c04fd930c9 |
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
| System-Flags           | 0x00000010                             |
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
| System-Flags           | 0x00000010                             |
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
| System-Flags           | 0x00000010                             |
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
| System-Flags           | 0x00000010                             |
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
| System-Flags           | 0x00000010                             |
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
| System-Flags           | 0x00000010                             |
| In verwendete Klassen        | [**RID-Set**](c-ridset.md)<br/> |



 

 





