---
description: Damit ein Client ein PrintTicket erstellen kann, muss das PrintCapabilities-Dokument Eigenschaften von Featureinstanzen und Optionsinstanzen im Feature bereitstellen.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Wichtige Eigenschafteninstanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4691b73b1206ee092c171b213a3815925b7f53c6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409123"
---
# <a name="important-property-instances"></a><span data-ttu-id="0c513-103">Wichtige Eigenschafteninstanzen</span><span class="sxs-lookup"><span data-stu-id="0c513-103">Important Property Instances</span></span>

<span data-ttu-id="0c513-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="0c513-104">This topic is not current.</span></span> <span data-ttu-id="0c513-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="0c513-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0c513-106">Damit ein PrintCapabilities-Client ein angemessenes PrintTicket erstellen kann, muss das PrintCapabilities-Dokument bestimmte Eigenschaften von Featureinstanzen sowie Optionsinstanzen innerhalb des Features bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0c513-106">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="0c513-107">Ein generisches Benutzeroberflächenmodul erfordert solche Informationen, um eine Benutzeroberfläche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0c513-107">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="0c513-108">Dies erfordert wiederum, dass die Druckschemaschlüsselwörter einige Eigenschafteninstanzen definieren, die als untergeordnete Elemente von Feature- und Optionselementen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0c513-108">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="0c513-109">Featureelemente können die folgende Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c513-109">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="0c513-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0c513-110">Property</span></span>                  | <span data-ttu-id="0c513-111">Werte</span><span class="sxs-lookup"><span data-stu-id="0c513-111">Values</span></span>                                 | <span data-ttu-id="0c513-112">Zweck</span><span class="sxs-lookup"><span data-stu-id="0c513-112">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c513-113">SelectionType</span><span class="sxs-lookup"><span data-stu-id="0c513-113">SelectionType</span></span> <br/> | <span data-ttu-id="0c513-114">PickOne</span><span class="sxs-lookup"><span data-stu-id="0c513-114">PickOne</span></span><br/> <span data-ttu-id="0c513-115">PickMany</span><span class="sxs-lookup"><span data-stu-id="0c513-115">PickMany</span></span><br/> | <span data-ttu-id="0c513-116">Gibt die Anzahl der Optionen an, die für dieses Feature zu einem bestimmten Zeitpunkt ausgewählt werden können, entweder eine (PickOne) oder mehrere Optionen (PickMany).</span><span class="sxs-lookup"><span data-stu-id="0c513-116">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="0c513-117">Der Client kann diese Informationen verwenden, um ein PrintTicket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0c513-117">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="0c513-118">Diese Informationen wirken sich auf das Benutzeroberflächenverhalten und die PrintTicket-Überprüfung durch den Anbieter aus.</span><span class="sxs-lookup"><span data-stu-id="0c513-118">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="0c513-119">Optionselemente können die folgende Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c513-119">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="0c513-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0c513-120">Property</span></span>                   | <span data-ttu-id="0c513-121">Werte</span><span class="sxs-lookup"><span data-stu-id="0c513-121">Values</span></span>                           | <span data-ttu-id="0c513-122">Zweck</span><span class="sxs-lookup"><span data-stu-id="0c513-122">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c513-123">IdentityOption</span><span class="sxs-lookup"><span data-stu-id="0c513-123">IdentityOption</span></span> <br/> | <span data-ttu-id="0c513-124">True</span><span class="sxs-lookup"><span data-stu-id="0c513-124">True</span></span><br/> <span data-ttu-id="0c513-125">Falsch</span><span class="sxs-lookup"><span data-stu-id="0c513-125">False</span></span><br/> | <span data-ttu-id="0c513-126">Das Auswählen der IdentityOption-Eigenschaft wird so interpretiert, dass diese Funktion deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="0c513-126">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="0c513-127">Ein Feature, das eine SelectionType-Eigenschaft enthält, deren Wert PickMany ist, muss auch eine Option mit einer IdentityOption-Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c513-127">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="0c513-128">Der Benutzeroberflächencode (oder der Client, der ein PrintTicket erstellt) muss jede andere Option deaktivieren, wenn die IdentityOption-Eigenschaft ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="0c513-128">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="0c513-129">Die Elemente Feature, Option und ParameterDef können die folgende Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c513-129">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="0c513-130">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0c513-130">Property</span></span>              | <span data-ttu-id="0c513-131">Werte</span><span class="sxs-lookup"><span data-stu-id="0c513-131">Values</span></span>                          | <span data-ttu-id="0c513-132">Zweck</span><span class="sxs-lookup"><span data-stu-id="0c513-132">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c513-133">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="0c513-133">DisplayUI</span></span> <br/> | <span data-ttu-id="0c513-134">Anzeigen</span><span class="sxs-lookup"><span data-stu-id="0c513-134">Show</span></span><br/> <span data-ttu-id="0c513-135">Ausblenden</span><span class="sxs-lookup"><span data-stu-id="0c513-135">Hide</span></span><br/> | <span data-ttu-id="0c513-136">Gibt an, ob das übergeordnete Element auf der Benutzeroberfläche angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c513-136">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="0c513-137">Show gibt an, dass das Element auf der Benutzeroberfläche angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c513-137">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="0c513-138">Ausblenden gibt an, dass das Element nicht auf der Benutzeroberfläche angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c513-138">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="0c513-139">Wenn diese Eigenschaft nicht für ein Element definiert ist, lautet die Standardinterpretation Show, was bedeutet, dass das Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0c513-139">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="0c513-140">Die Elemente Feature, Option und ParameterDef können die folgende Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="0c513-140">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="0c513-141">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="0c513-141">Property</span></span>                | <span data-ttu-id="0c513-142">Wert</span><span class="sxs-lookup"><span data-stu-id="0c513-142">Value</span></span>             | <span data-ttu-id="0c513-143">Zweck</span><span class="sxs-lookup"><span data-stu-id="0c513-143">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c513-144">DisplayName</span><span class="sxs-lookup"><span data-stu-id="0c513-144">DisplayName</span></span> <br/> | <span data-ttu-id="0c513-145">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0c513-145">String</span></span><br/> | <span data-ttu-id="0c513-146">Gibt die Anzeigezeichenfolge für das übergeordnete Element an und überschreibt den Standardanzeigenamen.</span><span class="sxs-lookup"><span data-stu-id="0c513-146">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="0c513-147">Kann von PrintCapabilities-Anbietern verwendet werden, um einen lokalisierten und benutzerfreundlichen Anzeigenamen darzustellen.</span><span class="sxs-lookup"><span data-stu-id="0c513-147">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="0c513-148">Der Standardwert für den Anzeigenamen ist das Name-Attribut für das übergeordnete Element.</span><span class="sxs-lookup"><span data-stu-id="0c513-148">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="0c513-149">Wenn bei Option-Elementen das Name-Attribut nicht angegeben wird, muss die DisplayName-Eigenschaft vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="0c513-149">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="0c513-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0c513-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c513-151">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="0c513-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




