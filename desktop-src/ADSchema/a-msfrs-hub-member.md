---
title: ms-FRS-Hub-Member-Attribut
description: Das attribut ms-FRS-Hub-Member wird verwendet, um die bevorzugten NTFRS-Topologieeinstellungen aufzuzeichnen.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- MS-FRS-Hub-Member-Attribut AD-Schema
- MSFRS-Hub-Member-Attribut AD-Schema
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa08d1eb3cbb8086149192e6ecd5fa3880f01e6cfa1800468d2825c243b211e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803309"
---
# <a name="ms-frs-hub-member-attribute"></a>ms-FRS-Hub-Member-Attribut

Das **attribut ms-FRS-Hub-Member** wird verwendet, um die bevorzugten NTFRS-Topologieeinstellungen aufzuzeichnen. Wenn ein FRS-Mitglied einer Replikatgruppe hinzugefügt oder gelöscht wird, wird auf diese Attribute verwiesen, und die Verbindungen zwischen den restlichen FRS-Membern in der Replikatgruppe werden entsprechend angepasst.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------|
| CN                | ms-FRS-Hub-Member                                                  |
| Ldap-Anzeigename | msFRS-Hub-Member                                                   |
| Size              | \-                                                                 |
| Aktualisieren von Berechtigungen  | Domänenadministrator                                               |
| Updatehäufigkeit  | Wenn die Replikatgruppe erstellt wird oder sich die bevorzugte Topologie ändert. |
| Attribute-Id      | 1.2.840.113556.1.4.1693                                            |
| System-ID-GUID    | 5643ff81-35b6-4ca9-9512-baf0bd0a2772                               |
| Syntax            | [**Object(DS-DN)**](s-object-ds-dn.md)                            |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist einwertig       | True                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist einwertig       | True                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Ist einwertig       | True                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Is-Single-Valued       | True                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-----------------------------------------------------------|
| Link-ID                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | False                                                     |
| Is-Single-Valued       | True                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a>Hinweise

Dies ist der vollqualifizierte Distinguished Name eines [**NTFRS-Member-Objekts.**](c-ntfrsmember.md) Der Distinguished Name hat das Format "CN= *<computerGuid>* , CN= *<Dfs Link Name>* , CN= *<Dfs Root name>* , CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..."

 

 





