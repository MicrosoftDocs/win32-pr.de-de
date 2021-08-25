---
title: Revisionsattribut
description: Die Revisionsebene für einen Sicherheitsdeskriptor oder eine andere Änderung. Wird nur in den Objekten sam-server und ds-ui-settings verwendet.
ms.assetid: 480de80f-3e76-4a62-a4a7-29a67f910a62
ms.tgt_platform: multiple
keywords:
- Revisionsattribut AD-Schema
- Revisionattribut AD-Schema
topic_type:
- apiref
api_name:
- Revision
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 655b947e0d2420ba731329dc09104d9a6da19342de41408c06173aecdb4f3737
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119837390"
---
# <a name="revision-attribute"></a>Revisionsattribut

Die Revisionsebene für einen Sicherheitsdeskriptor oder eine andere Änderung. Wird nur in den Objekten sam-server und ds-ui-settings verwendet.



| Eingabe | Wert |
|-------------------|--------------------------------------|
| CN                | Revision                             |
| Ldap-Anzeigename | revision                             |
| Size              | 4 Bytes                              |
| Aktualisieren von Berechtigungen  | Dieser Wert wird vom System festgelegt.     |
| Updatehäufigkeit  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.145               |
| System-Id-Guid    | bf967a21-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Enumeration**](s-enumeration.md) |



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
|------------------------|---------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falsch                                                                                 |
| Is-Single-Valued       | Richtig                                                                                  |
| Ist indiziert             | Falsch                                                                                 |
| Im globalen Katalog      | Falsch                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falsch                                                                                 |
| Is-Single-Valued       | Richtig                                                                                  |
| Ist indiziert             | Falsch                                                                                 |
| Im globalen Katalog      | Falsch                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Eingabe | Wert |
|------------------------|---------------------------------|
| Link-ID                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falsch                           |
| Is-Single-Valued       | Richtig                            |
| Ist indiziert             | Falsch                           |
| Im globalen Katalog      | Falsch                           |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| In verwendete Klassen        | [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falsch                                                                                 |
| Is-Single-Valued       | Richtig                                                                                  |
| Ist indiziert             | Falsch                                                                                 |
| Im globalen Katalog      | Falsch                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falsch                                                                                 |
| Is-Single-Valued       | Richtig                                                                                  |
| Ist indiziert             | Falsch                                                                                 |
| Im globalen Katalog      | Falsch                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falsch                                                                                 |
| Is-Single-Valued       | Richtig                                                                                  |
| Ist indiziert             | Falsch                                                                                 |
| Im globalen Katalog      | Falsch                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Nach oben**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|---------------------------------------------------------------------------------------|
| Link-ID                | \-                                                                                    |
| MAPI-Id                | \-                                                                                    |
| System-Only            | Falsch                                                                                 |
| Is-Single-Valued       | Richtig                                                                                  |
| Ist indiziert             | Falsch                                                                                 |
| Im globalen Katalog      | Falsch                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                          |
| Range-Lower            | \-                                                                                    |
| Range-Upper            | \-                                                                                    |
| Search-Flags           | 0x00000000                                                                            |
| System-Flags           | 0x00000010                                                                            |
| In verwendete Klassen        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> [**Nach oben**](c-top.md)<br/> |



 

 





