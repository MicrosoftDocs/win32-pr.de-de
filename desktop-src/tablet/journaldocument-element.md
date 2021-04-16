---
description: Das Element der obersten Ebene in einer Journal Notiz-XML-Datei.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: Journaldocument-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 408df14347c130e6b0a73ba869b634ca2493fb56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530170"
---
# <a name="journaldocument-element"></a>Journaldocument-Element

Das Element der obersten Ebene in einer Journal Notiz-XML-Datei.

## <a name="definition"></a>Definition

``` syntax
<xs:element name="JournalDocument">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="Stationery" type="StationeryType" minOccurs="0" maxOccurs="unbounded" />
    <xs:element name="JournalPage" type="JournalPageType" maxOccurs="unbounded" />
   </xs:sequence>
   <xs:attribute name="Version" type="xs:string" use="required" fixed="1.0" />
   <xs:attribute name="DefaultPageWidth" type="xs:nonNegativeInteger" use="required" />
   <xs:attribute name="DefaultPageHeight" type="xs:nonNegativeInteger" use="required" />
  </xs:complexType>
</xs:element>/>
```

## <a name="parent-elements"></a>Übergeordnete Elemente

Keine

## <a name="child-elements"></a>Untergeordnete Elemente

[**Schreib**](stationery-element.md)

[**Journalpage**](journalpage-element.md)

## <a name="attributes"></a>Attribute



| Attribut             | type                      | Erforderlich | BESCHREIBUNG                                                      | Mögliche Werte           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Version**           | **xs:string**             | Erforderlich | Die Version des Journal Dokuments, das in der XML-Datei dargestellt wird. | 1.0                       |
| **DefaultPageWidth**  | **xs:nonNegativeInteger** | Erforderlich | Die Standardbreite der Seite für das Journal Dokument.          | Eine beliebige nicht negative ganze Zahl. |
| **Defaultpageheight** | **xs:nonNegativeInteger** | Erforderlich | Die Standardhöhe der Seite für das Journal Dokument.         | Eine beliebige nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|              |                                            |
|--------------|--------------------------------------------|
| Elementtyp | **Journaldocument**                        |
| Namespace    | urn: Schemas-Microsoft-com: TabletPC: RichInk |
| Schemaname  | Journal Leser                             |



 

 

 



