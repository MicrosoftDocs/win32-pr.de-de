---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 35e1ccc2-ffc1-47a6-aba8-5a5cb442e8ae
title: ParameterRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2ef6655439718c1038afe2d342910c54db45ba
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354923"
---
# <a name="parameterref"></a><span data-ttu-id="4a43c-104">ParameterRef</span><span class="sxs-lookup"><span data-stu-id="4a43c-104">ParameterRef</span></span>

<span data-ttu-id="4a43c-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="4a43c-105">This topic is not current.</span></span> <span data-ttu-id="4a43c-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4a43c-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4a43c-107">Ein ParameterRef-Element definiert einen Verweis auf ein parameterinit-Element.</span><span class="sxs-lookup"><span data-stu-id="4a43c-107">A ParameterRef element defines a reference to a ParameterInit element.</span></span> <span data-ttu-id="4a43c-108">Ein ScoredProperty-Element, das ein ParameterRef-Element enthält, weist kein explizit festgelegtes Value-Element auf.</span><span class="sxs-lookup"><span data-stu-id="4a43c-108">A ScoredProperty element that contains a ParameterRef element does not have an explicitly-set Value element.</span></span> <span data-ttu-id="4a43c-109">Stattdessen empfängt das ScoredProperty-Element seinen Wert aus dem parameterinit-Element, auf das von einem ParameterRef-Element verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4a43c-109">Instead, the ScoredProperty element receives its value from the ParameterInit element referenced by a ParameterRef element.</span></span>

## <a name="element-tag"></a><span data-ttu-id="4a43c-110">Elementtag</span><span class="sxs-lookup"><span data-stu-id="4a43c-110">Element Tag</span></span>

<ParameterRef>

## <a name="xml-attributes"></a><span data-ttu-id="4a43c-111">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="4a43c-111">XML Attributes</span></span>

<span data-ttu-id="4a43c-112">In der folgenden Tabelle werden die XML-Attribute aufgelistet, die sich möglicherweise auf dieses Element beziehen.</span><span class="sxs-lookup"><span data-stu-id="4a43c-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="4a43c-113">XML-Attribut</span><span class="sxs-lookup"><span data-stu-id="4a43c-113">XML Attribute</span></span>   | <span data-ttu-id="4a43c-114">Details</span><span class="sxs-lookup"><span data-stu-id="4a43c-114">Details</span></span>                                                                                                                        |
|-----------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a43c-115">name</span><span class="sxs-lookup"><span data-stu-id="4a43c-115">name</span></span><br/> | <span data-ttu-id="4a43c-116">Enthält das Name-Attribut des ParameterDef-Elements, auf das innerhalb des Kontexts des aktuellen Dokuments verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="4a43c-116">Holds the name attribute of the ParameterDef element that is referenced within the context of the current document.</span></span><br/> |



 

<span data-ttu-id="4a43c-117">Weitere Informationen finden Sie im Abschnitt [XML-Attribute](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="4a43c-117">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="4a43c-118">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="4a43c-118">Element Information</span></span>

<span data-ttu-id="4a43c-119">In der folgenden Tabelle werden die Elemente aufgelistet, die übergeordnete Elemente dieses Elements sein können, die Elemente, die möglicherweise untergeordnete Elemente dieses Elements sind, sowie alle Einschränkungen für das Element selbst.</span><span class="sxs-lookup"><span data-stu-id="4a43c-119">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="4a43c-120">Category</span><span class="sxs-lookup"><span data-stu-id="4a43c-120">Category</span></span>                   | <span data-ttu-id="4a43c-121">Details</span><span class="sxs-lookup"><span data-stu-id="4a43c-121">Details</span></span>                                                                                           |
|----------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a43c-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4a43c-122">Parent elements</span></span><br/> | <span data-ttu-id="4a43c-123">ScoredProperty</span><span class="sxs-lookup"><span data-stu-id="4a43c-123">ScoredProperty</span></span> <br/>                                                                        |
| <span data-ttu-id="4a43c-124">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4a43c-124">Child elements</span></span><br/>  | <span data-ttu-id="4a43c-125">Keine zulässig.</span><span class="sxs-lookup"><span data-stu-id="4a43c-125">None permitted.</span></span><br/>                                                                        |
| <span data-ttu-id="4a43c-126">Dieses Element</span><span class="sxs-lookup"><span data-stu-id="4a43c-126">This element</span></span><br/>    | <span data-ttu-id="4a43c-127">Es sind keine Zeichendaten zulässig.</span><span class="sxs-lookup"><span data-stu-id="4a43c-127">No character data is permitted.</span></span><br/> <span data-ttu-id="4a43c-128">Doppelte untergeordnete gleich geordnete Elemente sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="4a43c-128">Duplicate child siblings are not permitted.</span></span><br/> |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="4a43c-129">Konfigurations Abhängigkeiten</span><span class="sxs-lookup"><span data-stu-id="4a43c-129">Configuration Dependencies</span></span>

<span data-ttu-id="4a43c-130">ParameterRef-Elemente haben möglicherweise keine Konfigurations Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="4a43c-130">ParameterRef elements may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="4a43c-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4a43c-131">Example</span></span>

<span data-ttu-id="4a43c-132">Im folgenden Beispiel wird veranschaulicht, wie Sie ParameterRef-Elemente verwenden, um Benutzern die Eingabe von benutzerdefinierten Mediengrößen Parametern zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="4a43c-132">The following example illustrates how to use ParameterRef elements to enable users to enter custom media size parameters.</span></span>

``` syntax
<psf:Option name="psk:CustomMediaSize" constrained="psk:None">
  <psf:ScoredProperty name="psk:MediaSizeWidth">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeWidth" />
  </psf:ScoredProperty>
  <psf:ScoredProperty name="psk:MediaSizeHeight">
    <psf:ParameterRef name="psk:PageMediaSizeMediaSizeHeight" />
  </psf:ScoredProperty>
  <psf:Property name="psk:DisplayName">
    <psf:Value xsi:type="xs:string">Fabrikam User Custom</psf:Value>
  </psf:Property>
</psf:Option>
```

## <a name="related-topics"></a><span data-ttu-id="4a43c-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a43c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a43c-134">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="4a43c-134">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




