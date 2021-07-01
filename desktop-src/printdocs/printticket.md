---
description: Hier finden Sie Informationen zum PrintTicket-Element. Dieses Thema ist nicht aktuell. Aktuelle Informationen finden Sie unter Print Schema Specification(Spezifikation des Druckschemas).
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b279ff681704a63f6547738c73fb9192d6f8a65d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120075"
---
# <a name="printticket"></a><span data-ttu-id="3f542-105">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="3f542-105">PrintTicket</span></span>

<span data-ttu-id="3f542-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="3f542-106">This topic is not current.</span></span> <span data-ttu-id="3f542-107">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="3f542-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="3f542-108">Ein PrintTicket-Element ist das Stammelement des PrintTicket-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="3f542-108">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="3f542-109">Ein PrintTicket-Element enthält alle Auftragsformatierungsinformationen, die zum Ausgeben eines Auftrags erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3f542-109">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="3f542-110">Elementtag</span><span class="sxs-lookup"><span data-stu-id="3f542-110">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="3f542-111">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="3f542-111">XML Attributes</span></span>

<span data-ttu-id="3f542-112">In der folgenden Tabelle sind die XML-Attribute aufgeführt, die zu diesem Element gehören können.</span><span class="sxs-lookup"><span data-stu-id="3f542-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="3f542-113">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="3f542-113">XML Attribute</span></span>      | <span data-ttu-id="3f542-114">Details</span><span class="sxs-lookup"><span data-stu-id="3f542-114">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f542-115">version</span><span class="sxs-lookup"><span data-stu-id="3f542-115">version</span></span><br/> | <span data-ttu-id="3f542-116">Gibt die Version des Schemas an, das Elementtypen und deren Struktur definiert, ein Literal vom Typ integer.</span><span class="sxs-lookup"><span data-stu-id="3f542-116">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="3f542-117">Die aktuelle Schemaversion ist "1".</span><span class="sxs-lookup"><span data-stu-id="3f542-117">The current schema version is "1".</span></span> <span data-ttu-id="3f542-118">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3f542-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="3f542-119">Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="3f542-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="3f542-120">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="3f542-120">Element Information</span></span>

<span data-ttu-id="3f542-121">In der folgenden Tabelle sind die Elemente aufgeführt, die möglicherweise die untergeordneten Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="3f542-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="3f542-122">Category</span><span class="sxs-lookup"><span data-stu-id="3f542-122">Category</span></span>                   | <span data-ttu-id="3f542-123">Details</span><span class="sxs-lookup"><span data-stu-id="3f542-123">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f542-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f542-124">Parent elements</span></span><br/> | <span data-ttu-id="3f542-125">Nur Dokumentstamm.</span><span class="sxs-lookup"><span data-stu-id="3f542-125">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="3f542-126">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3f542-126">Child elements</span></span><br/>  | <span data-ttu-id="3f542-127">*Feature* (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="3f542-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="3f542-128">*ParameterInit* (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="3f542-128">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="3f542-129">*Eigenschaft* (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="3f542-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="3f542-130">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="3f542-130">This element</span></span><br/>    | <span data-ttu-id="3f542-131">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="3f542-131">No character data is permitted.</span></span><br/> <span data-ttu-id="3f542-132">Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="3f542-132">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="3f542-133">Konfigurationsabhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="3f542-133">Configuration Dependencies</span></span>

<span data-ttu-id="3f542-134">Konfigurationsabhängigkeiten gelten nur für Elemente in einem PrintCapabilities-Dokument.</span><span class="sxs-lookup"><span data-stu-id="3f542-134">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="3f542-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3f542-135">Example</span></span>

<span data-ttu-id="3f542-136">Siehe [PrintTicket-Beispiel.](printticket-example.md)</span><span class="sxs-lookup"><span data-stu-id="3f542-136">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f542-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3f542-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f542-138">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="3f542-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




