---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c6dd8ce98b071f1eb239762544a9b72160035
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355117"
---
# <a name="printcapabilities"></a><span data-ttu-id="e26c0-104">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="e26c0-104">PrintCapabilities</span></span>

<span data-ttu-id="e26c0-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="e26c0-105">This topic is not current.</span></span> <span data-ttu-id="e26c0-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e26c0-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e26c0-107">Ein printfunktionen-Element stellt den Stamm des printfunktionalitäten-Dokuments dar.</span><span class="sxs-lookup"><span data-stu-id="e26c0-107">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="e26c0-108">Das Dokument printfunktionen enthält alle Informationen, die zum Beschreiben der unterstützten Geräte Attribute erforderlich sind, wenn eine bestimmte Gerätekonfiguration erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e26c0-108">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="e26c0-109">Elementtag</span><span class="sxs-lookup"><span data-stu-id="e26c0-109">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="e26c0-110">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="e26c0-110">XML Attributes</span></span>

<span data-ttu-id="e26c0-111">In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.</span><span class="sxs-lookup"><span data-stu-id="e26c0-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="e26c0-112">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="e26c0-112">XML Attribute</span></span>      | <span data-ttu-id="e26c0-113">Details</span><span class="sxs-lookup"><span data-stu-id="e26c0-113">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e26c0-114">version</span><span class="sxs-lookup"><span data-stu-id="e26c0-114">version</span></span><br/> | <span data-ttu-id="e26c0-115">Gibt die Version des Schemas an, das Elementtypen und deren Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="e26c0-115">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="e26c0-116">Das Versions Attribut ist vom Typ Integer.</span><span class="sxs-lookup"><span data-stu-id="e26c0-116">The version attribute is of type integer.</span></span> <span data-ttu-id="e26c0-117">Die aktuelle Schema Version ist "1".</span><span class="sxs-lookup"><span data-stu-id="e26c0-117">The current schema version is designated "1".</span></span> <span data-ttu-id="e26c0-118">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e26c0-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="e26c0-119">Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="e26c0-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="e26c0-120">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="e26c0-120">Element Information</span></span>

<span data-ttu-id="e26c0-121">In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="e26c0-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="e26c0-122">Category</span><span class="sxs-lookup"><span data-stu-id="e26c0-122">Category</span></span>                   | <span data-ttu-id="e26c0-123">Details</span><span class="sxs-lookup"><span data-stu-id="e26c0-123">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e26c0-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e26c0-124">Parent elements</span></span><br/> | <span data-ttu-id="e26c0-125">Nur Dokument Stamm.</span><span class="sxs-lookup"><span data-stu-id="e26c0-125">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="e26c0-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e26c0-126">Child elements</span></span><br/>  | <span data-ttu-id="e26c0-127">*Feature* (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="e26c0-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="e26c0-128">*ParameterDef* (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="e26c0-128">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="e26c0-129">*Property* (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="e26c0-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="e26c0-130">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="e26c0-130">This element</span></span><br/>    | <span data-ttu-id="e26c0-131">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="e26c0-131">No character data is permitted.</span></span><br/> <span data-ttu-id="e26c0-132">Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="e26c0-132">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="e26c0-133">Konfigurations Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="e26c0-133">Configuration Dependencies</span></span>

<span data-ttu-id="e26c0-134">Das root-Element weist möglicherweise keine Konfigurations Abhängigkeiten auf.</span><span class="sxs-lookup"><span data-stu-id="e26c0-134">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="e26c0-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e26c0-135">Example</span></span>

<span data-ttu-id="e26c0-136">Weitere Informationen finden Sie unter [Beispiel für printfunktionen](printcapabilities-document-example.md).</span><span class="sxs-lookup"><span data-stu-id="e26c0-136">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e26c0-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e26c0-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e26c0-138">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="e26c0-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




