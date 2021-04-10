---
title: Location-Attribut
description: Der Speicherort des Benutzers, z. b. Office-Nummer.
ms.assetid: 3ee97a61-6dce-4f41-b03a-a475706f3cbd
ms.tgt_platform: multiple
keywords:
- AD-Schema für Location-Attribut
- AD-Schema für Location-Attribut
topic_type:
- apiref
api_name:
- Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a37f15e80d470c0662036745f285aea87e79391
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104122587"
---
# <a name="location-attribute-ad-schema"></a>Location-Attribut (AD-Schema)

Der Speicherort des Benutzers, z. b. Office-Nummer.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Standort                                    |
| LDAP-Display-Name | location                                    |
| Size              | \-                                          |
| Berechtigung aktualisieren  | \-                                          |
| Aktualisierungshäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.222                      |
| System-ID-GUID    | 09dcb79f -165B-11D0-A064-00aa006c33ed        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                               |
| System-Only            | False                                                                                                                                                            |
| Ist-einwertig       | Richtig                                                                                                                                                             |
| Ist indiziert             | Richtig                                                                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                                                                             |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                |
| Range-Upper            | 1024                                                                                                                                                             |
| Search-Flags           | 0x00000001                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                       |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Website**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | False                                                                                                                                                                                              |
| Ist-einwertig       | Richtig                                                                                                                                                                                               |
| Ist indiziert             | Richtig                                                                                                                                                                                               |
| Im globalen Katalog      | Richtig                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Versand**](c-room.md)<br/> [**Website**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------|
| Link-ID                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | False                                                                   |
| Ist-einwertig       | Richtig                                                                    |
| Ist indiziert             | Richtig                                                                    |
| Im globalen Katalog      | Richtig                                                                    |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                            |
| Range-Lower            | 0                                                                       |
| Range-Upper            | 1024                                                                    |
| Search-Flags           | 0x00000001                                                              |
| System-Flags           | 0x00000010                                                              |
| In verwendete Klassen        | [**Website**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | False                                                                                                                                                                                              |
| Ist-einwertig       | Richtig                                                                                                                                                                                               |
| Ist indiziert             | Richtig                                                                                                                                                                                               |
| Im globalen Katalog      | Richtig                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Versand**](c-room.md)<br/> [**Website**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | False                                                                                                                                                                                              |
| Ist-einwertig       | Richtig                                                                                                                                                                                               |
| Ist indiziert             | Richtig                                                                                                                                                                                               |
| Im globalen Katalog      | Richtig                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Versand**](c-room.md)<br/> [**Website**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | False                                                                                                                                                                                              |
| Ist-einwertig       | Richtig                                                                                                                                                                                               |
| Ist indiziert             | Richtig                                                                                                                                                                                               |
| Im globalen Katalog      | Richtig                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Versand**](c-room.md)<br/> [**Website**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | False                                                                                                                                                                                              |
| Ist-einwertig       | Richtig                                                                                                                                                                                               |
| Ist indiziert             | Richtig                                                                                                                                                                                               |
| Im globalen Katalog      | Richtig                                                                                                                                                                                               |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druck Warteschlange**](c-printqueue.md)<br/> [**Versand**](c-room.md)<br/> [**Website**](c-site.md)<br/> [**Subnetz**](c-subnet.md)<br/> |



 

 





