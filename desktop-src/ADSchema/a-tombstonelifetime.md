---
title: Tombstone-Lifetime-Attribut
description: Die Anzahl von Tagen, bevor ein gelöschtes Objekt aus den Verzeichnisdiensten entfernt wird.
ms.assetid: 58898097-912b-4fe6-b6ea-91f49aaa2b1b
ms.tgt_platform: multiple
keywords:
- Tombstone-Lifetime AD-Schema
- TOMBSTONELifetime-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Tombstone-Lifetime
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c96d440b82f488e7968f787ae52d9f431350bee6050bd50b385f5751f51e76a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644950"
---
# <a name="tombstone-lifetime-attribute"></a>Tombstone-Lifetime-Attribut

Die Anzahl von Tagen, bevor ein gelöschtes Objekt aus den Verzeichnisdiensten entfernt wird. Dies hilft, Objekte von replizierten Servern zu entfernen und zu verhindern, dass Wiederherstellungen ein gelöschtes Objekt erneut bereitstellen. Dieser Wert befindet sich im Verzeichnisdienstobjekt in der Konfigurations-NIC.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------|
| CN                | Tombstone-Lifetime                                        |
| Ldap-Anzeigename | Tombstonelifetime                                         |
| Size              | 4 Bytes. Der Standardwert ist 60 Tage, wenn kein Wert eingegeben wird. |
| Aktualisieren von Berechtigungen  | \-                                                        |
| Updatehäufigkeit  | \-                                                        |
| Attribute-Id      | 1.2.840.113556.1.2.54                                     |
| System-Id-Guid    | 16c3a860-1273-11d0-a060-00aa006c33ed                      |
| Syntax            | [**Enumeration**](s-enumeration.md)                      |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
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
| Is-Single-Valued       | True                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Is-Single-Valued       | True                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Is-Single-Valued       | True                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Ist einwertig       | True                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Ist einwertig       | True                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Ist einwertig       | True                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------------|
| Link-ID                | \-                                               |
| MAPI-Id                | 0x8145                                           |
| System-Only            | False                                            |
| Ist einwertig       | True                                             |
| Ist indiziert             | False                                            |
| Im globalen Katalog      | False                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| In verwendete Klassen        | [**NTDS-Service**](c-ntdsservice.md)<br/> |



 

 





