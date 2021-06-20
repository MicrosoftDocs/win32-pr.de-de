---
description: Erfahren Sie mehr über das ParameterInit-Element, das einen Wert für eine Instanz eines ParameterDef-Elements definiert.
ms.assetid: d5419c40-43e9-49ff-a378-9aeb0757e400
title: ParameterInit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e211fcad2c53824c7786850a7fc78c6825c219a7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407263"
---
# <a name="parameterinit"></a><span data-ttu-id="c8a20-103">ParameterInit</span><span class="sxs-lookup"><span data-stu-id="c8a20-103">ParameterInit</span></span>

<span data-ttu-id="c8a20-104">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="c8a20-104">This topic is not current.</span></span> <span data-ttu-id="c8a20-105">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="c8a20-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c8a20-106">Definiert einen Wert für eine Instanz eines ParameterDef-Elements.</span><span class="sxs-lookup"><span data-stu-id="c8a20-106">Defines a value for an instance of a ParameterDef element.</span></span> <span data-ttu-id="c8a20-107">Ein ParameterInit-Element ist das Ziel des Verweises, der von einem ParameterRef-Element vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="c8a20-107">A ParameterInit element is the target of the reference made by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="c8a20-108">Elementtag</span><span class="sxs-lookup"><span data-stu-id="c8a20-108">Element Tag</span></span>

<ParameterInit>

## <a name="xml-attributes"></a><span data-ttu-id="c8a20-109">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="c8a20-109">XML Attributes</span></span>

<span data-ttu-id="c8a20-110">In der folgenden Tabelle sind die XML-Attribute aufgeführt, die für dieses Element gelten können.</span><span class="sxs-lookup"><span data-stu-id="c8a20-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="c8a20-111">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="c8a20-111">XML Attribute</span></span>   | <span data-ttu-id="c8a20-112">Details</span><span class="sxs-lookup"><span data-stu-id="c8a20-112">Details</span></span>                                                                                                                               |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a20-113">name</span><span class="sxs-lookup"><span data-stu-id="c8a20-113">name</span></span><br/> | <span data-ttu-id="c8a20-114">Enthält das Name-Attribut des ParameterDef-Elements, das im Kontext des aktuellen Dokuments initialisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8a20-114">Holds the name attribute of the ParameterDef element that is to be initialized within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="c8a20-115">Weitere Informationen finden Sie im Abschnitt [XML-Attribute.](xml-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="c8a20-115">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="c8a20-116">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="c8a20-116">Element Information</span></span>

<span data-ttu-id="c8a20-117">In der folgenden Tabelle sind die Elemente aufgeführt, die diesem Element unter Umständen über- oder unteren Elementen liegen, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="c8a20-117">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="c8a20-118">Kategorie</span><span class="sxs-lookup"><span data-stu-id="c8a20-118">Category</span></span>                   |                                                                                                   |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8a20-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c8a20-119">Parent elements</span></span><br/> | <span data-ttu-id="c8a20-120">PrintTicket (PrintTicket root)</span><span class="sxs-lookup"><span data-stu-id="c8a20-120">PrintTicket (PrintTicket root)</span></span><br/>                                                         |
| <span data-ttu-id="c8a20-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c8a20-121">Child elements</span></span><br/>  | <span data-ttu-id="c8a20-122">Wert (eins)</span><span class="sxs-lookup"><span data-stu-id="c8a20-122">Value (one)</span></span><br/>                                                                            |
| <span data-ttu-id="c8a20-123">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="c8a20-123">This element</span></span><br/>    | <span data-ttu-id="c8a20-124">Zeichendaten sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="c8a20-124">No character data is permitted.</span></span><br/> <span data-ttu-id="c8a20-125">Doppelte untergeordnete gleichgeordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="c8a20-125">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="c8a20-126">Konfigurationsabhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="c8a20-126">Configuration Dependencies</span></span>

<span data-ttu-id="c8a20-127">Keine</span><span class="sxs-lookup"><span data-stu-id="c8a20-127">None</span></span>

## <a name="example"></a><span data-ttu-id="c8a20-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c8a20-128">Example</span></span>

<span data-ttu-id="c8a20-129">Im folgenden Beispiel wird ein -Parameter mit 1 initialisiert.</span><span class="sxs-lookup"><span data-stu-id="c8a20-129">The following example initializes a parameter to 1.</span></span> <span data-ttu-id="c8a20-130">Im Beispiel in [ParameterDef](parameterdef.md) wird veranschaulicht, wie alle erforderlichen Property-Elemente für diesen Parameter festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c8a20-130">The example in [ParameterDef](parameterdef.md) demonstrates how to set all of the required Property elements for this parameter.</span></span>

``` syntax
<psf:ParameterInit name="psk:PageCopyCount">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
</psf:ParameterInit>
```

## <a name="related-topics"></a><span data-ttu-id="c8a20-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c8a20-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8a20-132">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="c8a20-132">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




