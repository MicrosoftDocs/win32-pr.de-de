---
title: MS-FRS-Hub-Member-Attribut
description: Das MS-FRS-Hub-Member-Attribut wird verwendet, um die bevorzugten NTFRS-topologieeinstellungen aufzuzeichnen.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- AD-Schema für MS-FRS-Hub-Member-Attribut
- AD-Schema für msfrs-Hub-Member-Attribut
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a211c5951ac589d00c4b8c92c031c80b2d1415
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106342909"
---
# <a name="ms-frs-hub-member-attribute"></a>MS-FRS-Hub-Member-Attribut

Das **MS-FRS-Hub-Member-** Attribut wird verwendet, um die bevorzugten NTFRS-topologieeinstellungen aufzuzeichnen. Wenn ein FRS-Element einer Replikat Gruppe hinzugefügt oder gelöscht wird, werden diese Attribute referenziert, und es werden entsprechende Anpassungen an den Verbindungen zwischen dem Rest der FRS-Mitglieder in der Replikat Gruppe vorgenommen.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------|
| CN                | MS-FRS-Hub-Member                                                  |
| LDAP-Display-Name | msfrs-Hub-Member                                                   |
| Size              | \-                                                                 |
| Berechtigung aktualisieren  | Domänen Administrator                                               |
| Aktualisierungshäufigkeit  | Wenn die Replikat Gruppe erstellt oder die bevorzugte Topologie geändert wird. |
| Attribute-Id      | 1.2.840.113556.1.4.1693                                            |
| System-ID-GUID    | 5643ff81-35b6-4ca9-9512-baf0bd0a2772                               |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)                            |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist-einwertig       | Richtig                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist-einwertig       | Richtig                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist-einwertig       | Richtig                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist-einwertig       | Richtig                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist-einwertig       | Richtig                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a>Bemerkungen

Dies ist der voll qualifizierte Distinguished Name eines [**NTFRS-Member-**](c-ntfrsmember.md) Objekts. Der Distinguished Name hat das Format "CN = *<computerGuid>* , CN = *<Dfs Link Name>* , CN = *<Dfs Root name>* , CN = DFS Volumes, CN = File Replication Service, CN = System, DC =..."

 

 





