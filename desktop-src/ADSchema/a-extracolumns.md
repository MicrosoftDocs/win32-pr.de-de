---
title: Extra-Columns-Attribut
description: Dies ist ein mehrwertiges Attribut, dessen Werte aus einem 5-Tupel (Attributname), (Spaltentitel), (Standardsichtbarkeit (0,1)), (Spaltenbreite ( \ 8211;1 für automatische Breite)) und 0 (für die zukünftige Verwendung reserviert) 0 (null) bestehen.
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- Extra-Columns AD-Schema
- ad-Schema des extraColumns-Attributs
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6314a18ecac01a306c72d5879d191c5a744c20171495a3d57192078202d129f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118177182"
---
# <a name="extra-columns-attribute"></a>Extra-Columns-Attribut

Dies ist ein mehrwertiges Attribut, dessen Werte aus einem 5-Tupel bestehen: (Attributname), (Spaltentitel), (Standardsichtbarkeit (0,1)), (Spaltenbreite ( 1 für automatische Breite)), 0 (für die zukünftige Verwendung muss 0 (null) reserviert sein). Dieser Wert wird von der AD-Konsole Benutzer und Computer verwendet.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Extra-Columns                                                                                                                                                        |
| Ldap-Anzeigename | extraColumns                                                                                                                                                         |
| Size              | Jeder Wert wäre die Größe der Zeichenfolge des obigen 5-Tupels. Standardmäßig gibt es 22 Werte für das Default-Display-Objekt im DisplaySpecifier-Container. |
| Aktualisieren von Berechtigungen  | Domänenadministrator                                                                                                                                                 |
| Updatehäufigkeit  | Dies wird nur aktualisiert, wenn ein Dienst wie Exchange installiert ist.                                                                                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1687                                                                                                                                              |
| System-Id-Guid    | d24e2846-1dd9-4bcf-99d7-a6227cc86da7                                                                                                                                 |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------|
| Link-ID                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falsch                                                      |
| Is-Single-Valued       | Falsch                                                      |
| Ist indiziert             | Falsch                                                      |
| Im globalen Katalog      | Falsch                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| In verwendete Klassen        | [**Anzeigespezifizierer**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------|
| Link-ID                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falsch                                                      |
| Is-Single-Valued       | Falsch                                                      |
| Ist indiziert             | Falsch                                                      |
| Im globalen Katalog      | Falsch                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| In verwendete Klassen        | [**Anzeigespezifizierer**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------|
| Link-ID                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falsch                                                      |
| Is-Single-Valued       | Falsch                                                      |
| Ist indiziert             | Falsch                                                      |
| Im globalen Katalog      | Falsch                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| In verwendete Klassen        | [**Anzeigespezifizierer**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------|
| Link-ID                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falsch                                                      |
| Is-Single-Valued       | Falsch                                                      |
| Ist indiziert             | Falsch                                                      |
| Im globalen Katalog      | Falsch                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| In verwendete Klassen        | [**Anzeigespezifizierer**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------|
| Link-ID                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | Falsch                                                      |
| Is-Single-Valued       | Falsch                                                      |
| Ist indiziert             | Falsch                                                      |
| Im globalen Katalog      | Falsch                                                      |
| NT-Security-Descriptor | O:BAG:BAD:S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| In verwendete Klassen        | [**Anzeigespezifizierer**](c-displayspecifier.md)<br/> |



 

 





