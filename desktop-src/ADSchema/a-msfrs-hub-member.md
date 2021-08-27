---
title: ms-FRS-Hub-Member-Attribut
description: Das attribut ms-FRS-Hub-Member wird verwendet, um die bevorzugten NTFRS-Topologieeinstellungen zu erfassen.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- AD-Schema des ms-FRS-Hub-Member-Attributs
- AD-Schema des msFRS-Hub-Member-Attributs
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f2cc1014b081ac13183144fca34c2087539de0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885708"
---
# <a name="ms-frs-hub-member-attribute"></a>ms-FRS-Hub-Member-Attribut

Das **attribut ms-FRS-Hub-Member** wird verwendet, um die bevorzugten NTFRS-Topologieeinstellungen zu erfassen. Wenn ein FRS-Mitglied einer Replikatgruppe hinzugefügt oder gelöscht wird, werden auf diese Attribute verwiesen, und es werden entsprechende Anpassungen an den Verbindungen zwischen den restlichen FRS-Membern in der Replikatgruppe vorgenommen.



| Eingabe | Wert |
|-------------------|--------------------------------------------------------------------|
| CN                | ms-FRS-Hub-Member                                                  |
| Ldap-Anzeigename | msFRS-Hub-Member                                                   |
| Size              | \-                                                                 |
| Aktualisieren von Berechtigungen  | Domänenadministrator                                               |
| Updatehäufigkeit  | Wenn die Replikatgruppe erstellt wird oder sich die bevorzugte Topologie ändert. |
| Attribute-Id      | 1.2.840.113556.1.4.1693                                            |
| System-Id-Guid    | 5643ff81-35b6-4ca9-9512-baf0bd0a2772                               |
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
| Is-Single-Valued       | True                                                      |
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
| Is-Single-Valued       | True                                                      |
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
| Is-Single-Valued       | True                                                      |
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
| Ist einwertig       | True                                                      |
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
| Ist einwertig       | True                                                      |
| Ist indiziert             | False                                                     |
| Im globalen Katalog      | False                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| In verwendete Klassen        | [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a>Hinweise

Dies ist der vollqualifizierte Distinguished Name eines [**NTFRS-Member-Objekts.**](c-ntfrsmember.md) Der Distinguished Name weist das Format "CN=*&lt; &gt; computerGuid*, CN= *<Dfs Link Name>* , CN= *<Dfs Root name>* , CN=DFS Volumes, CN=File Replication Service,CN=System, DC=..." auf.

 

 





