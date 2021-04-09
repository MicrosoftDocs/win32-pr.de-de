---
title: Tombstone-Lifetime-Attribut
description: Die Anzahl der Tage, bevor ein gelöschtes Objekt aus den Verzeichnisdiensten entfernt wird.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- AD-Schema für Tombstone-Lifetime-Attribut
- tombstoneLifetime-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb2bd0b7b970270c626437ee65288fd07bf48272
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103859747"
---
# <a name="tombstone-lifetime-attribute"></a>Tombstone-Lifetime-Attribut

Die Anzahl der Tage, bevor ein gelöschtes Objekt aus den Verzeichnisdiensten entfernt wird. Dies hilft beim Entfernen von Objekten von replizierten Servern und verhindert, dass Wiederherstellungen ein gelöschtes Objekt erneut einführen. Dieser Wert befindet sich im Verzeichnisdienst Objekt in der Konfigurations-NIC.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------|
| CN                | Tombstone-Lifetime                                        |
| LDAP-Display-Name | tombstoneLifetime                                         |
| Size              | 4 Bytes. Der Standardwert ist 60 Tage, wenn kein Wert eingegeben wird. |
| Berechtigung aktualisieren  | \-                                                        |
| Aktualisierungshäufigkeit  | \-                                                        |
| Attribute-Id      | 1.2.840.113556.1.2.54                                     |
| System-ID-GUID    | 16c3a860-1273-11D0-a060-00aa006c33ed                      |
| Syntax            | [**Enumeration**](s-enumeration.md)                      |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Ist-einwertig       | Richtig                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Ist-einwertig       | Richtig                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Ist-einwertig       | Richtig                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Ist-einwertig       | Richtig                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Ist-einwertig       | Richtig                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Ist-einwertig       | Richtig                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Ist-einwertig       | Richtig                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Dienst**](c-ntdsservice.md)<br/> |



 

 





