---
title: ms-DS-Logon-Time-Sync-Interval-Attribut
description: Dieses Attribut steuert die Granularität (in Tagen), mit der der Zeitpunkt der letzten Anmeldung für einen Benutzer oder Computer, der im lastLogonTimestamp-Attribut aufgezeichnet wurde, auf alle DCS in einer Domäne repliziert wird.
ms.assetid: f1f9f1f8-df60-44b5-965d-631c4dd4ef84
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-Logon-Time-Sync-Interval-Attribut
- AD-Schema des msDS-logontimesyncinterval-Attributs
topic_type:
- apiref
api_name:
- ms-DS-Logon-Time-Sync-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbf23ca77bda9dac76f02986be1c05c80559199
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104520167"
---
# <a name="ms-ds-logon-time-sync-interval-attribute"></a>ms-DS-Logon-Time-Sync-Interval-Attribut

Dieses Attribut steuert die Granularität (in Tagen), mit der der Zeitpunkt der letzten Anmeldung für einen Benutzer oder Computer, der im lastLogonTimestamp-Attribut aufgezeichnet wurde, auf alle DCS in einer Domäne repliziert wird.



| Eingabe | Wert |
|-------------------|------------------------------------------------------------------------------------------------------------|
| CN                | ms-DS-Logon-Time-Sync-Interval                                                                             |
| LDAP-Display-Name | MSDS-logontimesyncinterval                                                                                 |
| Size              | 4 Bytes                                                                                                    |
| Berechtigung aktualisieren  | Domänen Administrator                                                                                       |
| Aktualisierungshäufigkeit  | Da es sich hierbei um eine Richtlinien Einstellung handelt, wird Sie nur dann aktualisiert, wenn eine Änderung der Domänen weiten Richtlinie gewünscht wird. |
| Attribute-Id      | 1.2.840.113556.1.4.1784                                                                                    |
| System-ID-GUID    | ad7940f8-e43a-4a42-83bc-d688e59ea605                                                                       |
| Syntax            | [**Enumeration**](s-enumeration.md)                                                                       |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domäne**](c-samdomain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domäne**](c-samdomain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domäne**](c-samdomain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domäne**](c-samdomain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------|
| Link-ID                | \-                                           |
| MAPI-Id                | \-                                           |
| System-Only            | False                                        |
| Ist-einwertig       | Richtig                                         |
| Ist indiziert             | False                                        |
| Im globalen Katalog      | False                                        |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                 |
| Range-Lower            | \-                                           |
| Range-Upper            | \-                                           |
| Search-Flags           | 0x00000000                                   |
| System-Flags           | 0x00000010                                   |
| In verwendete Klassen        | [**Sam-Domäne**](c-samdomain.md)<br/> |



 

 





