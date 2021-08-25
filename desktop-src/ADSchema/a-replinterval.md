---
title: Repl-Interval-Attribut
description: Das -Attribut Site-Link-Objekten, die das Intervall zwischen Replikationszyklen zwischen den Standorten in der Standortliste in Minuten definieren.
ms.assetid: ef4cbf75-7283-4930-9f98-1ffd6eb05669
ms.tgt_platform: multiple
keywords:
- Repl-Interval AD-Schema
- replInterval-Attribut AD-Schema
topic_type:
- apiref
api_name:
- Repl-Interval
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb5cd02d3458684f6d70cff84435c7809fcd4c912befd65373a264f961cefd72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837440"
---
# <a name="repl-interval-attribute"></a>Repl-Interval-Attribut

Das -Attribut Site-Link-Objekten, die das Intervall zwischen Replikationszyklen zwischen den Standorten in der Standortliste in Minuten definieren. Muss ein Vielfaches von 15 Minuten (die Granularität der standortübergreifenden DS-Replikation), mindestens 15 Minuten und maximal 10.080 Minuten (eine Woche) sein.



| Eingabe | Wert |
|-------------------|------------------------------------------------|
| CN                | Repl-Interval                                  |
| Ldap-Anzeigename | replInterval                                   |
| Size              | 4 Bytes                                        |
| Aktualisieren von Berechtigungen  | Unternehmensadministrator                       |
| Updatehäufigkeit  | Wenn sich das Replikationsintervall ändern muss. |
| Attribute-Id      | 1.2.840.113556.1.4.1336                        |
| System-Id-Guid    | 45ba9d1a-56fa-11d2-90d0-00c04fd91ab1           |
| Syntax            | [**Enumeration**](s-enumeration.md)           |



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
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falsch                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                       |
| Ist indiziert             | Falsch                                                                                                      |
| Im globalen Katalog      | Falsch                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standortübergreifender Transport**](c-intersitetransport.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falsch                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                       |
| Ist indiziert             | Falsch                                                                                                      |
| Im globalen Katalog      | Falsch                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standortübergreifender Transport**](c-intersitetransport.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falsch                                                                                                      |
| Is-Single-Valued       | Richtig                                                                                                       |
| Ist indiziert             | Falsch                                                                                                      |
| Im globalen Katalog      | Falsch                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standortübergreifender Transport**](c-intersitetransport.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falsch                                                                                                      |
| Ist einwertig       | Richtig                                                                                                       |
| Ist indiziert             | Falsch                                                                                                      |
| Im globalen Katalog      | Falsch                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standortübergreifender Transport**](c-intersitetransport.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falsch                                                                                                      |
| Ist einwertig       | Richtig                                                                                                       |
| Ist indiziert             | Falsch                                                                                                      |
| Im globalen Katalog      | Falsch                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standortübergreifender Transport**](c-intersitetransport.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falsch                                                                                                      |
| Ist einwertig       | Richtig                                                                                                       |
| Ist indiziert             | Falsch                                                                                                      |
| Im globalen Katalog      | Falsch                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standortübergreifender Transport**](c-intersitetransport.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                                         |
| MAPI-Id                | \-                                                                                                         |
| System-Only            | Falsch                                                                                                      |
| Ist einwertig       | Richtig                                                                                                       |
| Ist indiziert             | Falsch                                                                                                      |
| Im globalen Katalog      | Falsch                                                                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                               |
| Range-Lower            | \-                                                                                                         |
| Range-Upper            | \-                                                                                                         |
| Search-Flags           | 0x00000000                                                                                                 |
| System-Flags           | 0x00000010                                                                                                 |
| In verwendete Klassen        | [**Standortübergreifender Transport**](c-intersitetransport.md)<br/> [**Site-Link**](c-sitelink.md)<br/> |



 

 





