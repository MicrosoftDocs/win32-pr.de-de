---
description: In diesem Thema wird das Eigenschaftenbeschreibungsschema vorgestellt, das vom Shell-Eigenschaftensystem verwendet wird.
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Grundlegendes zum Eigenschaftenbeschreibungsschema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85dbb0f20c5c4a206069e80aa308a26908bf90ee0d00cf80712a342e834411e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554560"
---
# <a name="understanding-the-property-description-schema"></a>Grundlegendes zum Eigenschaftenbeschreibungsschema

In diesem Thema wird das Eigenschaftenbeschreibungsschema vorgestellt, das vom Shell-Eigenschaftensystem verwendet wird.

Die Einführung neuer Features für Windows Vista und höher erforderte, dass das vorhandene Shell-Eigenschaftensystem auf Folgendes erweitert werden muss:

-   Unterstützt ein umfassendes und erweiterbares Eigenschaftenbeschreibungssystem, das Informationen zu Eigenschaften bereitstellt, einschließlich Anzeigenamen, Typ, Anzeigetyp, Sortier- und Gruppenverhalten sowie andere Attribute, die zum Darstellen und Verwenden der Eigenschaften erforderlich sind.
-   Unterstützt eine Bestandsliste von Eigenschaftstypen (kombiniert mit der Benutzeroberfläche, die diese Typen in verschiedenen Ansichten bearbeiten kann, z. B. listenansicht, Vorschaubereich, Eigenschaftendialoge usw.), die verschiedenen Eigenschaften zugeordnet werden können.
-   Geben Sie Eigenschaftenbeschreibungslisten an, die den Satz von Eigenschaften definieren, die in verschiedenen Ansichten angezeigt werden.
-   Stellen Sie eine vereinfachte Schnittstelle [**(IPropertyStore)**](/windows/win32/api/propsys/nn-propsys-ipropertystore)bereit, damit Eigenschaftenhandler einfacher geschrieben und Eigenschaften in Dateien beibehalten werden können.
-   Unterstützung für Nicht-Dateieigenschaftenhandler, um Eigenschaften in der Ansicht verfügbar zu machen.

Diese Features werden in einer Architektur erreicht, die abstrakten Zugriff auf die Eigenschaften eines Shellelements bietet. Diese Abstraktion wird als Shell-Eigenschaftensystem bezeichnet.

-   [Was ist das Eigenschaftenbeschreibungsschema?](#what-is-the-property-description-schema)
-   [Gründe für die Verwendung eines Schemas](#why-use-a-schema)
-   [Was sind die hauptteiligen Schemateile?](#what-are-the-major-schema-parts)
-   [Änderungen für Windows 7](#changes-for-windows-7)
-   [Zugehörige Themen](#related-topics)

## <a name="what-is-the-property-description-schema"></a>Was ist das Eigenschaftenbeschreibungsschema?

Das Schemasubsystem besteht aus folgendem Code:

-   Eine oder mehrere PROPDESC-Schemadateien, die Eigenschaftenbeschreibungen definieren. Das Eigenschaftenbeschreibungsschema wird zur Laufzeit im System in einer Auflistung von XML-Schemadateien (mit der Dateierweiterung .propdesc) definiert. Diese Dateien werden verzögert geladen, wenn sie für einen Teil des Eigenschaftensystems erforderlich sind.
-   Ein In-Memory-Schemacache, der zum Speichern der analysierten Schemadateien verwendet wird, die alle Eigenschaftenbeschreibungen enthalten, die in das Subsystem eingeführt wurden. Es ist nicht erforderlich, die PROPDESC-Konfigurationsdateien, die das Schema beschreiben, neu zu prüfen. Weitere Informationen finden Sie unter [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)und [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).
-   Ein Subsystemobjekt, das [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)implementiert, das zum Abrufen oder Arbeiten mit Eigenschaftenbeschreibungen verwendet wird.
-   Ein Subsystemobjekt, das [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)implementiert, das verwendet wird, um basierend auf einer Eigenschaftenbeschreibung zu informieren und zu arbeiten.
-   Ein Subsystemobjekt, das [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)implementiert, das als Auflistung von Eigenschaftenbeschreibungen verwendet wird.

> [!Note]  
> Sie müssen `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` dem Stammschemaelement Ihrer PROPDESC-Dateien hinzufügen.

 

## <a name="why-use-a-schema"></a>Gründe für die Verwendung eines Schemas

Eigenschaften selbst sind nicht typsicher. Eine Komponente kann der System.Author-Eigenschaft einen [](/windows/win32/api/minwinbase/ns-minwinbase-filetime) numerischen Wert oder dem System einen FILETIME-Datumsstempel zuweisen. Musik. Die AlbumTitle-Eigenschaft und die Eigenschaftsspeicher lassen sie ohne weitere Erzwingung oder Anleitung zu. Daher mussten wir die Eigenschaften "schematisieren", wodurch wir zum Schemasubsystem gelangen.

## <a name="what-are-the-major-schema-parts"></a>Was sind die Wichtigsten Schemateile?

Das vom Shell-Eigenschaftensystem verwendete Eigenschaftenbeschreibungsschema besteht aus einem einzelnen [propertyDescriptionList-Element](./propdesc-schema-propertydescriptionlist.md) sowie einem *schemaVersion-Attribut,* das die Version dieses Schemadefinitionsformats angibt. Hinweis: Der Wert muss "1.0" sein.


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



[PropertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) besteht aus einem oder mehreren [propertyDescription-Elementen](./propdesc-schema-propertydescription.md) sowie *Herausgeber-* und *Produktattributen.*


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



Eine [propertyDescription](./propdesc-schema-propertydescription.md) besteht aus einem [searchInfo-](./propdesc-schema-searchinfo.md) und einem null- oder [labelInfo-,](./propdesc-schema-labelinfo.md) [typeInfo-](./propdesc-schema-typeinfo.md)und [displayInfo-Element](./propdesc-schema-displayinfo.md) sowie *aus formatID-,* *propID-,* *propstr-* und name-Attributen. 

Es sollte ein [propertyDescription-Element](./propdesc-schema-propertydescription.md) für jeden eindeutigen kanonischen Eigenschaftennamen vorhanden sein, der im System verfügbar sein soll. Die Zeichenfolgenattribute haben einen Grenzwert von 512 Zeichen. Werte, die länger als 512 Zeichen sind, werden abgeschnitten.


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

Das Eigenschaftenbeschreibungsschema wurde für Windows 7 geändert. Dies sind nicht breaking changes. Wenn ein Eigenschaftselement oder Attribut in Windows 7 nicht mehr unterstützt wird, ignoriert das Windows 7-Betriebssystem die Windows Vista-Elemente oder -Attribute. Auf ähnliche Weise ignoriert Windows Vista auch neue Windows 7-Eigenschaftselemente oder -Attribute.

Es wird jedoch empfohlen, benutzerdefinierte Eigenschaften für Windows 7 zu aktualisieren, um eine bessere und konsistentere Benutzererfahrung zu gewährleisten.

Im Folgenden werden neue Elemente und Attribute beschrieben:

-   [relatedPropertyInfo-](./propdesc-schema-relatedpropertyinfo.md) und [relatedProperty-Elemente](./propdesc-schema-relatedproperty.md)
-   [image-Element](./propdesc-schema-image.md)
-   mnemonics-Attribut des [searchInfo-Elements](./propdesc-schema-searchinfo.md)
-   mnemonics-Attribut [](./propdesc-schema-enum.md) des Enumerationselements
-   searchRawValue-Attribut des [typeInfo-Elements](./propdesc-schema-typeinfo.md)

Die folgenden Elemente und Attribute wurden geändert:

-   [enumeratedList-,](./propdesc-schema-enumeratedlist.md) [enum-](./propdesc-schema-enum.md)und [enumRange-Elemente](./propdesc-schema-enumrange.md)
-   [drawControl-Element](./propdesc-schema-drawcontrol.md)
-   [editControl-Element](./propdesc-schema-editcontrol.md)
-   propID-Attribut des [propertyDescription-Elements](./propdesc-schema-propertydescription.md)
-   columnIndexType-Attribut des [searchInfo-Elements](./propdesc-schema-searchinfo.md)

Die folgenden Elemente und Attribute wurden entfernt:

-   [queryControl-Element](./propdesc-schema-querycontrol.md)
-   isQueryable-Attribut des [typeInfo-Elements](./propdesc-schema-typeinfo.md)
-   includeInFullTextQuery-Attribut des [typeInfo-Elements](./propdesc-schema-typeinfo.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[Typeinfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[Stringformat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[Numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[Filtercontrol](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> </dl>

 

 
