---
title: Location-Attribut
description: Der Standort des Benutzers, z. B. die Büronummer.
ms.assetid: 3ee97a61-6dce-4f41-b03a-a475706f3cbd
ms.tgt_platform: multiple
keywords:
- Ad-Schema des Speicherortattributs
- LOCATION-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Location
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7e8080ffa24c9b2a147e6e3ec76f586a92fba3456aa1f80d2875c1292940232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705770"
---
# <a name="location-attribute-ad-schema"></a>Location-Attribut (AD-Schema)

Der Standort des Benutzers, z. B. die Büronummer.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Standort                                    |
| Ldap-Anzeigename | location                                    |
| Size              | \-                                          |
| Aktualisieren von Berechtigungen  | \-                                          |
| Updatehäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.222                      |
| System-ID-GUID    | 09dcb79f-165f-11d0-a064-00aa006c33ed        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                               |
| System-Only            | Falsch                                                                                                                                                            |
| Ist einwertig       | Richtig                                                                                                                                                             |
| Ist indiziert             | Richtig                                                                                                                                                             |
| Im globalen Katalog      | Richtig                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                |
| Range-Upper            | 1024                                                                                                                                                             |
| Search-Flags           | 0x00000001                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                       |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druckwarteschlange**](c-printqueue.md)<br/> [**Website**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falsch                                                                                                                                                                                              |
| Ist einwertig       | Richtig                                                                                                                                                                                               |
| Ist indiziert             | Richtig                                                                                                                                                                                               |
| Im globalen Katalog      | Richtig                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druckwarteschlange**](c-printqueue.md)<br/> [**Zimmer**](c-room.md)<br/> [**Website**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|-------------------------------------------------------------------------|
| Link-ID                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falsch                                                                   |
| Ist einwertig       | Richtig                                                                    |
| Ist indiziert             | Richtig                                                                    |
| Im globalen Katalog      | Richtig                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                            |
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
| System-Only            | Falsch                                                                                                                                                                                              |
| Is-Single-Valued       | Richtig                                                                                                                                                                                               |
| Ist indiziert             | Richtig                                                                                                                                                                                               |
| Im globalen Katalog      | Richtig                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druckwarteschlange**](c-printqueue.md)<br/> [**Zimmer**](c-room.md)<br/> [**Website**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falsch                                                                                                                                                                                              |
| Is-Single-Valued       | Richtig                                                                                                                                                                                               |
| Ist indiziert             | Richtig                                                                                                                                                                                               |
| Im globalen Katalog      | Richtig                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druckwarteschlange**](c-printqueue.md)<br/> [**Zimmer**](c-room.md)<br/> [**Website**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falsch                                                                                                                                                                                              |
| Is-Single-Valued       | Richtig                                                                                                                                                                                               |
| Ist indiziert             | Richtig                                                                                                                                                                                               |
| Im globalen Katalog      | Richtig                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druckwarteschlange**](c-printqueue.md)<br/> [**Zimmer**](c-room.md)<br/> [**Website**](c-site.md)<br/> [**Subnet**](c-subnet.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                                                                                                                 |
| MAPI-Id                | \-                                                                                                                                                                                                 |
| System-Only            | Falsch                                                                                                                                                                                              |
| Is-Single-Valued       | Richtig                                                                                                                                                                                               |
| Ist indiziert             | Richtig                                                                                                                                                                                               |
| Im globalen Katalog      | Richtig                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                               |
| Search-Flags           | 0x00000001                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                         |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> [**Druckwarteschlange**](c-printqueue.md)<br/> [**Zimmer**](c-room.md)<br/> [**Website**](c-site.md)<br/> [**Subnetz**](c-subnet.md)<br/> |



 

 





