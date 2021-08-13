---
description: Enthält die Details zu einer einzelnen Seite in einer Journalnotiz.
ms.assetid: 8cada667-188b-42f9-8602-34e23d512b82
title: JournalPage-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5062838476e6f67605101157640a490645e454b62d852b69f51dc4bb2215db99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442800"
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



| attribute      | Typ                      | Erforderlich | Beschreibung                                                                        | Mögliche Werte                                          |
|----------------|---------------------------|----------|------------------------------------------------------------------------------------|----------------------------------------------------------|
| **Number**     | **xs:nonNegativeInteger** | Erforderlich | Die Ordnungszahl der Seite im Journaldokument, beginnend mit einem (1). | Eine nicht negative ganze Zahl.                                |
| **Width**      | **xs:nonNegativeInteger** | Erforderlich | Die Breite der Seite.                                                             | Eine nicht negative ganze Zahl.                                |
| **Height**     | **xs:nonNegativeInteger** | Erforderlich | Die Höhe der Seite.                                                            | Eine nicht negative ganze Zahl.                                |
| **LineHeight** | **xs:nonNegativeInteger** | Optional | Die Höhe der auf der Seite verwendeten Zeile.                                           | Eine nicht negative ganze Zahl.                                |
| **Languageid** | **xs:nonNegativeInteger** | Optional | Die für die Seite verwendete Sprach-ID.                                                 | Eine nicht negative ganze Zahl, die eine gültige Sprach-ID darstellt. |



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|---------------------------------------------------------------------|
| Elementtyp | [**complexType: JournalPageType**](journalpagetype-complex-type.md) |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink                          |
| Schemaname  | Journalreader                                                      |



 

 

 



