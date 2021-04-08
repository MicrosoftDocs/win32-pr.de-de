---
title: ms-DS-zusätzliches-DNS-Host-Name-Attribut
description: Das-Attribut wird verwendet, um den zusätzlichen DNS-Hostnamen eines Computer Objekts zu speichern. Dieses Attribut wird verwendet, wenn ein DC umbenannt wird.
ms.assetid: ea06f756-d9b6-409d-a008-0e3a1874ad94
ms.tgt_platform: multiple
keywords:
- AD-Schema für ms-DS-additional-DNS-Host-Name-Attribut
- AD-Schema für das msDS-additionaldnshostname-Attribut
topic_type:
- apiref
api_name:
- ms-DS-Additional-Dns-Host-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dea3212a19bf743e608f356170adf7a03c06d0
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103957523"
---
# <a name="ms-ds-additional-dns-host-name-attribute"></a>ms-DS-zusätzliches-DNS-Host-Name-Attribut

Das-Attribut wird verwendet, um den zusätzlichen DNS-Hostnamen eines Computer Objekts zu speichern. Dieses Attribut wird zum Zeitpunkt der Umbenennung eines Computers verwendet, oder die Namen werden mit "Netdom Computername" verwaltet.



| Eingabe | Wert |
|-------------------|-----------------------------------------------------------------------------|
| CN                | ms-DS-Zusatz-DNS-Hostname                                              |
| LDAP-Display-Name | MSDS-additionaldnshostname                                                  |
| Size              | Jeder Wert kann 2048 Zeichen umfassen. Die Anzahl von Werten ist das Daten Bank Limit von ungefähr 1200 Werten. |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.                                            |
| Aktualisierungshäufigkeit  | Wenn ein Computer umbenannt wird.                                                 |
| Attribute-Id      | 1.2.840.113556.1.4.1717                                                     |
| System-ID-GUID    | 80863791-dbe9-4eb8-837e-7F 0ab55d9ac7                                        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                 |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|-------------------------------------------|
| Link-ID                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Richtig                                      |
| Ist-einwertig       | False                                     |
| Ist indiziert             | False                                     |
| Im globalen Katalog      | False                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------|
| Link-ID                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Richtig                                      |
| Ist-einwertig       | False                                     |
| Ist indiziert             | False                                     |
| Im globalen Katalog      | False                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|-------------------------------------------|
| Link-ID                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Richtig                                      |
| Ist-einwertig       | False                                     |
| Ist indiziert             | False                                     |
| Im globalen Katalog      | False                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|-------------------------------------------|
| Link-ID                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Richtig                                      |
| Ist-einwertig       | False                                     |
| Ist indiziert             | False                                     |
| Im globalen Katalog      | False                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|-------------------------------------------|
| Link-ID                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | Richtig                                      |
| Ist-einwertig       | False                                     |
| Ist indiziert             | False                                     |
| Im globalen Katalog      | False                                     |
| NT-Security-Descriptor | o:Bag: schlecht: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 2048                                      |
| Search-Flags           | 0x00000000                                |
| System-Flags           | 0x00000010                                |
| In verwendete Klassen        | [**Computer**](c-computer.md)<br/> |



 

 





