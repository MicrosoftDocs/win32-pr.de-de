---
description: Enthält die Details zu einer einzelnen Seite in einer Journal Notiz.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: Journalpage-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7223818de8200f2ff7748edd7eb472f49e92e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866775"
---
# <a name="journalpage-element"></a>Journalpage-Element

Enthält die Details zu einer einzelnen Seite in einer Journal Notiz.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**Journaldocument**](journaldocument-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**Stationär**](stationery-element.md)

[**Docimage**](docimage-element.md)

[**Titleinfo**](titleinfo-element.md)

[**Inhalt**](content-element--journal-reader.md)

## <a name="attributes"></a>Attribute



| Attribut      | type                      | Erforderlich | BESCHREIBUNG                                                                        | Mögliche Werte                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Number**     | **xs:nonNegativeInteger** | Erforderlich | Die Ordinalzahl der Seite im Journal Dokument, beginnend mit eins (1). | Eine beliebige nicht negative ganze Zahl.                                |
| **Width**      | **xs:nonNegativeInteger** | Erforderlich | Die Breite der Seite.                                                             | Eine beliebige nicht negative ganze Zahl.                                |
| **Height**     | **xs:nonNegativeInteger** | Erforderlich | Die Höhe der Seite.                                                            | Eine beliebige nicht negative ganze Zahl.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Optional | Die Höhe der auf der Seite verwendeten Zeile.                                           | Eine beliebige nicht negative ganze Zahl.                                |
| **LanguageID** | **xs:nonNegativeInteger** | Optional | Die Sprach-ID, die für die Seite verwendet wird.                                                 | Eine nicht negative ganze Zahl, die eine gültige Sprach-ID darstellt. |



 

## <a name="element-information"></a>Elementinformationen



|              |                                                                     |
|--------------|---------------------------------------------------------------------|
| Elementtyp | ComplexType für [**journalpagetype**](journalpagetype-complex-type.md) |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk                          |
| Schemaname  | Journal Leser                                                      |



 

 

 



