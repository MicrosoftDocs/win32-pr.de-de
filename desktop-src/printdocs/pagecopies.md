---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: a15fe075-6696-4c70-b658-ae62d542bb4e
title: Pagekopien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6feef0745e3f9a86b3697b7e0ab65111fc3dfcb
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219065"
---
# <a name="pagecopies"></a><span data-ttu-id="ad1ad-104">Pagekopien</span><span class="sxs-lookup"><span data-stu-id="ad1ad-104">PageCopies</span></span>

<span data-ttu-id="ad1ad-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="ad1ad-105">This topic is not current.</span></span> <span data-ttu-id="ad1ad-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ad1ad-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ad1ad-107">Gibt die Anzahl der Kopien einer Seite an.</span><span class="sxs-lookup"><span data-stu-id="ad1ad-107">Specifies the number of copies of a page.</span></span>

-   [<span data-ttu-id="ad1ad-108">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ad1ad-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ad1ad-109">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ad1ad-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ad1ad-110">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="ad1ad-110">Element Information</span></span>



| <span data-ttu-id="ad1ad-111">Name</span><span class="sxs-lookup"><span data-stu-id="ad1ad-111">Name</span></span>                       |                         |
|----------------------------|-------------------------|
| <span data-ttu-id="ad1ad-112">Elementtyp</span><span class="sxs-lookup"><span data-stu-id="ad1ad-112">Element Type</span></span> <br/>   | <span data-ttu-id="ad1ad-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ad1ad-113">ParameterDef</span></span><br/> |
| <span data-ttu-id="ad1ad-114">Bereichs Präfix</span><span class="sxs-lookup"><span data-stu-id="ad1ad-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ad1ad-115">Seite</span><span class="sxs-lookup"><span data-stu-id="ad1ad-115">Page</span></span><br/>         |
| <span data-ttu-id="ad1ad-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad1ad-116">Notes</span></span> <br/>          | <span data-ttu-id="ad1ad-117">Keine</span><span class="sxs-lookup"><span data-stu-id="ad1ad-117">None</span></span><br/>         |



 

## <a name="structure-content"></a><span data-ttu-id="ad1ad-118">Strukturieren von Inhalt</span><span class="sxs-lookup"><span data-stu-id="ad1ad-118">Structure Content</span></span>

<span data-ttu-id="ad1ad-119">Die XML-Struktur dieses Elements lautet:</span><span class="sxs-lookup"><span data-stu-id="ad1ad-119">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageCopies">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Unconditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">copies</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="ad1ad-120">Struktur Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ad1ad-120">Structure Properties</span></span>

<span data-ttu-id="ad1ad-121">In der folgenden Tabelle werden die Merkmale der Variablen beschrieben, die in der XML-Struktur definiert sind.</span><span class="sxs-lookup"><span data-stu-id="ad1ad-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ad1ad-122">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ad1ad-122">Property</span></span>                | <span data-ttu-id="ad1ad-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ad1ad-123">xsi:type</span></span>           | <span data-ttu-id="ad1ad-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ad1ad-124">Value</span></span>                        |
|-------------------------|--------------------|------------------------------|
| <span data-ttu-id="ad1ad-125">DataType</span><span class="sxs-lookup"><span data-stu-id="ad1ad-125">DataType</span></span><br/>     | <span data-ttu-id="ad1ad-126">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad1ad-126">string</span></span><br/>  | <span data-ttu-id="ad1ad-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ad1ad-127">xs:integer</span></span><br/>        |
| <span data-ttu-id="ad1ad-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ad1ad-128">DefaultValue</span></span><br/> | <span data-ttu-id="ad1ad-129">integer</span><span class="sxs-lookup"><span data-stu-id="ad1ad-129">integer</span></span><br/> | <span data-ttu-id="ad1ad-130">1</span><span class="sxs-lookup"><span data-stu-id="ad1ad-130">1</span></span><br/>                 |
| <span data-ttu-id="ad1ad-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ad1ad-131">MaxValue</span></span><br/>     | <span data-ttu-id="ad1ad-132">integer</span><span class="sxs-lookup"><span data-stu-id="ad1ad-132">integer</span></span><br/> | <span data-ttu-id="ad1ad-133">nicht definiert</span><span class="sxs-lookup"><span data-stu-id="ad1ad-133">undefined</span></span><br/>         |
| <span data-ttu-id="ad1ad-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="ad1ad-134">MinValue</span></span><br/>     | <span data-ttu-id="ad1ad-135">integer</span><span class="sxs-lookup"><span data-stu-id="ad1ad-135">integer</span></span><br/> | <span data-ttu-id="ad1ad-136">1</span><span class="sxs-lookup"><span data-stu-id="ad1ad-136">1</span></span><br/>                 |
| <span data-ttu-id="ad1ad-137">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="ad1ad-137">Mandatory</span></span><br/>    | <span data-ttu-id="ad1ad-138">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad1ad-138">string</span></span><br/>  | <span data-ttu-id="ad1ad-139">PSK: nicht bedingt</span><span class="sxs-lookup"><span data-stu-id="ad1ad-139">psk:Unconditional</span></span><br/> |
| <span data-ttu-id="ad1ad-140">Mehrere</span><span class="sxs-lookup"><span data-stu-id="ad1ad-140">Multiple</span></span><br/>     | <span data-ttu-id="ad1ad-141">integer</span><span class="sxs-lookup"><span data-stu-id="ad1ad-141">integer</span></span><br/> | <span data-ttu-id="ad1ad-142">1</span><span class="sxs-lookup"><span data-stu-id="ad1ad-142">1</span></span><br/>                 |
| <span data-ttu-id="ad1ad-143">UnitType</span><span class="sxs-lookup"><span data-stu-id="ad1ad-143">UnitType</span></span><br/>     | <span data-ttu-id="ad1ad-144">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="ad1ad-144">string</span></span><br/>  | <span data-ttu-id="ad1ad-145">Uni</span><span class="sxs-lookup"><span data-stu-id="ad1ad-145">copies</span></span><br/>            |



 

## <a name="related-topics"></a><span data-ttu-id="ad1ad-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ad1ad-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad1ad-147">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="ad1ad-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




