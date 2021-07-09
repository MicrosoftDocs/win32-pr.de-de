---
description: Abrufen von Informationen zum Option-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification (Spezifikation des Druckschemas).
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Option
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ac4318e6a79a3d4daa77f15901d032c66134bdd
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113549378"
---
# <a name="option"></a><span data-ttu-id="9d3cd-105">Option</span><span class="sxs-lookup"><span data-stu-id="9d3cd-105">Option</span></span>

<span data-ttu-id="9d3cd-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-106">This topic is not current.</span></span> <span data-ttu-id="9d3cd-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="9d3cd-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="9d3cd-108">Ein Option-Element enthält alle Property- und ScoredProperty-Elemente, die dieser Option zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-108">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="9d3cd-109">Elementtag</span><span class="sxs-lookup"><span data-stu-id="9d3cd-109">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="9d3cd-110">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="9d3cd-110">XML Attributes</span></span>

<span data-ttu-id="9d3cd-111">In der folgenden Tabelle sind die XML-Attribute aufgeführt, die möglicherweise zu diesem Element gehören.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="9d3cd-112">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="9d3cd-112">XML Attribute</span></span>          | <span data-ttu-id="9d3cd-113">Details</span><span class="sxs-lookup"><span data-stu-id="9d3cd-113">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d3cd-114">Eingeschränkt</span><span class="sxs-lookup"><span data-stu-id="9d3cd-114">constrained</span></span><br/> | <span data-ttu-id="9d3cd-115">Dieses Attribut ist für ein PrintCapabilities-Dokument optional.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-115">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="9d3cd-116">Dieses Attribut gibt an, ob die Option zur Auswahl oder Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-116">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="9d3cd-117">Dieses XML-Attribut kann auf einen der folgenden Werte festgelegt werden: None, PrintTicketSettings, AdminSetting oder DeviceSettings.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-117">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="9d3cd-118">Siehe [XML-Attribute.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="9d3cd-118">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="9d3cd-119">name</span><span class="sxs-lookup"><span data-stu-id="9d3cd-119">name</span></span><br/>        | <span data-ttu-id="9d3cd-120">Enthält den Namen der Option, entweder eine Standardoption oder eine privat definierte Option.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-120">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="9d3cd-121">Das XML-Attribut wird auf diese Weise verwendet, um zwischen Option-Instanzen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-121">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="9d3cd-122">Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="9d3cd-122">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="9d3cd-123">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="9d3cd-123">Element Information</span></span>

<span data-ttu-id="9d3cd-124">In der folgenden Tabelle sind die Elemente aufgeführt, die möglicherweise die untergeordneten Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-124">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="9d3cd-125">Category</span><span class="sxs-lookup"><span data-stu-id="9d3cd-125">Category</span></span>                   | <span data-ttu-id="9d3cd-126">Details</span><span class="sxs-lookup"><span data-stu-id="9d3cd-126">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d3cd-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d3cd-127">Parent elements</span></span><br/> | <span data-ttu-id="9d3cd-128">Funktion</span><span class="sxs-lookup"><span data-stu-id="9d3cd-128">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9d3cd-129">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d3cd-129">Child elements</span></span><br/>  | <span data-ttu-id="9d3cd-130">*Eigenschaft* (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="9d3cd-130">*Property* (zero or more)</span></span><br/> <span data-ttu-id="9d3cd-131">*ScoredProperty* (null oder mehr für Optionen mit dem XML-Attribut 'Name'; mindestens eine für Optionen, die das XML-Attribut 'name' nicht \* verwenden)</span><span class="sxs-lookup"><span data-stu-id="9d3cd-131">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="9d3cd-132">\* nur öffentliche Optionen, die im Druckschema definiert sind, dürfen kein "name"-Attribut aufweisen, z. B. DocumentNUp)</span><span class="sxs-lookup"><span data-stu-id="9d3cd-132">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="9d3cd-133">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="9d3cd-133">This element</span></span><br/>    | <span data-ttu-id="9d3cd-134">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-134">No character data is permitted.</span></span><br/> <span data-ttu-id="9d3cd-135">Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-135">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="9d3cd-136">Konfigurationsabhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="9d3cd-136">Configuration Dependencies</span></span>

<span data-ttu-id="9d3cd-137">Ein Optionsdefinitionselement hat möglicherweise keine Konfigurationsabhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-137">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="9d3cd-138">Elementverwendung</span><span class="sxs-lookup"><span data-stu-id="9d3cd-138">Element Usage</span></span>

<span data-ttu-id="9d3cd-139">Der Zweck des Option-Elements besteht darin, einen der Zustände zu charakterisieren, die ein durch ein Feature-Element dargestelltes Gerätekonfigurationsattribut annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-139">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="9d3cd-140">Jede Option-Elementdefinition enthält mindestens ein ScoredProperty-Element, das ein intrinsisches oder wesentliches Merkmal dieser Option beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-140">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="9d3cd-141">Zur Vereinfachung der Portabilität und Beibehaltung der Absicht definiert das Druckschema viele allgemeine Featureelemente und eine Vielzahl von Optionselementen für jedes Feature.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-141">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="9d3cd-142">Daher ist es wichtig, nach Möglichkeit ausdrucksschemadefinierte Optionselemente zu verwenden, bevor Sie eigene Optionsdefinitionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-142">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="9d3cd-143">Das Verständnis des Prozesses zum Definieren von Optionselementen bietet nützliche Einblicke in die Verwendung des PrintCapabilities-Dokuments und von PrintTickets in der Druckarchitektur von Microsoft .NET Framework Version 3.0 und Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-143">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="9d3cd-144">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9d3cd-144">Example</span></span>

<span data-ttu-id="9d3cd-145">Im folgenden Beispiel wird ein Name für die Option definiert.</span><span class="sxs-lookup"><span data-stu-id="9d3cd-145">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="9d3cd-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d3cd-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d3cd-147">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="9d3cd-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




