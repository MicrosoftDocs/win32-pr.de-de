---
description: Weist Enumerationstext einem Wertebereich zu. Jedes enumrange-Element gibt einen Minimalwert an und erstreckt sich bis zum nächsten Element Minimalwert oder bis keine weiteren enumrange-Elemente vorhanden sind.
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumbereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959359"
---
# <a name="enumrange"></a>enumbereich

Weist Enumerationstext einem Wertebereich zu. Jedes [enumrange]() -Element gibt einen Minimalwert an und erstreckt sich bis zum nächsten Element Minimalwert oder bis keine weiteren enumrange-Elemente vorhanden sind.

## <a name="syntax"></a>Syntax

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                         | Untergeordnete Elemente |
|--------------------------------------------------------|----------------|
| [enumeratedlist](./propdesc-schema-enumeratedlist.md) | none           |



 

## <a name="attributes"></a>Attribute



| Attribut | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| minValue  | Öffentlich. Erforderlich. Der Minimalwert im Bereich.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| setValue  | Öffentlich. Dies ist optional. Wenn ein Benutzer diese Enumeration aus einem ListBox-Eigenschaften Steuerelement auswählt, wird dieser diskrete Wert als Eigenschafts Wert zugewiesen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| text      | Öffentlich. Dies ist optional. Der Text, der verwendet wird, um den Enumerationswert anzuzeigen. Die Syntax ermöglicht eine direkte Anzeige Zeichenfolge oder einen indirekten Verweis auf eine Anzeige Zeichenfolge. Verwenden Sie die indirekte Anzeige Zeichenfolge, damit Sie lokalisiert werden kann.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Zugriffstasten | **Windows 7 und höher.** Öffentlich. Dies ist optional. Eine Liste von mnetmonischen Werten, die verwendet werden können, um auf die Eigenschaft in Such Abfragen zu verweisen. Die Liste wird durch das \| Zeichen "" getrennt.                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| name      | Erforderlich. Der kanonische Eigenschaftsname, der für das System eindeutig ist. Beispiel: System. Rating. Dieses Attribut ist auf 64 Zeichen beschränkt. Beim Namen wird die Groß-/Kleinschreibung beachtet, und es sollte die folgende Syntax verwendet werden: Publisher. Application. PropertyName. Die folgenden Methoden geben diesen Wert zurück: [**IExplorerCommand:: GetCanonicalName**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**ipropertydescription:: GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2:: GetCanonicalName**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)und [**ipropertyui:: GetCanonicalName**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)). |



 

 

 
