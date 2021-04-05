---
description: In diesem Thema wird das Eigenschafts Beschreibungs Schema eingeführt, das vom Shell-Eigenschaften System verwendet wird
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Grundlegendes zum Eigenschafts Beschreibungs Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51d9e7c2b6fb4b599f977c0c49ad1cb2514fe8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042031"
---
# <a name="understanding-the-property-description-schema"></a>Grundlegendes zum Eigenschafts Beschreibungs Schema

In diesem Thema wird das Eigenschafts Beschreibungs Schema eingeführt, das vom Shell-Eigenschaften System verwendet wird

Die Einführung neuer Features für Windows Vista und höher erforderte, dass das vorhandene shelleigenschaftensystem auf Folgendes erweitert werden muss:

-   Unterstützen Sie ein umfassendes und erweiterbares Eigenschafts Beschreibungs System, das Informationen zu Eigenschaften wie anzeigen Amen, Typ, Anzeigetyp, Sortier-und Gruppenverhalten und anderen Attributen bereitstellt, die erforderlich sind, um die Eigenschaften anzuzeigen und zu verarbeiten.
-   Unterstützen Sie eine Bestandsliste von Eigenschafts Typen (in Kombination mit der Benutzeroberfläche, die diese Typen in verschiedenen Ansichten bearbeiten kann, wie z. b. ListView, Vorschaubereich, Eigenschaften Dialogfelder usw.), die verschiedenen Eigenschaften zugeordnet werden können.
-   Geben Sie Eigenschaften Beschreibungs Listen an, die den Satz von Eigenschaften definieren, die in unterschiedlichen Ansichten angezeigt werden.
-   Stellen Sie eine vereinfachte Schnittstelle ( [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) bereit, sodass Eigenschafts Handler einfacher geschrieben werden können, sodass Eigenschaften in Dateien persistent gespeichert werden können.
-   Unterstützung für nicht-Dateieigenschaften Handler, um Eigenschaften in der Ansicht verfügbar zu machen.

Diese Features werden in einer Architektur erzielt, die abstrakten Zugriff auf die Eigenschaften eines shellelements bereitstellt. Diese Abstraktion wird als shelleigenschaftensystem bezeichnet.

-   [Was ist das Eigenschafts Beschreibungs Schema?](#what-is-the-property-description-schema)
-   [Gründe für die Verwendung eines Schemas](#why-use-a-schema)
-   [Was sind die wichtigsten Schema Teile?](#what-are-the-major-schema-parts)
-   [Änderungen für Windows 7](#changes-for-windows-7)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-the-property-description-schema"></a>Was ist das Eigenschafts Beschreibungs Schema?

Das Schema Subsystem besteht aus folgendem:

-   Eine oder mehrere. PropDesc-Schema Dateien, die Eigenschafts Beschreibungen definieren. Das Eigenschafts Beschreibungs Schema wird in einer Auflistung von XML-Schema Dateien (mit der Dateierweiterung ". PropDesc") zur Laufzeit des Systems definiert. Diese Dateien werden verzögert geladen, wenn Sie von einem Teil des Eigenschaften Systems benötigt werden.
-   Ein in-Memory-Schema Cache zum Speichern der analysierten Schema Dateien, die alle Eigenschafts Beschreibungen enthalten, die mit dem Subsystem eingeführt wurden. Es ist nicht erforderlich, die. PropDesc-Konfigurationsdateien zu analysieren, die das Schema beschreiben. Weitere Informationen finden Sie unter [**psregisterpropertyschema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**psunregisterpropertyschema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)und [**psrefreshpropertyschema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).
-   Ein subsystemobjekt, das [**ipropertysystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)implementiert, das verwendet wird, um Eigenschafts Beschreibungen abzurufen oder mit Ihnen zu arbeiten.
-   Ein subsystemobjekt, das [**ipropertydescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)implementiert, das verwendet wird, um basierend auf einer Eigenschafts Beschreibung zu informieren und zu arbeiten.
-   Ein subsystemobjekt, das [**ipropertydescriptionlist**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)implementiert, das als Auflistung von Eigenschafts Beschreibungen verwendet wird.

> [!Note]  
> Sie müssen `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` dem Root-Schema Element ihrer. PropDesc-Dateien hinzufügen.

 

## <a name="why-use-a-schema"></a>Gründe für die Verwendung eines Schemas

Eigenständige Eigenschaften sind nicht typsicher. Eine Komponente kann der System. Author-Eigenschaft einen numerischen Wert oder einen [**Dateizeit**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Datumsstempel der System. Music. albumtitle-Eigenschaft zuweisen. ohne weitere Erzwingung oder Anleitungen wird Sie von den Eigenschaften speichern zugelassen. Wir mussten also einen Begriff "schematisieren", um die Eigenschaften zu "schematisieren", was uns zum Schema Subsystem führt.

## <a name="what-are-the-major-schema-parts"></a>Was sind die wichtigsten Schema Teile?

Das vom shelleigenschafts System verwendete Eigenschafts Beschreibungs Schema besteht aus einem einzelnen [propertydescriptionlist](./propdesc-schema-propertydescriptionlist.md) -Element sowie einem *Schemaversion* -Attribut, das die Version dieses Schema Definitions Formats angibt. Hinweis: der Wert muss "1,0" sein.


```
<!-- schema -->
    <xs:element name="schema">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescriptionList" minOccurs="1" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="schemaVersion"  type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



Die [propertydescriptionlist](./propdesc-schema-propertydescriptionlist.md) besteht aus einem oder mehreren [propertydescription](./propdesc-schema-propertydescription.md) -Elementen sowie aus *Verleger* -und *Produkt* Attributen.


```
<!-- propertyDescriptionList -->
    <xs:element name="propertyDescriptionList">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product"   type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



Eine [propertydescription](./propdesc-schema-propertydescription.md) besteht aus einem [SearchInfo](./propdesc-schema-searchinfo.md) -Element und keinem oder einem " [Labelinfo](./propdesc-schema-labelinfo.md)", einem [TypeInfo](./propdesc-schema-typeinfo.md)-Element und einem [DisplayInfo](./propdesc-schema-displayinfo.md) -Element sowie den Attributen " *FormatID*", " *PROPID*", " *propstr*" und " *Name* ".

Es sollte ein [propertydescription](./propdesc-schema-propertydescription.md) -Element für jeden eindeutigen kanonischen Eigenschaftsnamen vorhanden sein, der im System verfügbar sein soll. Die Zeichen folgen Attribute haben ein Limit von 512 Zeichen. Werte, die länger als 512 Zeichen sind, werden abgeschnitten.


```
<!-- propertyDescription -->
    <xs:element name="propertyDescription">
      <xs:complexType>
        <xs:all>
          <xs:element name="description"    type="xs:string" minOccurs="0" maxOccurs="1"/>
          <xs:element ref="searchInfo"   minOccurs="1" maxOccurs="1"/>
          <xs:element ref="labelInfo"    minOccurs="0" maxOccurs="1"/>
          <xs:element ref="typeInfo"     minOccurs="0" maxOccurs="1"/>
          <xs:element ref="displayInfo"  minOccurs="0" maxOccurs="1"/>
        </xs:all>
        <xs:attribute name="formatID"  type="upcase-uuid" use="required""/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required""/>
        <xs:attribute name="name"      type="canonical-name" use="required"/>
      </xs:complexType>
    </xs:element>
```



## <a name="changes-for-windows-7"></a>Änderungen für Windows 7

Das Eigenschafts Beschreibungs Schema wurde für Windows 7 geändert. Dabei handelt es sich um nicht unterbrechende Änderungen. Wenn ein Eigenschafts Element oder-Attribut in Windows 7 nicht mehr unterstützt wird, ignoriert das Windows 7-Betriebssystem das Windows Vista-Element oder die Windows Vista-Attribute. Ebenso ignoriert Windows Vista auch neue Eigenschaften Elemente oder Attribute von Windows 7.

Es wird jedoch empfohlen, benutzerdefinierte Eigenschaften für Windows 7 zu aktualisieren, um eine bessere und konsistentere Benutzer Leistung zu erzielen.

Im folgenden finden Sie neue Elemente und Attribute:

-   [relatedpropertyinfo](./propdesc-schema-relatedpropertyinfo.md) -und [relatedproperty](./propdesc-schema-relatedproperty.md) -Elemente
-   [Image](./propdesc-schema-image.md) -Element
-   mnetmonics-Attribut des [SearchInfo](./propdesc-schema-searchinfo.md) -Elements
-   mnetmonics-Attribut des [Enumeration](./propdesc-schema-enum.md) -Elements
-   searchrawvalue-Attribut des [Typeingabe Info](./propdesc-schema-typeinfo.md) -Elements

Die folgenden Elemente und Attribute wurden geändert:

-   [enumeratedlist](./propdesc-schema-enumeratedlist.md)-, [Enumeration](./propdesc-schema-enum.md)-und [enumrange](./propdesc-schema-enumrange.md) -Elemente
-   [DrawControl](./propdesc-schema-drawcontrol.md) -Element
-   [editcontrol](./propdesc-schema-editcontrol.md) -Element
-   PROPID-Attribut des [propertydescription](./propdesc-schema-propertydescription.md) -Elements
-   columnindextype-Attribut des [SearchInfo](./propdesc-schema-searchinfo.md) -Elements

Die folgenden Elemente und Attribute wurden entfernt:

-   [querycontrol](./propdesc-schema-querycontrol.md) -Element
-   isquervable-Attribut des [Typeingabe Info](./propdesc-schema-typeinfo.md) -Elements
-   includeinfulltextquery-Attribut des [TypeInfo](./propdesc-schema-typeinfo.md) -Elements

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[propertydescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[SearchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[Labelinfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[TypeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[Display Info](./propdesc-schema-displayinfo.md)
</dt> <dt>

[StringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[BooleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[NumberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedlist](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[DrawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editcontrol](./propdesc-schema-editcontrol.md)
</dt> <dt>

[FilterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[querycontrol](./propdesc-schema-querycontrol.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> </dl>

 

 
