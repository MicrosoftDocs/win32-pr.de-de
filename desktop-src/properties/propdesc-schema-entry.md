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
# <a name="understanding-the-property-description-schema"></a><span data-ttu-id="47ab0-103">Grundlegendes zum Eigenschafts Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="47ab0-103">Understanding the Property Description Schema</span></span>

<span data-ttu-id="47ab0-104">In diesem Thema wird das Eigenschafts Beschreibungs Schema eingeführt, das vom Shell-Eigenschaften System verwendet wird</span><span class="sxs-lookup"><span data-stu-id="47ab0-104">This topic introduces the property description schema used by the Shell property system.</span></span>

<span data-ttu-id="47ab0-105">Die Einführung neuer Features für Windows Vista und höher erforderte, dass das vorhandene shelleigenschaftensystem auf Folgendes erweitert werden muss:</span><span class="sxs-lookup"><span data-stu-id="47ab0-105">The introduction of new features for Windows Vista and later required that the existing Shell property system be extended to:</span></span>

-   <span data-ttu-id="47ab0-106">Unterstützen Sie ein umfassendes und erweiterbares Eigenschafts Beschreibungs System, das Informationen zu Eigenschaften wie anzeigen Amen, Typ, Anzeigetyp, Sortier-und Gruppenverhalten und anderen Attributen bereitstellt, die erforderlich sind, um die Eigenschaften anzuzeigen und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="47ab0-106">Support a rich and extensible property description system that provides information about properties including display names, type, display type, sort and group behavior, and other attributes needed to present and operate over the properties.</span></span>
-   <span data-ttu-id="47ab0-107">Unterstützen Sie eine Bestandsliste von Eigenschafts Typen (in Kombination mit der Benutzeroberfläche, die diese Typen in verschiedenen Ansichten bearbeiten kann, wie z. b. ListView, Vorschaubereich, Eigenschaften Dialogfelder usw.), die verschiedenen Eigenschaften zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="47ab0-107">Support a stock list of property types (combined with UI that can edit those types in different views like the listview, preview pane, property dialogs, and so on) that can be associated with various properties.</span></span>
-   <span data-ttu-id="47ab0-108">Geben Sie Eigenschaften Beschreibungs Listen an, die den Satz von Eigenschaften definieren, die in unterschiedlichen Ansichten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="47ab0-108">Supply property description lists, which define the set of properties displayed in various views.</span></span>
-   <span data-ttu-id="47ab0-109">Stellen Sie eine vereinfachte Schnittstelle ( [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) bereit, sodass Eigenschafts Handler einfacher geschrieben werden können, sodass Eigenschaften in Dateien persistent gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="47ab0-109">Provide a simplified interface, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), so property handlers can be written more easily and so properties can be persisted to files.</span></span>
-   <span data-ttu-id="47ab0-110">Unterstützung für nicht-Dateieigenschaften Handler, um Eigenschaften in der Ansicht verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="47ab0-110">Support for non-file property handlers to expose properties in the view.</span></span>

<span data-ttu-id="47ab0-111">Diese Features werden in einer Architektur erzielt, die abstrakten Zugriff auf die Eigenschaften eines shellelements bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="47ab0-111">These features are achieved on an architecture that provides abstract access to the properties of a Shell item.</span></span> <span data-ttu-id="47ab0-112">Diese Abstraktion wird als shelleigenschaftensystem bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="47ab0-112">This abstraction is called the Shell property system.</span></span>

-   [<span data-ttu-id="47ab0-113">Was ist das Eigenschafts Beschreibungs Schema?</span><span class="sxs-lookup"><span data-stu-id="47ab0-113">What Is the Property Description Schema?</span></span>](#what-is-the-property-description-schema)
-   [<span data-ttu-id="47ab0-114">Gründe für die Verwendung eines Schemas</span><span class="sxs-lookup"><span data-stu-id="47ab0-114">Why Use a Schema?</span></span>](#why-use-a-schema)
-   [<span data-ttu-id="47ab0-115">Was sind die wichtigsten Schema Teile?</span><span class="sxs-lookup"><span data-stu-id="47ab0-115">What Are the Major Schema Parts?</span></span>](#what-are-the-major-schema-parts)
-   [<span data-ttu-id="47ab0-116">Änderungen für Windows 7</span><span class="sxs-lookup"><span data-stu-id="47ab0-116">Changes for Windows 7</span></span>](#changes-for-windows-7)
-   [<span data-ttu-id="47ab0-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47ab0-117">Related topics</span></span>](#related-topics)

## <a name="what-is-the-property-description-schema"></a><span data-ttu-id="47ab0-118">Was ist das Eigenschafts Beschreibungs Schema?</span><span class="sxs-lookup"><span data-stu-id="47ab0-118">What Is the Property Description Schema?</span></span>

<span data-ttu-id="47ab0-119">Das Schema Subsystem besteht aus folgendem:</span><span class="sxs-lookup"><span data-stu-id="47ab0-119">The schema subsystem consists of the following:</span></span>

-   <span data-ttu-id="47ab0-120">Eine oder mehrere. PropDesc-Schema Dateien, die Eigenschafts Beschreibungen definieren.</span><span class="sxs-lookup"><span data-stu-id="47ab0-120">One or more .propdesc schema files that define property descriptions.</span></span> <span data-ttu-id="47ab0-121">Das Eigenschafts Beschreibungs Schema wird in einer Auflistung von XML-Schema Dateien (mit der Dateierweiterung ". PropDesc") zur Laufzeit des Systems definiert.</span><span class="sxs-lookup"><span data-stu-id="47ab0-121">The property description schema is defined in a collection of XML schema files (using the .propdesc file extension) at runtime on the system.</span></span> <span data-ttu-id="47ab0-122">Diese Dateien werden verzögert geladen, wenn Sie von einem Teil des Eigenschaften Systems benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="47ab0-122">These files are lazy-loaded when a part of the property system requires them.</span></span>
-   <span data-ttu-id="47ab0-123">Ein in-Memory-Schema Cache zum Speichern der analysierten Schema Dateien, die alle Eigenschafts Beschreibungen enthalten, die mit dem Subsystem eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="47ab0-123">An in-memory schema cache used to store the parsed schema files, which include all property descriptions introduced to the subsystem.</span></span> <span data-ttu-id="47ab0-124">Es ist nicht erforderlich, die. PropDesc-Konfigurationsdateien zu analysieren, die das Schema beschreiben.</span><span class="sxs-lookup"><span data-stu-id="47ab0-124">There is no need to reparse the .propdesc config files that describe the schema.</span></span> <span data-ttu-id="47ab0-125">Weitere Informationen finden Sie unter [**psregisterpropertyschema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**psunregisterpropertyschema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)und [**psrefreshpropertyschema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span><span class="sxs-lookup"><span data-stu-id="47ab0-125">For more information, see [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema), and [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span></span>
-   <span data-ttu-id="47ab0-126">Ein subsystemobjekt, das [**ipropertysystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem)implementiert, das verwendet wird, um Eigenschafts Beschreibungen abzurufen oder mit Ihnen zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="47ab0-126">A subsystem object that implements [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), which is used to obtain or work with property descriptions.</span></span>
-   <span data-ttu-id="47ab0-127">Ein subsystemobjekt, das [**ipropertydescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription)implementiert, das verwendet wird, um basierend auf einer Eigenschafts Beschreibung zu informieren und zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="47ab0-127">A subsystem object that implements [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), which is used to inform and operate based on a property description.</span></span>
-   <span data-ttu-id="47ab0-128">Ein subsystemobjekt, das [**ipropertydescriptionlist**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist)implementiert, das als Auflistung von Eigenschafts Beschreibungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="47ab0-128">A subsystem object that implements [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which is used as a collection of property descriptions.</span></span>

> [!Note]  
> <span data-ttu-id="47ab0-129">Sie müssen `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` dem Root-Schema Element ihrer. PropDesc-Dateien hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="47ab0-129">You must add `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` to the root schema element of your .propdesc files.</span></span>

 

## <a name="why-use-a-schema"></a><span data-ttu-id="47ab0-130">Gründe für die Verwendung eines Schemas</span><span class="sxs-lookup"><span data-stu-id="47ab0-130">Why Use a Schema?</span></span>

<span data-ttu-id="47ab0-131">Eigenständige Eigenschaften sind nicht typsicher.</span><span class="sxs-lookup"><span data-stu-id="47ab0-131">Properties, by themselves, are not type-safe.</span></span> <span data-ttu-id="47ab0-132">Eine Komponente kann der System. Author-Eigenschaft einen numerischen Wert oder einen [**Dateizeit**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Datumsstempel der System. Music. albumtitle-Eigenschaft zuweisen. ohne weitere Erzwingung oder Anleitungen wird Sie von den Eigenschaften speichern zugelassen.</span><span class="sxs-lookup"><span data-stu-id="47ab0-132">A component can assign a numerical value to the System.Author property, or a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) date-stamp to the System.Music.AlbumTitle property, and, without any further enforcement or guidance, the property stores will allow it.</span></span> <span data-ttu-id="47ab0-133">Wir mussten also einen Begriff "schematisieren", um die Eigenschaften zu "schematisieren", was uns zum Schema Subsystem führt.</span><span class="sxs-lookup"><span data-stu-id="47ab0-133">So, we needed a notion to "schematize" the properties, which brings us to the schema subsystem.</span></span>

## <a name="what-are-the-major-schema-parts"></a><span data-ttu-id="47ab0-134">Was sind die wichtigsten Schema Teile?</span><span class="sxs-lookup"><span data-stu-id="47ab0-134">What Are the Major Schema Parts?</span></span>

<span data-ttu-id="47ab0-135">Das vom shelleigenschafts System verwendete Eigenschafts Beschreibungs Schema besteht aus einem einzelnen [propertydescriptionlist](./propdesc-schema-propertydescriptionlist.md) -Element sowie einem *Schemaversion* -Attribut, das die Version dieses Schema Definitions Formats angibt.</span><span class="sxs-lookup"><span data-stu-id="47ab0-135">The property description schema used by the Shell property system is composed of a single [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) element, as well as a *schemaVersion* attribute, which indicates the version of this schema definition format.</span></span> <span data-ttu-id="47ab0-136">Hinweis: der Wert muss "1,0" sein.</span><span class="sxs-lookup"><span data-stu-id="47ab0-136">Note: value must be "1.0".</span></span>


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



<span data-ttu-id="47ab0-137">Die [propertydescriptionlist](./propdesc-schema-propertydescriptionlist.md) besteht aus einem oder mehreren [propertydescription](./propdesc-schema-propertydescription.md) -Elementen sowie aus *Verleger* -und *Produkt* Attributen.</span><span class="sxs-lookup"><span data-stu-id="47ab0-137">The [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) is composed of one or more [propertyDescription](./propdesc-schema-propertydescription.md) elements, as well as *publisher* and *product* attributes.</span></span>


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



<span data-ttu-id="47ab0-138">Eine [propertydescription](./propdesc-schema-propertydescription.md) besteht aus einem [SearchInfo](./propdesc-schema-searchinfo.md) -Element und keinem oder einem " [Labelinfo](./propdesc-schema-labelinfo.md)", einem [TypeInfo](./propdesc-schema-typeinfo.md)-Element und einem [DisplayInfo](./propdesc-schema-displayinfo.md) -Element sowie den Attributen " *FormatID*", " *PROPID*", " *propstr*" und " *Name* ".</span><span class="sxs-lookup"><span data-stu-id="47ab0-138">A [propertyDescription](./propdesc-schema-propertydescription.md) is composed of one [searchInfo](./propdesc-schema-searchinfo.md) and zero or one [labelInfo](./propdesc-schema-labelinfo.md), [typeInfo](./propdesc-schema-typeinfo.md), and [displayInfo](./propdesc-schema-displayinfo.md) elements, as well as *formatID*, *propID*, *propstr*, and *name* attributes.</span></span>

<span data-ttu-id="47ab0-139">Es sollte ein [propertydescription](./propdesc-schema-propertydescription.md) -Element für jeden eindeutigen kanonischen Eigenschaftsnamen vorhanden sein, der im System verfügbar sein soll.</span><span class="sxs-lookup"><span data-stu-id="47ab0-139">There should be one [propertyDescription](./propdesc-schema-propertydescription.md) element for every unique canonical property name that is intended to be available in the system.</span></span> <span data-ttu-id="47ab0-140">Die Zeichen folgen Attribute haben ein Limit von 512 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="47ab0-140">The string attributes have a limit of 512 characters.</span></span> <span data-ttu-id="47ab0-141">Werte, die länger als 512 Zeichen sind, werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="47ab0-141">Values longer than 512 characters are truncated.</span></span>


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



## <a name="changes-for-windows-7"></a><span data-ttu-id="47ab0-142">Änderungen für Windows 7</span><span class="sxs-lookup"><span data-stu-id="47ab0-142">Changes for Windows 7</span></span>

<span data-ttu-id="47ab0-143">Das Eigenschafts Beschreibungs Schema wurde für Windows 7 geändert.</span><span class="sxs-lookup"><span data-stu-id="47ab0-143">The property description schema has been changed for Windows 7.</span></span> <span data-ttu-id="47ab0-144">Dabei handelt es sich um nicht unterbrechende Änderungen.</span><span class="sxs-lookup"><span data-stu-id="47ab0-144">These are non-breaking changes.</span></span> <span data-ttu-id="47ab0-145">Wenn ein Eigenschafts Element oder-Attribut in Windows 7 nicht mehr unterstützt wird, ignoriert das Windows 7-Betriebssystem das Windows Vista-Element oder die Windows Vista-Attribute.</span><span class="sxs-lookup"><span data-stu-id="47ab0-145">If a property element or attribute is no longer supported in Windows 7, the Windows 7 operating system ignores the Windows Vista element or attributes.</span></span> <span data-ttu-id="47ab0-146">Ebenso ignoriert Windows Vista auch neue Eigenschaften Elemente oder Attribute von Windows 7.</span><span class="sxs-lookup"><span data-stu-id="47ab0-146">Similarly, Windows Vista ignores new Windows 7 property elements or attributes as well.</span></span>

<span data-ttu-id="47ab0-147">Es wird jedoch empfohlen, benutzerdefinierte Eigenschaften für Windows 7 zu aktualisieren, um eine bessere und konsistentere Benutzer Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="47ab0-147">However, updating custom properties for Windows 7 is recommended for a better and more consistent user experience.</span></span>

<span data-ttu-id="47ab0-148">Im folgenden finden Sie neue Elemente und Attribute:</span><span class="sxs-lookup"><span data-stu-id="47ab0-148">The following are new elements and attributes:</span></span>

-   <span data-ttu-id="47ab0-149">[relatedpropertyinfo](./propdesc-schema-relatedpropertyinfo.md) -und [relatedproperty](./propdesc-schema-relatedproperty.md) -Elemente</span><span class="sxs-lookup"><span data-stu-id="47ab0-149">[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) and [relatedProperty](./propdesc-schema-relatedproperty.md) elements</span></span>
-   <span data-ttu-id="47ab0-150">[Image](./propdesc-schema-image.md) -Element</span><span class="sxs-lookup"><span data-stu-id="47ab0-150">[image](./propdesc-schema-image.md) element</span></span>
-   <span data-ttu-id="47ab0-151">mnetmonics-Attribut des [SearchInfo](./propdesc-schema-searchinfo.md) -Elements</span><span class="sxs-lookup"><span data-stu-id="47ab0-151">mnemonics attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>
-   <span data-ttu-id="47ab0-152">mnetmonics-Attribut des [Enumeration](./propdesc-schema-enum.md) -Elements</span><span class="sxs-lookup"><span data-stu-id="47ab0-152">mnemonics attribute of the [enum](./propdesc-schema-enum.md) element</span></span>
-   <span data-ttu-id="47ab0-153">searchrawvalue-Attribut des [Typeingabe Info](./propdesc-schema-typeinfo.md) -Elements</span><span class="sxs-lookup"><span data-stu-id="47ab0-153">searchRawValue attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

<span data-ttu-id="47ab0-154">Die folgenden Elemente und Attribute wurden geändert:</span><span class="sxs-lookup"><span data-stu-id="47ab0-154">The following elements and attributes have changed:</span></span>

-   <span data-ttu-id="47ab0-155">[enumeratedlist](./propdesc-schema-enumeratedlist.md)-, [Enumeration](./propdesc-schema-enum.md)-und [enumrange](./propdesc-schema-enumrange.md) -Elemente</span><span class="sxs-lookup"><span data-stu-id="47ab0-155">[enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md), and [enumRange](./propdesc-schema-enumrange.md) elements</span></span>
-   <span data-ttu-id="47ab0-156">[DrawControl](./propdesc-schema-drawcontrol.md) -Element</span><span class="sxs-lookup"><span data-stu-id="47ab0-156">[drawControl](./propdesc-schema-drawcontrol.md) element</span></span>
-   <span data-ttu-id="47ab0-157">[editcontrol](./propdesc-schema-editcontrol.md) -Element</span><span class="sxs-lookup"><span data-stu-id="47ab0-157">[editControl](./propdesc-schema-editcontrol.md) element</span></span>
-   <span data-ttu-id="47ab0-158">PROPID-Attribut des [propertydescription](./propdesc-schema-propertydescription.md) -Elements</span><span class="sxs-lookup"><span data-stu-id="47ab0-158">propID attribute of the [propertyDescription](./propdesc-schema-propertydescription.md) element</span></span>
-   <span data-ttu-id="47ab0-159">columnindextype-Attribut des [SearchInfo](./propdesc-schema-searchinfo.md) -Elements</span><span class="sxs-lookup"><span data-stu-id="47ab0-159">columnIndexType attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>

<span data-ttu-id="47ab0-160">Die folgenden Elemente und Attribute wurden entfernt:</span><span class="sxs-lookup"><span data-stu-id="47ab0-160">The following elements and attributes have been removed:</span></span>

-   <span data-ttu-id="47ab0-161">[querycontrol](./propdesc-schema-querycontrol.md) -Element</span><span class="sxs-lookup"><span data-stu-id="47ab0-161">[queryControl](./propdesc-schema-querycontrol.md) element</span></span>
-   <span data-ttu-id="47ab0-162">isquervable-Attribut des [Typeingabe Info](./propdesc-schema-typeinfo.md) -Elements</span><span class="sxs-lookup"><span data-stu-id="47ab0-162">isQueryable attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>
-   <span data-ttu-id="47ab0-163">includeinfulltextquery-Attribut des [TypeInfo](./propdesc-schema-typeinfo.md) -Elements</span><span class="sxs-lookup"><span data-stu-id="47ab0-163">includeInFullTextQuery attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

## <a name="related-topics"></a><span data-ttu-id="47ab0-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47ab0-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47ab0-165">propertydescription</span><span class="sxs-lookup"><span data-stu-id="47ab0-165">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="47ab0-166">SearchInfo</span><span class="sxs-lookup"><span data-stu-id="47ab0-166">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="47ab0-167">Labelinfo</span><span class="sxs-lookup"><span data-stu-id="47ab0-167">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="47ab0-168">TypeInfo</span><span class="sxs-lookup"><span data-stu-id="47ab0-168">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="47ab0-169">Display Info</span><span class="sxs-lookup"><span data-stu-id="47ab0-169">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="47ab0-170">StringFormat</span><span class="sxs-lookup"><span data-stu-id="47ab0-170">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="47ab0-171">BooleanFormat</span><span class="sxs-lookup"><span data-stu-id="47ab0-171">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="47ab0-172">NumberFormat</span><span class="sxs-lookup"><span data-stu-id="47ab0-172">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="47ab0-173">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="47ab0-173">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="47ab0-174">enumeratedlist</span><span class="sxs-lookup"><span data-stu-id="47ab0-174">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="47ab0-175">DrawControl</span><span class="sxs-lookup"><span data-stu-id="47ab0-175">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="47ab0-176">editcontrol</span><span class="sxs-lookup"><span data-stu-id="47ab0-176">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="47ab0-177">FilterControl</span><span class="sxs-lookup"><span data-stu-id="47ab0-177">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="47ab0-178">querycontrol</span><span class="sxs-lookup"><span data-stu-id="47ab0-178">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="47ab0-179">image</span><span class="sxs-lookup"><span data-stu-id="47ab0-179">image</span></span>](./propdesc-schema-image.md)
</dt> </dl>

 

 
