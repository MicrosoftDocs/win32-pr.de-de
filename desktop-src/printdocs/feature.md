---
description: Überprüfen Sie Featureelemente, die eine Liste von Options- und Property-Elementen enthalten, die ein Geräteattribut, eine Auftragsformatierungseinstellung oder ein anderes relevantes Merkmal beschreiben.
ms.assetid: 5a6553c2-f322-47e2-bbc8-44f6541f1288
title: Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28ab7e8cc69ecc9ba3956fbae3c5278baace8cf
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120635"
---
# <a name="feature"></a><span data-ttu-id="0285c-103">Funktion</span><span class="sxs-lookup"><span data-stu-id="0285c-103">Feature</span></span>

<span data-ttu-id="0285c-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0285c-104">This topic is not current.</span></span> <span data-ttu-id="0285c-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="0285c-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0285c-106">Ein Feature-Element enthält eine vollständige Liste der Option- und Property-Elemente, die ein Geräteattribut, eine Auftragsformatierungseinstellung oder ein anderes relevantes Merkmal vollständig beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0285c-106">A Feature element contains a complete list of the Option and Property elements that fully describe a device attribute, job formatting setting, or other relevant characteristic.</span></span>

## <a name="element-tag"></a><span data-ttu-id="0285c-107">Elementtag</span><span class="sxs-lookup"><span data-stu-id="0285c-107">Element Tag</span></span>

<Feature>

## <a name="xml-attributes"></a><span data-ttu-id="0285c-108">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="0285c-108">XML Attributes</span></span>

<span data-ttu-id="0285c-109">In der folgenden Tabelle sind die XML-Attribute aufgeführt, die zu diesem Element gehören können.</span><span class="sxs-lookup"><span data-stu-id="0285c-109">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="0285c-110">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="0285c-110">XML Attribute</span></span>   | <span data-ttu-id="0285c-111">Details</span><span class="sxs-lookup"><span data-stu-id="0285c-111">Details</span></span>                                                                                              |
|-----------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0285c-112">name</span><span class="sxs-lookup"><span data-stu-id="0285c-112">name</span></span><br/> | <span data-ttu-id="0285c-113">Enthält den Namen des Features, entweder ein Standardfeature oder ein privat definiertes Feature.</span><span class="sxs-lookup"><span data-stu-id="0285c-113">Holds the name of the Feature, either a standard Feature or a privately-defined Feature.</span></span> <br/> |



 

<span data-ttu-id="0285c-114">Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="0285c-114">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="0285c-115">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0285c-115">Element Information</span></span>

<span data-ttu-id="0285c-116">In der folgenden Tabelle sind die Elemente aufgeführt, die möglicherweise die untergeordneten Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="0285c-116">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0285c-117">Category</span><span class="sxs-lookup"><span data-stu-id="0285c-117">Category</span></span></th>
<th><span data-ttu-id="0285c-118">Details</span><span class="sxs-lookup"><span data-stu-id="0285c-118">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0285c-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0285c-119">Parent elements</span></span><br/></td>
<td><span data-ttu-id="0285c-120">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="0285c-120">PrintCapabilities</span></span> <br/> <span data-ttu-id="0285c-121">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="0285c-121">PrintTicket</span></span> <br/> <span data-ttu-id="0285c-122">Funktion</span><span class="sxs-lookup"><span data-stu-id="0285c-122">Feature</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0285c-123">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0285c-123">Child elements</span></span><br/></td>
<td><span data-ttu-id="0285c-124">Eine der folgenden Gruppen:</span><span class="sxs-lookup"><span data-stu-id="0285c-124">One of the following groups:</span></span><br/>
<ul>
<li><span data-ttu-id="0285c-125"><em>Feature</em> (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="0285c-125"><em>Feature</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="0285c-126"><em>Option</em> (mindestens eine Option)</span><span class="sxs-lookup"><span data-stu-id="0285c-126"><em>Option</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="0285c-127"><em>Eigenschaft</em> (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="0285c-127"><em>Property</em> (zero or more)</span></span><br/></li>
</ul>
<span data-ttu-id="0285c-128">oder</span><span class="sxs-lookup"><span data-stu-id="0285c-128">or</span></span> <br/>
<ul>
<li><span data-ttu-id="0285c-129">Feature (mindestens ein <em>Feature)</em></span><span class="sxs-lookup"><span data-stu-id="0285c-129"><em>Feature</em> (one or more)</span></span><br/></li>
<li><span data-ttu-id="0285c-130"><em>Option</em> (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="0285c-130"><em>Option</em> (zero or more)</span></span><br/></li>
<li><span data-ttu-id="0285c-131"><em>Eigenschaft</em> (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="0285c-131"><em>Property</em> (zero or more)</span></span><br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0285c-132">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="0285c-132">This element</span></span><br/></td>
<td><span data-ttu-id="0285c-133">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="0285c-133">No character data is permitted.</span></span><br/> <span data-ttu-id="0285c-134">Doppelte untergeordnete Optionselemente, die gleichgeordnete Elemente sind, sind zulässig.</span><span class="sxs-lookup"><span data-stu-id="0285c-134">Duplicate child Option elements that are siblings are permitted.</span></span> <span data-ttu-id="0285c-135">Doppelte Namensattributverknüpfungen zulässig.</span><span class="sxs-lookup"><span data-stu-id="0285c-135">Duplicate name attribute shortcuts permitted.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="configuration-dependencies"></a><span data-ttu-id="0285c-136">Konfigurationsabhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="0285c-136">Configuration Dependencies</span></span>

<span data-ttu-id="0285c-137">Featureelemente weisen möglicherweise keine Konfigurationsabhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="0285c-137">Feature elements may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="0285c-138">Elementverwendung</span><span class="sxs-lookup"><span data-stu-id="0285c-138">Element Usage</span></span>

### <a name="relationship-to-xml-attributes"></a><span data-ttu-id="0285c-139">Beziehung zu XML-Attributen</span><span class="sxs-lookup"><span data-stu-id="0285c-139">Relationship to XML Attributes</span></span>

<span data-ttu-id="0285c-140">In der Feature-/Optionsdarstellung wird ein Geräteattribut durch ein Feature-Element dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0285c-140">In Feature/Option representation, a device attribute is represented by a Feature element.</span></span> <span data-ttu-id="0285c-141">Das Geräteattribut wird durch das Name-Attribut im Feature-Element des Geräteattributs eindeutig identifiziert, wie im folgenden Beispiel.</span><span class="sxs-lookup"><span data-stu-id="0285c-141">The device attribute is uniquely identified by the name attribute in the device attribute's Feature element, as in the following example.</span></span> <span data-ttu-id="0285c-142">In diesem Beispiel lautet das Geräteattribut Auflösung.</span><span class="sxs-lookup"><span data-stu-id="0285c-142">In this example, the device attribute is Resolution.</span></span>

``` syntax
<Feature name="Resolution" />
```

<span data-ttu-id="0285c-143">Das Druckschema definiert einen Satz von Namensattributen für bestimmte Featureinstanzen.</span><span class="sxs-lookup"><span data-stu-id="0285c-143">The Print Schema defines a set of name attributes for certain Feature instances.</span></span> <span data-ttu-id="0285c-144">Diese Namensattribute dienen zum Identifizieren eines Satzes vordefinierter Featureinstanzen, die bestimmten konfigurierbaren Geräteattributen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0285c-144">These name attributes serve to identify a set of predefined Feature instances associated with specific configurable device attributes.</span></span> <span data-ttu-id="0285c-145">Diese Funktionsinstanznamen sollten nach Möglichkeit verwendet werden, da sie die Portabilität Ihres PrintCapabilities-Dokuments und der von ihnen abgeleiteten PrintTickets erhöhen.</span><span class="sxs-lookup"><span data-stu-id="0285c-145">These Feature instance names should be used whenever applicable, because they increase the portability of your PrintCapabilities document and the PrintTickets that are derived from them.</span></span> <span data-ttu-id="0285c-146">Privat definierte Featureinstanzen können eingeführt werden, wenn bestimmte Geräteattribute keiner der schemadefinierte Featureinstanzen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0285c-146">Privately-defined Feature instances may be introduced if certain device attributes do not correspond to any of the schema-defined Feature instances.</span></span> <span data-ttu-id="0285c-147">Informationen zur Syntax für Namensattribute und zu den Konventionen, die für schemadefinierte und private Namen gelten, finden Sie unter [XML-Attribute.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="0285c-147">For information about the syntax for name attributes and the conventions that apply to schema-defined and privately-defined names, see [XML Attributes](xml-attributes.md).</span></span>

### <a name="relationship-to-option-element"></a><span data-ttu-id="0285c-148">Beziehung zum Option-Element</span><span class="sxs-lookup"><span data-stu-id="0285c-148">Relationship to Option Element</span></span>

<span data-ttu-id="0285c-149">Jeder der möglichen Zustände wird durch ein Option-Element dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0285c-149">Each of the possible states is represented by an Option element.</span></span> <span data-ttu-id="0285c-150">Jede Option-Definition enthält mindestens ein ScoredProperty-Element, das den dargestellten Zustand eindeutig beschreibt oder kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="0285c-150">Each Option definition contains one or more ScoredProperty elements, which taken together uniquely describe or characterize the state that is being represented.</span></span> <span data-ttu-id="0285c-151">Das Verfahren zum Erstellen von Optionsdefinitionen wird unter [Optionsdefinitionen](option-definitions.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0285c-151">The technique used to create Option definitions is described in [Option Definitions](option-definitions.md).</span></span> <span data-ttu-id="0285c-152">Alle Option-Elemente, die einem bestimmten Feature-Element zugeordnet sind, befinden sich als untergeordnete Elemente des Feature-Elements.</span><span class="sxs-lookup"><span data-stu-id="0285c-152">All of the Option elements associated with a particular Feature element reside as child elements of the Feature element.</span></span>

### <a name="subfeatures"></a><span data-ttu-id="0285c-153">Unterfeatures</span><span class="sxs-lookup"><span data-stu-id="0285c-153">Subfeatures</span></span>

<span data-ttu-id="0285c-154">Das Druckschemaframework ermöglicht auch die hierarchische Gruppierung von Featureelementen.</span><span class="sxs-lookup"><span data-stu-id="0285c-154">The Print Schema Framework also allows Feature elements to be grouped together in a hierarchical manner.</span></span> <span data-ttu-id="0285c-155">Das heißt, ein Feature-Element kann selbst ein oder mehrere untergeordnete Feature-Elemente (Unterfeatures) enthalten.</span><span class="sxs-lookup"><span data-stu-id="0285c-155">That is, a Feature element can itself contain one or more child Feature elements (subfeatures).</span></span> <span data-ttu-id="0285c-156">Dies kann nützlich sein, um verwandte Featureelemente zu organisieren, oder für Featureelemente, die Aspekte eines Gerätefeatures steuern.</span><span class="sxs-lookup"><span data-stu-id="0285c-156">This can be useful for organizing related Feature elements, or for Feature elements that control aspects of a device feature.</span></span> <span data-ttu-id="0285c-157">Ein Beispiel ist ein Gerät, das Das Stapling unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0285c-157">One example is a device that supports stapling.</span></span> <span data-ttu-id="0285c-158">Ein solches Gerät kann dem Benutzer die Wahl geben, wo sich die Klammer befindet, z. B. in der oberen linken Ecke, in der oberen rechten Ecke oder am oberen Rand oder am linken Rand.</span><span class="sxs-lookup"><span data-stu-id="0285c-158">Such a device might offer the user a choice of where to locate the staple, such as at the upper left corner, or the upper right corner, or along the top edge, or along the left edge.</span></span> <span data-ttu-id="0285c-159">Die Benutzeroberfläche für dieses Gerät sollte dem Benutzer zuerst die höchsten Auswahlmöglichkeiten bieten können. In diesem Fall ist dies die Verwendung von Stapling.</span><span class="sxs-lookup"><span data-stu-id="0285c-159">The user interface (UI) for this device should be able to present the user with the highest level choices first, which in this case is whether to use stapling.</span></span> <span data-ttu-id="0285c-160">Erst nachdem sich der Benutzer für die Verwendung von Stapling entschieden hat, sollte ihm eine zweite Auswahlebene angezeigt werden, also einen festen Standort.</span><span class="sxs-lookup"><span data-stu-id="0285c-160">Only after the user has decided to use stapling should he or she be presented with a second tier of choices, staple location.</span></span> <span data-ttu-id="0285c-161">Eine Featurehierarchie fügt die zusätzliche Struktur hinzu, die eine solche Benutzeroberfläche ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="0285c-161">A feature hierarchy adds the additional structure that makes such a user interface possible.</span></span> <span data-ttu-id="0285c-162">Das Druckschemaframework ermöglicht untergeordneten Features ihre eigenen untergeordneten Features, wodurch eine unbegrenzte Schachtelungsebene ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="0285c-162">The Print Schema Framework allows subfeatures to have their own child subfeatures, thereby permitting an unlimited level of nesting.</span></span>

<span data-ttu-id="0285c-163">Mit dem Druckschemaframework können Option-Elemente auch auf der gleichen Ebene wie Unterfeatures angezeigt werden. das heißt, als gleichgeordnete Elemente innerhalb desselben übergeordneten Feature-Elements.</span><span class="sxs-lookup"><span data-stu-id="0285c-163">The Print Schema Framework also allows Option elements to appear at the same level as subfeatures; that is, as siblings within the same parent Feature element.</span></span> <span data-ttu-id="0285c-164">Dadurch kann der Benutzer die übergeordnete Entscheidung treffen (ob stapling verwendet werden soll), bevor er die Teilfeatureauswahl trifft.</span><span class="sxs-lookup"><span data-stu-id="0285c-164">This allows the user to make the high level decision (whether to use stapling) before making the subfeature selections.</span></span> <span data-ttu-id="0285c-165">In diesem Beispiel enthält das Feature-Stammelement "Klammer" möglicherweise zwei Optionselemente, "On" und "Off", sowie ein Unterfeature mit dem Namen "Location".</span><span class="sxs-lookup"><span data-stu-id="0285c-165">For this example the root Feature element, "Staple", might contain two Option elements, "On" and "Off", as well as a subfeature named "StapleLocation".</span></span>

## <a name="example"></a><span data-ttu-id="0285c-166">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0285c-166">Example</span></span>

``` syntax
<psf:Feature name="psk:JobOutputBin">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option constrained="psk:None">
    <psf:ScoredProperty name="psk:Bin">
      <psf:Value xsi:type="xs:string">SorterBin</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:MediaSheetCapacity">
      <psf:Value xsi:type="xs:integer">100</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="0285c-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0285c-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0285c-168">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="0285c-168">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




