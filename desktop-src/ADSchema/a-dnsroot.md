---
title: Dns-Root-Attribut
description: Der oberste DNS-Domänen Name, der einer Domäne/Verzeichnis Partition zugewiesen ist.
ms.assetid: 0b33daad-b5c5-4126-86fa-abd3e0006c5f
ms.tgt_platform: multiple
keywords:
- AD-Schema für Dns-Root-Attribut
- dnsRoot-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Dns-Root
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2c2fd2c39e8f0015d7641eccd27279b3478ec4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "106344525"
---
# <a name="dns-root-attribute"></a>Dns-Root-Attribut

Der oberste DNS-Domänen Name, der einer Domäne/Verzeichnis Partition zugewiesen ist. Dies wird für ein CrossRef-Objekt festgelegt und wird unter anderem für die Verweis Generierung verwendet. Beim Durchsuchen einer gesamten Domänen Struktur muss die Suche beim Dns-Root-Objekt initiiert werden. Dieses Attribut kann mehr wertig sein. in diesem Fall werden mehrere Verweise generiert.



| Eingabe | Wert |
|-------------------|---------------------------------------------|
| CN                | Dns-Root                                    |
| LDAP-Display-Name | dnsRoot                                     |
| Size              | \-                                          |
| Berechtigung aktualisieren  | Dieser Wert wird vom System festgelegt.            |
| Aktualisierungshäufigkeit  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.28                       |
| System-ID-GUID    | bf967959-0de6-11d0-a285-00aa003049e2        |
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
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Ist-einwertig       | False                                      |
| Ist indiziert             | Richtig                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Ist-einwertig       | False                                      |
| Ist indiziert             | Richtig                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Ist-einwertig       | False                                      |
| Ist indiziert             | Richtig                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Ist-einwertig       | False                                      |
| Ist indiziert             | Richtig                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Ist-einwertig       | False                                      |
| Ist indiziert             | Richtig                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Ist-einwertig       | False                                      |
| Ist indiziert             | Richtig                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|--------------------------------------------|
| Link-ID                | \-                                         |
| MAPI-Id                | \-                                         |
| System-Only            | False                                      |
| Ist-einwertig       | False                                      |
| Ist indiziert             | Richtig                                       |
| Im globalen Katalog      | False                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                               |
| Range-Lower            | 1                                          |
| Range-Upper            | 255                                        |
| Search-Flags           | 0x00000001                                 |
| System-Flags           | 0x00000010                                 |
| In verwendete Klassen        | [**Kreuz Verweis**](c-crossref.md)<br/> |



 

 





