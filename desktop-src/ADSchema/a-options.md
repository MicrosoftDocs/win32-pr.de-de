---
title: Options-Attribut
description: Ein Bitfeld, bei dem die Bedeutung der Bits von objectClass zu objectClass abweicht. Kann auf standortübergreifenden Transport-, NTDS-Connection-, NTDS-DSA-, NTDS-Site-Settings-und Site-Link-Objekten auftreten.
ms.assetid: 07495cc1-1db0-4e0d-afbe-b21d2b50b6a1
ms.tgt_platform: multiple
keywords:
- Options Attribut AD-Schema
- options Attribut AD-Schema
topic_type:
- apiref
api_name:
- Options
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cdd970a805816e941c9eb017bf6b96302eef2b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479991"
---
# <a name="options-attribute"></a>Options-Attribut

Ein Bitfeld, bei dem die Bedeutung der Bits von objectClass zu objectClass abweicht. Kann auf standortübergreifenden Transport-, NTDS-Connection-, NTDS-DSA-, NTDS-Site-Settings-und Site-Link-Objekten auftreten.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Optionen                              |
| LDAP-Display-Name | Optionen                              |
| Size              | 4 Bytes                              |
| Berechtigung aktualisieren  | \-                                   |
| Aktualisierungshäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.307               |
| System-ID-GUID    | 19195a53-6da0-11D0-afd3-00c04f 930c9 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                  |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                  |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                  |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                  |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                  |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                  |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                                                                                     |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                     |
| System-Only            | False                                                                                                                                                                                                                                                                  |
| Ist-einwertig       | Richtig                                                                                                                                                                                                                                                                   |
| Ist indiziert             | False                                                                                                                                                                                                                                                                  |
| Im globalen Katalog      | False                                                                                                                                                                                                                                                                  |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                                                                                           |
| Range-Lower            | \-                                                                                                                                                                                                                                                                     |
| Range-Upper            | \-                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                             |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                             |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**NTDS-Verbindung**](c-ntdsconnection.md)<br/> [**NTDS-DSA**](c-ntdsdsa.md)<br/> [**NTDS-Site-Settings**](c-ntdssitesettings.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



 

 





