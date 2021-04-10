---
title: Repl-Interval-Attribut
description: Das-Attribut von Site-Link-Objekten, das das Intervall in Minuten zwischen den Replikations Zyklen zwischen den Standorten in der Site Liste definiert.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- AD-Schema für Repl-Interval-Attribut
- replInterval-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e681b01fbc60b775b0cb947007056dc1d3d3adbb
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "104107589"
---
# <a name="repl-interval-attribute"></a>Repl-Interval-Attribut

Das-Attribut von Site-Link-Objekten, das das Intervall in Minuten zwischen den Replikations Zyklen zwischen den Standorten in der Site Liste definiert. Muss ein Vielfaches von 15 Minuten (die Granularität der standortübergreifenden DS-Replikation), mindestens 15 Minuten und maximal 10.080 Minuten (eine Woche) sein.



| Eingabe | Wert |
|-------------------|------------------------------------------------|
| CN                | Repl-Interval                                  |
| LDAP-Display-Name | replInterval                                   |
| Size              | 4 Bytes                                        |
| Berechtigung aktualisieren  | Unternehmensadministrator                       |
| Aktualisierungshäufigkeit  | Wann das Replikations Intervall geändert werden muss. |
| Attribute-Id      | 1.2.840.113556.1.4.1336                        |
| System-ID-GUID    | 45ba9d1a-56fa-11d2-90d0-00c04f d91ab1           |
| Syntax            | [**Enumeration**](s-enumeration.md)           |



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
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                       |
| Ist indiziert             | False                                                                                                      |
| Im globalen Katalog      | False                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                       |
| Ist indiziert             | False                                                                                                      |
| Im globalen Katalog      | False                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                       |
| Ist indiziert             | False                                                                                                      |
| Im globalen Katalog      | False                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                       |
| Ist indiziert             | False                                                                                                      |
| Im globalen Katalog      | False                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                       |
| Ist indiziert             | False                                                                                                      |
| Im globalen Katalog      | False                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                       |
| Ist indiziert             | False                                                                                                      |
| Im globalen Katalog      | False                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | False                                                                                                      |
| Ist-einwertig       | Richtig                                                                                                       |
| Ist indiziert             | False                                                                                                      |
| Im globalen Katalog      | False                                                                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standort übergreifender Transport**](c-intersitetransport.md)<br/> [**Standort Link**](c-sitelink.md)<br/> |



 

 





