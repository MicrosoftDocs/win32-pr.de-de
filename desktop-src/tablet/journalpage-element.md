---
description: Enthält die Details zu einer einzelnen Seite in einer Journalnotiz.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: JournalPage-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0939194585b067525fa841d6d41674180a40adb9
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432142"
---
# <a name="journalpage-element"></a>JournalPage-Element

Enthält die Details zu einer einzelnen Seite in einer Journalnotiz.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a>Übergeordnete Elemente

[**JournalDocument**](journaldocument-element.md)

## <a name="child-elements"></a>Untergeordnete Elemente

[**Stationär**](stationery-element.md)

[**DocImage**](docimage-element.md)

[**TitleInfo**](titleinfo-element.md)

[**Inhalt**](content-element--journal-reader.md)

## <a name="attributes"></a>Attribute



| attribute      | Typ                      | Erforderlich | BESCHREIBUNG                                                                        | Mögliche Werte                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Number**     | **xs:nonNegativeInteger** | Erforderlich | Die Ordnungszahl der Seite im Journaldokument, beginnend mit 1 (1). | Eine beliebige nicht negative ganze Zahl.                                |
| **Width**      | **xs:nonNegativeInteger** | Erforderlich | Die Breite der Seite.                                                             | Eine beliebige nicht negative ganze Zahl.                                |
| **Height**     | **xs:nonNegativeInteger** | Erforderlich | Die Höhe der Seite.                                                            | Eine beliebige nicht negative ganze Zahl.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Optional | Die Höhe der auf der Seite verwendeten Linie.                                           | Eine beliebige nicht negative ganze Zahl.                                |
| **Languageid** | **xs:nonNegativeInteger** | Optional | Die sprach-ID, die für die Seite verwendet wird.                                                 | Eine nicht negative ganze Zahl, die eine gültige Sprach-ID darstellt. |



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|---------------------------------------------------------------------|
| Elementtyp | [**complexType: JournalPageType**](journalpagetype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                          |
| Schemaname  | Journalreader                                                      |



 

 

 



