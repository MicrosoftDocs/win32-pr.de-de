---
title: Extra-Columns-Attribut
description: Dabei handelt es sich um ein mehr wertiges Attribut, dessen Werte aus einem 5 Tupel (Attribut Name), (Spaltentitel), (Standard Sichtbarkeit (0,0)), (Spaltenbreite (\ 8211; 1 für automatische Breite)), 0 (für die zukünftige Verwendung reserviert sein muss), 0 (null) ist.
ms.assetid: aafe4657-0295-4af2-a7d0-8c7561516e17
ms.tgt_platform: multiple
keywords:
- AD-Schema für Extra-Columns-Attribut
- extraColumns-Attribut, AD-Schema
topic_type:
- apiref
api_name:
- Extra-Columns
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0bc74532296c5e0f23da9635bb26df299ae60b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744377"
---
# <a name="extra-columns-attribute"></a>Extra-Columns-Attribut

Dabei handelt es sich um ein mehr wertiges Attribut, dessen Werte aus einem fünf Tupel bestehen: (Attribut Name), (Spaltentitel), (Standard Sichtbarkeit (0,0)), (Spaltenbreite (1 für automatische Breite)), 0 (für die zukünftige Verwendung reserviert muss NULL sein). Dieser Wert wird von der Konsole AD-Benutzer und-Computer verwendet.



| Eingabe | Wert |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CN                | Extra-Columns                                                                                                                                                        |
| LDAP-Display-Name | extraColumns                                                                                                                                                         |
| Size              | Jeder Wert wäre die Größe der Zeichenfolge des 5 Tupels oben. Standardmäßig sind 22 Werte im Display specifier-Container für das default-Display-Objekt vorhanden. |
| Berechtigung aktualisieren  | Domänen Administrator                                                                                                                                                 |
| Aktualisierungshäufigkeit  | Dies wird nur aktualisiert, wenn ein Dienst wie Exchange installiert ist.                                                                                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1687                                                                                                                                              |
| System-ID-GUID    | d24e2846-1dd9-4bcf-99d7-a6227cc86da7                                                                                                                                 |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                                                                                          |



## <a name="implementations"></a>Implementierungen

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Eingabe | Wert |
|------------------------|------------------------------------------------------------|
| Link-ID                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | False                                                      |
| Ist-einwertig       | False                                                      |
| Ist indiziert             | False                                                      |
| Im globalen Katalog      | False                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| In verwendete Klassen        | [**Anzeige-Spezifizierer**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------|
| Link-ID                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | False                                                      |
| Ist-einwertig       | False                                                      |
| Ist indiziert             | False                                                      |
| Im globalen Katalog      | False                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| In verwendete Klassen        | [**Anzeige-Spezifizierer**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Eingabe | Wert |
|------------------------|------------------------------------------------------------|
| Link-ID                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | False                                                      |
| Ist-einwertig       | False                                                      |
| Ist indiziert             | False                                                      |
| Im globalen Katalog      | False                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| In verwendete Klassen        | [**Anzeige-Spezifizierer**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Eingabe | Wert |
|------------------------|------------------------------------------------------------|
| Link-ID                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | False                                                      |
| Ist-einwertig       | False                                                      |
| Ist indiziert             | False                                                      |
| Im globalen Katalog      | False                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| In verwendete Klassen        | [**Anzeige-Spezifizierer**](c-displayspecifier.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Eingabe | Wert |
|------------------------|------------------------------------------------------------|
| Link-ID                | \-                                                         |
| MAPI-Id                | \-                                                         |
| System-Only            | False                                                      |
| Ist-einwertig       | False                                                      |
| Ist indiziert             | False                                                      |
| Im globalen Katalog      | False                                                      |
| NT-Security-Descriptor | o:Bag: schlecht: S:                                               |
| Range-Lower            | \-                                                         |
| Range-Upper            | \-                                                         |
| Search-Flags           | 0x00000000                                                 |
| System-Flags           | 0x00000010                                                 |
| In verwendete Klassen        | [**Anzeige-Spezifizierer**](c-displayspecifier.md)<br/> |



 

 





