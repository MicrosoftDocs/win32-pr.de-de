---
title: Schedule-Attribut
description: Ein Zeitplan-BLOB, wie vom Windows NT-Auftrags Dienst definiert. Wird von der Replikation verwendet.
ms.assetid: 5eb6409d-3fb5-4368-8b7f-ce19567b7260
ms.tgt_platform: multiple
keywords:
- AD-Schema für Zeit Plan Attribut
- AD-Schema für Zeit Plan Attribut
topic_type:
- apiref
api_name:
- Schedule
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abf53e86f77ecffc872d8b007e32b1f964ae244e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107552"
---
# <a name="schedule-attribute"></a>Schedule-Attribut

Ein Zeitplan-BLOB, wie vom Windows NT-Auftrags Dienst definiert. Wird von der Replikation verwendet.



| Eingabe | Wert |
|-------------------|-------------------------------------------------------|
| CN                | Zeitplan                                              |
| LDAP-Display-Name | schedule                                              |
| Size              | \-                                                    |
| Berechtigung aktualisieren  | \-                                                    |
| Aktualisierungshäufigkeit  | \-                                                    |
| Attribute-Id      | 1.2.840.113556.1.4.211                                |
| System-ID-GUID    | dd712224-10e4-11d0-a05f-00aa006c33ed                  |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md) |



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
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | False                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Abonnent**](c-ntfrssubscriber.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | False                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Abonnent**](c-ntfrssubscriber.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                            |
| MAPI-Id                | \-                                                                                                                                                            |
| System-Only            | False                                                                                                                                                         |
| Ist-einwertig       | Richtig                                                                                                                                                          |
| Ist indiziert             | False                                                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                  |
| Range-Lower            | \-                                                                                                                                                            |
| Range-Upper            | \-                                                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                                                    |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | False                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Abonnent**](c-ntfrssubscriber.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | False                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Abonnent**](c-ntfrssubscriber.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | False                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Abonnent**](c-ntfrssubscriber.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                               |
| System-Only            | False                                                                                                                                                                                                                                                                            |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                             |
| Ist indiziert             | False                                                                                                                                                                                                                                                                            |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                            |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                                     |
| Range-Lower            | \-                                                                                                                                                                                                                                                                               |
| Range-Upper            | \-                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                       |
| In verwendete Klassen        | [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**NTFRS-Replikat Satz**](c-ntfrsreplicaset.md)<br/> [**NTFRS-Abonnent**](c-ntfrssubscriber.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



 

 





