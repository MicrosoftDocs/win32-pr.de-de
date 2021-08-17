---
title: FRS-Version-GUID-Attribut
description: Wenn dieser Wert vorhanden ist, deutet die Änderung dieses Werts darauf hin, dass eine Konfigurationsänderung an dieser Replikatgruppe vorgenommen wurde.
ms.assetid: 27cd68c5-a8aa-4c14-bf1d-0eb7c4d9cca5
ms.tgt_platform: multiple
keywords:
- FRS-Version-GUID-Attribut AD-Schema
- AD-Schema des fRSVersionGUID-Attributs
topic_type:
- apiref
api_name:
- FRS-Version-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701fb9da7a876a39858cb6d38383f58d8ddc1231940df2c2fb922e0e05e00520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961429"
---
# <a name="frs-version-guid-attribute"></a>FRS-Version-GUID-Attribut

Wenn dieser Wert vorhanden ist, deutet die Änderung dieses Werts darauf hin, dass eine Konfigurationsänderung an dieser Replikatgruppe vorgenommen wurde.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | FRS-Version-GUID                                      |
| Ldap-Anzeigename | fRSVersionGUID                                        |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | \-                                                    |
| Updatehäufigkeit  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.43                                 |
| System-Id-Guid    | 26d9736c-6070-11d1-a9c6-0000f80367c1                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementierungen

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falsch                                                     |
| Is-Single-Valued       | Richtig                                                      |
| Ist indiziert             | Falsch                                                     |
| Im globalen Katalog      | Falsch                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | 16                                                        |
| Range-Upper            | 16                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000010                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falsch                                                     |
| Is-Single-Valued       | Richtig                                                      |
| Ist indiziert             | Falsch                                                     |
| Im globalen Katalog      | Falsch                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | 16                                                        |
| Range-Upper            | 16                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000010                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falsch                                                     |
| Is-Single-Valued       | Richtig                                                      |
| Ist indiziert             | Falsch                                                     |
| Im globalen Katalog      | Falsch                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | 16                                                        |
| Range-Upper            | 16                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000010                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falsch                                                     |
| Ist einwertig       | Richtig                                                      |
| Ist indiziert             | Falsch                                                     |
| Im globalen Katalog      | Falsch                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | 16                                                        |
| Range-Upper            | 16                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000010                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falsch                                                     |
| Ist einwertig       | Richtig                                                      |
| Ist indiziert             | Falsch                                                     |
| Im globalen Katalog      | Falsch                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | 16                                                        |
| Range-Upper            | 16                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000010                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | \-                                                        |
| MAPI-Id                | \-                                                        |
| System-Only            | Falsch                                                     |
| Ist einwertig       | Richtig                                                      |
| Ist indiziert             | Falsch                                                     |
| Im globalen Katalog      | Falsch                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | 16                                                        |
| Range-Upper            | 16                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000010                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



 

 





