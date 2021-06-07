---
description: Das Element der obersten Ebene in einer XML-Datei mit Journalnotizen.
ms.assetid: 3887667c-67a7-416a-b94d-c30bb02a7985
title: JournalDocument-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7820ef68dc87bf42d9580c800e2e165f2f2859a4
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432172"
---
# <a name="journaldocument-element"></a>JournalDocument-Element

Das Element der obersten Ebene in einer XML-Datei mit Journalnotizen.

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

[**Briefpapier**](stationery-element.md)

[**JournalPage**](journalpage-element.md)

## <a name="attributes"></a>Attribute



| attribute             | Typ                      | Erforderlich | BESCHREIBUNG                                                      | Mögliche Werte           |
|-----------------------|---------------------------|----------|------------------------------------------------------------------|---------------------------|
| **Version**           | **xs:string**             | Erforderlich | Die Version des Journaldokuments, das in der XML-Datei dargestellt wird. | 1.0                       |
| **DefaultPageWidth**  | **xs:nonNegativeInteger** | Erforderlich | Die Standardbreite der Seite für das Journaldokument.          | Eine nicht negative ganze Zahl. |
| **DefaultPageHeight** | **xs:nonNegativeInteger** | Erforderlich | Die Standardhöhe der Seite für das Journaldokument.         | Eine nicht negative ganze Zahl. |



 

## <a name="element-information"></a>Elementinformationen



|  Element     | Wert                                                     |
|--------------|--------------------------------------------|
| Elementtyp | **JournalDocument**                        |
| Namespace    | urn:schemas-microsoft-com:tabletpc:richink |
| Schemaname  | Journalreader                             |



 

 

 



