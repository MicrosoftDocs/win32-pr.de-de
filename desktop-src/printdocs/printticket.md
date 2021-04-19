---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d2e225eb38584e290db55c33594be80d0d7999
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106370363"
---
# <a name="printticket"></a><span data-ttu-id="6be1f-104">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="6be1f-104">PrintTicket</span></span>

<span data-ttu-id="6be1f-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="6be1f-105">This topic is not current.</span></span> <span data-ttu-id="6be1f-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6be1f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6be1f-107">Ein PrintTicket-Element ist das Stamm Element des PrintTicket-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="6be1f-107">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="6be1f-108">Ein PrintTicket-Element enthält alle Auftrags Formatierungsinformationen, die für die Ausgabe eines Auftrags erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6be1f-108">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="6be1f-109">Elementtag</span><span class="sxs-lookup"><span data-stu-id="6be1f-109">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="6be1f-110">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="6be1f-110">XML Attributes</span></span>

<span data-ttu-id="6be1f-111">In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.</span><span class="sxs-lookup"><span data-stu-id="6be1f-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="6be1f-112">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="6be1f-112">XML Attribute</span></span>      | <span data-ttu-id="6be1f-113">Details</span><span class="sxs-lookup"><span data-stu-id="6be1f-113">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6be1f-114">version</span><span class="sxs-lookup"><span data-stu-id="6be1f-114">version</span></span><br/> | <span data-ttu-id="6be1f-115">Gibt die Version des Schemas an, das Elementtypen und deren Struktur definiert, ein Literaltyp vom Typ Integer.</span><span class="sxs-lookup"><span data-stu-id="6be1f-115">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="6be1f-116">Die aktuelle Schema Version ist "1".</span><span class="sxs-lookup"><span data-stu-id="6be1f-116">The current schema version is "1".</span></span> <span data-ttu-id="6be1f-117">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6be1f-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="6be1f-118">Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="6be1f-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="6be1f-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="6be1f-119">Element Information</span></span>

<span data-ttu-id="6be1f-120">In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="6be1f-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="6be1f-121">Category</span><span class="sxs-lookup"><span data-stu-id="6be1f-121">Category</span></span>                   | <span data-ttu-id="6be1f-122">Details</span><span class="sxs-lookup"><span data-stu-id="6be1f-122">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6be1f-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6be1f-123">Parent elements</span></span><br/> | <span data-ttu-id="6be1f-124">Nur Dokument Stamm.</span><span class="sxs-lookup"><span data-stu-id="6be1f-124">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="6be1f-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6be1f-125">Child elements</span></span><br/>  | <span data-ttu-id="6be1f-126">*Feature* (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="6be1f-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="6be1f-127">*Parameterinit* (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="6be1f-127">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="6be1f-128">*Property* (0 (null) oder mehr)</span><span class="sxs-lookup"><span data-stu-id="6be1f-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="6be1f-129">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="6be1f-129">This element</span></span><br/>    | <span data-ttu-id="6be1f-130">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="6be1f-130">No character data is permitted.</span></span><br/> <span data-ttu-id="6be1f-131">Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="6be1f-131">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="6be1f-132">Konfigurations Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="6be1f-132">Configuration Dependencies</span></span>

<span data-ttu-id="6be1f-133">Konfigurations Abhängigkeiten gelten nur für Elemente in einem printfunktionalitäten-Dokument.</span><span class="sxs-lookup"><span data-stu-id="6be1f-133">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="6be1f-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6be1f-134">Example</span></span>

<span data-ttu-id="6be1f-135">Siehe [PrintTicket-Beispiel](printticket-example.md).</span><span class="sxs-lookup"><span data-stu-id="6be1f-135">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6be1f-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6be1f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6be1f-137">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="6be1f-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




