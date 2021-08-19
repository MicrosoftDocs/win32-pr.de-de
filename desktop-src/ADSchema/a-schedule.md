---
title: Schedule-Attribut
description: Ein zeitplanorientiertes BLOB gemäß definition Windows NT Job Service. Wird von der Replikation verwendet.
ms.assetid: 5eb6409d-3fb5-4368-8b7f-ce19567b7260
ms.tgt_platform: multiple
keywords:
- AD-Schema des Zeitplanattributs
- AD-Schema des Zeitplanattributs
topic_type:
- apiref
api_name:
- Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b65ff20b9eaba0c8429f5fec164e44a3e4b842e82bfddcca61461f6832f55d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022218"
---
# <a name="schedule-attribute"></a>Schedule-Attribut

Ein zeitplanorientiertes BLOB gemäß definition Windows NT Job Service. Wird von der Replikation verwendet.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Zeitplan                                              |
| Ldap-Anzeigename | schedule                                              |
| Size              | \-                                                    |
| Aktualisieren von Berechtigungen  | \-                                                    |
| Updatehäufigkeit  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.211                                |
| System-Id-Guid    | dd712224-10e4-11d0-a05f-00aa006c33ed                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falsch                                                                                                                                                                                                                                                                            |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Einstellungen**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falsch                                                                                                                                                                                                                                                                            |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Einstellungen**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                            |
| MAPI-Id                | \-                                                                                                                                                            |
| System-Only            | Falsch                                                                                                                                                         |
| Is-Single-Valued       | Richtig                                                                                                                                                          |
| Ist indiziert             | Falsch                                                                                                                                                         |
| Im globalen Katalog      | Falsch                                                                                                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                  |
| Range-Lower            | \-                                                                                                                                                            |
| Range-Upper            | \-                                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                                                    |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Einstellungen**](c-ntdssitesettings.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falsch                                                                                                                                                                                                                                                                            |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Einstellungen**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falsch                                                                                                                                                                                                                                                                            |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Einstellungen**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falsch                                                                                                                                                                                                                                                                            |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Einstellungen**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | Falsch                                                                                                                                                                                                                                                                            |
| Is-Single-Valued       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | Falsch                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | Falsch                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Einstellungen**](c-ntdssitesettings.md)<br/> [**NTFRS-Replica-Set**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Subscriber**](c-ntfrssubscriber.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



 

 





