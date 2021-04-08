---
title: Rid-Previous-Allocation-Pool-Attribut
description: Enthält den Pool relativer Bezeichner (RIDs), von denen ein Domänen Controller zugeordnet wird.
ms.assetid: d2f60259-388b-4dea-a1f7-9e650b1a66db
ms.tgt_platform: multiple
keywords:
- AD-Schema für Rid-Previous-Allocation-Pool-Attribut
- "\"ridpreviousallocationpool\"-Attribut, AD-Schema"
topic_type:
- apiref
api_name:
- RID-Previous-Allocation-Pool
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15438d55c9540ecca873395cc329058bc0773399
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859577"
---
# <a name="rid-previous-allocation-pool-attribute"></a>Rid-Previous-Allocation-Pool-Attribut

Das **RID-Previous-Allocation-Pool-** Attribut enthält den Pool von relativen Bezeichners (RIDs), von denen ein Domänen Controller zuweist. Bei diesem Attribut handelt es sich um einen 8-Byte-Wert, der ein paar von vier-Byte-Ganzzahlen enthält, die die Start-und Endwerte des RID-Pools darstellen. Der Startwert liegt in den unteren vier Bytes, und der Endwert liegt in den oberen vier Bytes.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Rid-Previous-Allocation-Pool         |
| LDAP-Display-Name | ridpreviousallocationpool            |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.372               |
| System-ID-GUID    | 6617188a-8-Datei mit dem Namen "", "AFDA-00c04" |
| Syntax            | [**Intervall**](s-interval.md)       |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Ist-einwertig       | Richtig                                   |
| Ist indiziert             | False                                  |
| Im globalen Katalog      | False                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**Rid-Satz**](c-ridset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------|
| Link-ID                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Richtig                                   |
| Ist-einwertig       | Richtig                                   |
| Ist indiziert             | False                                  |
| Im globalen Katalog      | False                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**Rid-Satz**](c-ridset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------|
| Link-ID                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Richtig                                   |
| Ist-einwertig       | Richtig                                   |
| Ist indiziert             | False                                  |
| Im globalen Katalog      | False                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**Rid-Satz**](c-ridset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------|
| Link-ID                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Richtig                                   |
| Ist-einwertig       | Richtig                                   |
| Ist indiziert             | False                                  |
| Im globalen Katalog      | False                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**Rid-Satz**](c-ridset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------|
| Link-ID                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Richtig                                   |
| Ist-einwertig       | Richtig                                   |
| Ist indiziert             | False                                  |
| Im globalen Katalog      | False                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**Rid-Satz**](c-ridset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------|
| Link-ID                | \-                                     |
| MAPI-Id                | \-                                     |
| System-Only            | Richtig                                   |
| Ist-einwertig       | Richtig                                   |
| Ist indiziert             | False                                  |
| Im globalen Katalog      | False                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                           |
| Range-Lower            | \-                                     |
| Range-Upper            | \-                                     |
| Search-Flags           | 0x00000000                             |
| System-Flags           | 0x00000011                             |
| In verwendete Klassen        | [**Rid-Satz**](c-ridset.md)<br/> |



 

 





