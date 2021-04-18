---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: feda78d9-58e7-4668-8a25-40e5fd8ad456
title: Option
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 379834d12cd01847c95783d727be5dcdc6c575bf
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354293"
---
# <a name="option"></a><span data-ttu-id="253dd-104">Option</span><span class="sxs-lookup"><span data-stu-id="253dd-104">Option</span></span>

<span data-ttu-id="253dd-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="253dd-105">This topic is not current.</span></span> <span data-ttu-id="253dd-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="253dd-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="253dd-107">Ein Option-Element enthält alle Eigenschaften-und ScoredProperty-Elemente, die dieser Option zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="253dd-107">An Option element contains all of the Property and ScoredProperty elements associated with this option.</span></span>

## <a name="element-tag"></a><span data-ttu-id="253dd-108">Elementtag</span><span class="sxs-lookup"><span data-stu-id="253dd-108">Element Tag</span></span>

<Option>

## <a name="xml-attributes"></a><span data-ttu-id="253dd-109">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="253dd-109">XML Attributes</span></span>

<span data-ttu-id="253dd-110">In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.</span><span class="sxs-lookup"><span data-stu-id="253dd-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="253dd-111">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="253dd-111">XML Attribute</span></span>          | <span data-ttu-id="253dd-112">Details</span><span class="sxs-lookup"><span data-stu-id="253dd-112">Details</span></span>                                                                                                                                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="253dd-113">schwierige</span><span class="sxs-lookup"><span data-stu-id="253dd-113">constrained</span></span><br/> | <span data-ttu-id="253dd-114">Dieses Attribut ist für ein printfunktionalitäten-Dokument optional.</span><span class="sxs-lookup"><span data-stu-id="253dd-114">This attribute is optional for a PrintCapabilities document.</span></span><br/> <span data-ttu-id="253dd-115">Dieses Attribut gibt an, ob die Option zur Auswahl oder Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="253dd-115">This attribute indicates whether the Option is available for selection or use.</span></span> <span data-ttu-id="253dd-116">Dieses XML-Attribut kann auf einen der folgenden Werte festgelegt werden: None, printticketsettings, adminsetting oder devicesettings.</span><span class="sxs-lookup"><span data-stu-id="253dd-116">This XML attribute can be set to one of the following values: None, PrintTicketSettings, AdminSetting or DeviceSettings.</span></span> <br/> <span data-ttu-id="253dd-117">Siehe [XML-Attribute](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="253dd-117">See [XML Attributes](xml-attributes.md)</span></span><br/> |
| <span data-ttu-id="253dd-118">name</span><span class="sxs-lookup"><span data-stu-id="253dd-118">name</span></span><br/>        | <span data-ttu-id="253dd-119">Enthält den Namen der Option, entweder eine Standardoption oder eine privat definierte Option.</span><span class="sxs-lookup"><span data-stu-id="253dd-119">Holds the name of the Option, either a standard Option or a privately-defined Option.</span></span> <span data-ttu-id="253dd-120">Das XML-Attribut wird auf diese Weise verwendet, um zwischen Options Instanzen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="253dd-120">The XML attribute is used this way in order to differentiate between Option instances.</span></span> <br/>                                                                                                                                                        |



 

<span data-ttu-id="253dd-121">Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="253dd-121">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="253dd-122">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="253dd-122">Element Information</span></span>

<span data-ttu-id="253dd-123">In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="253dd-123">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="253dd-124">Category</span><span class="sxs-lookup"><span data-stu-id="253dd-124">Category</span></span>                   | <span data-ttu-id="253dd-125">Details</span><span class="sxs-lookup"><span data-stu-id="253dd-125">Details</span></span>                                                                                                                                                                                                                                                                                          |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="253dd-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="253dd-126">Parent elements</span></span><br/> | <span data-ttu-id="253dd-127">Funktion</span><span class="sxs-lookup"><span data-stu-id="253dd-127">Feature</span></span> <br/>                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="253dd-128">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="253dd-128">Child elements</span></span><br/>  | <span data-ttu-id="253dd-129">*Property* (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="253dd-129">*Property* (zero or more)</span></span><br/> <span data-ttu-id="253dd-130">*ScoredProperty* (0 (null) oder mehr für Optionen mit dem XML-Attribut ' Name '; mindestens eine for-Option, die das XML-Attribut ' Name ' nicht nutzt \* )</span><span class="sxs-lookup"><span data-stu-id="253dd-130">*ScoredProperty* (zero or more for Options with XML Attribute 'name'; one or more for Options not utilizing XML Attribute 'name'\*)</span></span><br/> <span data-ttu-id="253dd-131">\* nur öffentliche Optionen, die im Druck Schema definiert sind, dürfen kein "Name"-Attribut haben, z. b. "DocumentNUp"</span><span class="sxs-lookup"><span data-stu-id="253dd-131">\* only public Options defined in Print Schema can have no 'name' attribute, such as DocumentNUp)</span></span><br/> |
| <span data-ttu-id="253dd-132">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="253dd-132">This element</span></span><br/>    | <span data-ttu-id="253dd-133">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="253dd-133">No character data is permitted.</span></span><br/> <span data-ttu-id="253dd-134">Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="253dd-134">Duplicate child siblings are not permitted.</span></span><br/>                                                                                                                                                                                                |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="253dd-135">Konfigurations Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="253dd-135">Configuration Dependencies</span></span>

<span data-ttu-id="253dd-136">Ein Options Definitions Element weist möglicherweise keine Konfigurations Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="253dd-136">An Option definition element may not have any configuration dependencies.</span></span>

## <a name="element-usage"></a><span data-ttu-id="253dd-137">Element Verwendung</span><span class="sxs-lookup"><span data-stu-id="253dd-137">Element Usage</span></span>

<span data-ttu-id="253dd-138">Der Zweck des Option-Elements besteht darin, einen der Zustände zu bezeichnen, die von einem Geräte Konfigurations Attribut, das von einem Feature-Element dargestellt wird, angenommen werden kann.</span><span class="sxs-lookup"><span data-stu-id="253dd-138">The purpose of the Option element is to characterize one of the states that a device configuration attribute, represented by a Feature element, can assume.</span></span> <span data-ttu-id="253dd-139">Jede Options Element Definition enthält ein oder mehrere ScoredProperty-Elemente, die eine intrinsische oder wesentliche Eigenschaft dieser Option beschreiben.</span><span class="sxs-lookup"><span data-stu-id="253dd-139">Each Option element definition contains one or more ScoredProperty elements that describe an intrinsic or essential characteristic of that Option.</span></span> <span data-ttu-id="253dd-140">Um die Portabilität und die Beibehaltung der Absicht zu vereinfachen, definiert das Druck Schema viele gängige Funktionselemente und eine Vielzahl von Options Elementen für jede Funktion.</span><span class="sxs-lookup"><span data-stu-id="253dd-140">To facilitate portability and preservation of intent, the Print Schema defines many common Feature elements and a variety of Option elements for each Feature.</span></span> <span data-ttu-id="253dd-141">Daher ist es wichtig, dass Sie, wenn überhaupt möglich, Schema definierte Options Elemente verwenden, bevor Sie eigene Options Definitionen erstellen.</span><span class="sxs-lookup"><span data-stu-id="253dd-141">It is therefore important to use Print Schema-defined Option elements, if at all possible, before you create your own Option definitions.</span></span> <span data-ttu-id="253dd-142">Das Verständnis des Prozesses zum Definieren von Options Elementen bietet nützliche Einblicke in die Art und Weise, in der die Printworks-Dokumente und-PrintTickets in der Microsoft .NET Framework-Version 3,0 und Windows Vista-Druck Architektur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="253dd-142">Understanding the process of defining Option elements provides useful insights into the way the PrintCapabilities document and PrintTickets are used in the Microsoft .NET Framework version 3.0 and Windows Vista printing architecture.</span></span>

## <a name="example"></a><span data-ttu-id="253dd-143">Beispiel</span><span class="sxs-lookup"><span data-stu-id="253dd-143">Example</span></span>

<span data-ttu-id="253dd-144">Im folgenden Beispiel wird ein Name für die Option definiert.</span><span class="sxs-lookup"><span data-stu-id="253dd-144">The following example defines a name for the Option.</span></span>

``` syntax
<psf:Option name="psk:PrintFront" />
```

## <a name="related-topics"></a><span data-ttu-id="253dd-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="253dd-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="253dd-146">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="253dd-146">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




