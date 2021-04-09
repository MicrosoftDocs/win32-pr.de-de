---
title: Time-Refresh-Attribut
description: Dieses Attribut verfügt über das Intervall, in dem ein in einer Active Directory integrierter Zone enthaltener Ressourcen Daten Satz für den DNS-Server aktualisiert werden soll. Das Standardintervall beträgt 7 Tage.
ms.assetid: 9e473c29-7fcf-4d6d-8a7c-2791c7822c7d
ms.tgt_platform: multiple
keywords:
- AD-Schema für Time-Refresh-Attribut
- timerefresh-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Time-Refresh
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87bc360686b1692d2dbda1ee23ad6351e69d3afe
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957571"
---
# <a name="time-refresh-attribute"></a>Time-Refresh-Attribut

Dieses Attribut verfügt über das Intervall, in dem ein in einer Active Directory integrierter Zone enthaltener Ressourcen Daten Satz für den DNS-Server aktualisiert werden soll. Das Standardintervall beträgt 7 Tage.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Time-Refresh                         |
| LDAP-Display-Name | timerefresh                          |
| Size              | \-                                   |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.503               |
| System-ID-GUID    | ddac0cf1-af8f-11d0-afeb-00c04fd930c9 |
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
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Ist-einwertig       | Richtig                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Ist-einwertig       | Richtig                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Ist-einwertig       | Richtig                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Ist-einwertig       | Richtig                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Ist-einwertig       | Richtig                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                            |
| MAPI-Id                | \-                                                                                                                            |
| System-Only            | False                                                                                                                         |
| Ist-einwertig       | Richtig                                                                                                                          |
| Ist indiziert             | False                                                                                                                         |
| Im globalen Katalog      | False                                                                                                                         |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                  |
| Range-Lower            | \-                                                                                                                            |
| Range-Upper            | \-                                                                                                                            |
| Search-Flags           | 0x00000000                                                                                                                    |
| System-Flags           | 0x00000010                                                                                                                    |
| In verwendete Klassen        | [**Link-Track-OMT-Entry**](c-linktrackomtentry.md)<br/> [**Link-Track-Vol-Entry**](c-linktrackvolentry.md)<br/> |



 

 





