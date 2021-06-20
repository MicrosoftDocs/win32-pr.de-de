---
description: Erfahren Sie mehr über das PrintCapabilities-Element, das den Stamm des PrintCapabilities-Dokuments darstellt.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2158fd651849df2e4ea24c640065f1041569741a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407023"
---
# <a name="printcapabilities"></a><span data-ttu-id="22ccb-103">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="22ccb-103">PrintCapabilities</span></span>

<span data-ttu-id="22ccb-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="22ccb-104">This topic is not current.</span></span> <span data-ttu-id="22ccb-105">Die aktuellsten Informationen finden Sie unter Print Schema Specification (Spezifikation des [Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="22ccb-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="22ccb-106">Ein PrintCapabilities-Element stellt den Stamm des PrintCapabilities-Dokuments dar.</span><span class="sxs-lookup"><span data-stu-id="22ccb-106">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="22ccb-107">Das PrintCapabilities-Dokument enthält alle Informationen, die zur Beschreibung der unterstützten Geräteattribute bei einer bestimmten Gerätekonfiguration erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="22ccb-107">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="22ccb-108">Elementtag</span><span class="sxs-lookup"><span data-stu-id="22ccb-108">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="22ccb-109">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="22ccb-109">XML Attributes</span></span>

<span data-ttu-id="22ccb-110">In der folgenden Tabelle sind die XML-Attribute aufgeführt, die zu diesem Element gehören können.</span><span class="sxs-lookup"><span data-stu-id="22ccb-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="22ccb-111">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="22ccb-111">XML Attribute</span></span>      | <span data-ttu-id="22ccb-112">Details</span><span class="sxs-lookup"><span data-stu-id="22ccb-112">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22ccb-113">version</span><span class="sxs-lookup"><span data-stu-id="22ccb-113">version</span></span><br/> | <span data-ttu-id="22ccb-114">Gibt die Version des Schemas an, das Elementtypen und deren Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="22ccb-114">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="22ccb-115">Das Versionsattribut ist vom Typ integer.</span><span class="sxs-lookup"><span data-stu-id="22ccb-115">The version attribute is of type integer.</span></span> <span data-ttu-id="22ccb-116">Die aktuelle Schemaversion wird als "1" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="22ccb-116">The current schema version is designated "1".</span></span> <span data-ttu-id="22ccb-117">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="22ccb-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="22ccb-118">Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="22ccb-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="22ccb-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="22ccb-119">Element Information</span></span>

<span data-ttu-id="22ccb-120">In der folgenden Tabelle sind die Elemente aufgeführt, die möglicherweise die untergeordneten Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="22ccb-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="22ccb-121">Category</span><span class="sxs-lookup"><span data-stu-id="22ccb-121">Category</span></span>                   | <span data-ttu-id="22ccb-122">Details</span><span class="sxs-lookup"><span data-stu-id="22ccb-122">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22ccb-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="22ccb-123">Parent elements</span></span><br/> | <span data-ttu-id="22ccb-124">Nur Dokumentstamm.</span><span class="sxs-lookup"><span data-stu-id="22ccb-124">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="22ccb-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="22ccb-125">Child elements</span></span><br/>  | <span data-ttu-id="22ccb-126">*Feature* (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="22ccb-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="22ccb-127">*ParameterDef* (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="22ccb-127">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="22ccb-128">*Eigenschaft* (null oder mehr)</span><span class="sxs-lookup"><span data-stu-id="22ccb-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="22ccb-129">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="22ccb-129">This element</span></span><br/>    | <span data-ttu-id="22ccb-130">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="22ccb-130">No character data is permitted.</span></span><br/> <span data-ttu-id="22ccb-131">Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="22ccb-131">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="22ccb-132">Konfigurationsabhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="22ccb-132">Configuration Dependencies</span></span>

<span data-ttu-id="22ccb-133">Das Stammelement hat möglicherweise keine Konfigurationsabhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="22ccb-133">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="22ccb-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="22ccb-134">Example</span></span>

<span data-ttu-id="22ccb-135">Weitere Informationen finden Sie im [PrintCapabilities-Dokumentbeispiel.](printcapabilities-document-example.md)</span><span class="sxs-lookup"><span data-stu-id="22ccb-135">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="22ccb-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="22ccb-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22ccb-137">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="22ccb-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




