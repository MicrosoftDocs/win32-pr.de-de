---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Wichtige Eigenschaften Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3f58c099913b129ee7be0337ecab3343a5e5e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353645"
---
# <a name="important-property-instances"></a><span data-ttu-id="59457-104">Wichtige Eigenschaften Instanzen</span><span class="sxs-lookup"><span data-stu-id="59457-104">Important Property Instances</span></span>

<span data-ttu-id="59457-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="59457-105">This topic is not current.</span></span> <span data-ttu-id="59457-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="59457-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="59457-107">Damit ein Printworks-Client ein vernünftiges PrintTicket erstellen kann, muss das Printworks-Dokument bestimmte Eigenschaften von Funktions Instanzen sowie Options Instanzen innerhalb des Features bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="59457-107">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="59457-108">Ein generisches Benutzeroberflächen Modul benötigt solche Informationen, um eine Benutzeroberfläche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="59457-108">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="59457-109">Dies erfordert wiederum, dass die Schlüsselwörter des Druck Schemas einige Eigenschaften Instanzen definieren, die als untergeordnete Elemente von Feature-und Option-Elementen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="59457-109">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="59457-110">Funktionselemente können die folgende Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="59457-110">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="59457-111">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="59457-111">Property</span></span>                  | <span data-ttu-id="59457-112">Werte</span><span class="sxs-lookup"><span data-stu-id="59457-112">Values</span></span>                                 | <span data-ttu-id="59457-113">Zweck</span><span class="sxs-lookup"><span data-stu-id="59457-113">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59457-114">SelectionType</span><span class="sxs-lookup"><span data-stu-id="59457-114">SelectionType</span></span> <br/> | <span data-ttu-id="59457-115">Pickone</span><span class="sxs-lookup"><span data-stu-id="59457-115">PickOne</span></span><br/> <span data-ttu-id="59457-116">Pickmany</span><span class="sxs-lookup"><span data-stu-id="59457-116">PickMany</span></span><br/> | <span data-ttu-id="59457-117">Gibt die Anzahl der Optionen an, die für diese Funktion zu einem bestimmten Zeitpunkt ausgewählt werden können, entweder eine (pickone) oder mehr als eine (pickmany).</span><span class="sxs-lookup"><span data-stu-id="59457-117">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="59457-118">Der Client kann diese Informationen verwenden, um ein Print Ticket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="59457-118">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="59457-119">Diese Informationen betreffen das Verhalten der Benutzeroberfläche sowie die PrintTicket-Validierung durch den Anbieter.</span><span class="sxs-lookup"><span data-stu-id="59457-119">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="59457-120">Options Elemente können die folgende Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="59457-120">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="59457-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="59457-121">Property</span></span>                   | <span data-ttu-id="59457-122">Werte</span><span class="sxs-lookup"><span data-stu-id="59457-122">Values</span></span>                           | <span data-ttu-id="59457-123">Zweck</span><span class="sxs-lookup"><span data-stu-id="59457-123">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59457-124">Identityoption</span><span class="sxs-lookup"><span data-stu-id="59457-124">IdentityOption</span></span> <br/> | <span data-ttu-id="59457-125">Richtig</span><span class="sxs-lookup"><span data-stu-id="59457-125">True</span></span><br/> <span data-ttu-id="59457-126">False</span><span class="sxs-lookup"><span data-stu-id="59457-126">False</span></span><br/> | <span data-ttu-id="59457-127">Das Auswählen der identityoption-Eigenschaft wird so interpretiert, dass diese Funktion deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="59457-127">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="59457-128">Eine Funktion, die eine SelectionType-Eigenschaft enthält, deren Wert pickmany ist, muss auch eine Option enthalten, die über eine identityoption-Eigenschaft verfügt.</span><span class="sxs-lookup"><span data-stu-id="59457-128">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="59457-129">Der UI-Code (oder der Client, der ein Print Ticket erstellt) muss alle anderen Optionen deaktivieren, wenn die identityoption-Eigenschaft ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="59457-129">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="59457-130">Die Elemente "Feature", "Option" und "ParameterDef" können die folgende Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="59457-130">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="59457-131">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="59457-131">Property</span></span>              | <span data-ttu-id="59457-132">Werte</span><span class="sxs-lookup"><span data-stu-id="59457-132">Values</span></span>                          | <span data-ttu-id="59457-133">Zweck</span><span class="sxs-lookup"><span data-stu-id="59457-133">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59457-134">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="59457-134">DisplayUI</span></span> <br/> | <span data-ttu-id="59457-135">Anzeigen</span><span class="sxs-lookup"><span data-stu-id="59457-135">Show</span></span><br/> <span data-ttu-id="59457-136">Ausblenden</span><span class="sxs-lookup"><span data-stu-id="59457-136">Hide</span></span><br/> | <span data-ttu-id="59457-137">Gibt an, ob das übergeordnete Element in der Benutzeroberfläche angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="59457-137">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="59457-138">Anzeigen gibt an, dass das Element in der Benutzeroberfläche angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="59457-138">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="59457-139">Hide gibt an, dass das Element nicht in der Benutzeroberfläche angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="59457-139">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="59457-140">Wenn diese Eigenschaft nicht für ein Element definiert ist, wird die Standardinterpretation angezeigt, was bedeutet, dass das Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="59457-140">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="59457-141">Die Elemente "Feature", "Option" und "ParameterDef" können die folgende Eigenschaft enthalten.</span><span class="sxs-lookup"><span data-stu-id="59457-141">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="59457-142">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="59457-142">Property</span></span>                | <span data-ttu-id="59457-143">Wert</span><span class="sxs-lookup"><span data-stu-id="59457-143">Value</span></span>             | <span data-ttu-id="59457-144">Zweck</span><span class="sxs-lookup"><span data-stu-id="59457-144">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59457-145">DisplayName</span><span class="sxs-lookup"><span data-stu-id="59457-145">DisplayName</span></span> <br/> | <span data-ttu-id="59457-146">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="59457-146">String</span></span><br/> | <span data-ttu-id="59457-147">Gibt die Anzeige Zeichenfolge für das übergeordnete Element an und überschreibt den Standard anzeigen Amen.</span><span class="sxs-lookup"><span data-stu-id="59457-147">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="59457-148">Kann von printfunktionalitäten-Anbietern verwendet werden, um einen lokalisierten und benutzerfreundlichen anzeigen Amen zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="59457-148">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="59457-149">Der Standardwert für den anzeigen Amen ist das Name-Attribut für das übergeordnete Element.</span><span class="sxs-lookup"><span data-stu-id="59457-149">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="59457-150">Im Fall von Option-Elementen muss die Display Name-Eigenschaft vorhanden sein, wenn das Name-Attribut nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="59457-150">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="59457-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="59457-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59457-152">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="59457-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




