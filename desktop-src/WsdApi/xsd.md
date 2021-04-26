---
description: Gibt eine XSD-Datei an, die für Vertragsinformationen zu verarbeiten ist.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: xsd-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851ce31230ff88ea2465040c33dc131e0902392c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994547"
---
# <a name="xsd-element"></a><span data-ttu-id="0aee9-103">xsd-Element</span><span class="sxs-lookup"><span data-stu-id="0aee9-103">xsd element</span></span>

<span data-ttu-id="0aee9-104">Gibt eine XSD-Datei an, die für Vertragsinformationen zu verarbeiten ist.</span><span class="sxs-lookup"><span data-stu-id="0aee9-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="0aee9-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="0aee9-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="0aee9-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="0aee9-106">Attributes</span></span>



| <span data-ttu-id="0aee9-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="0aee9-107">Attribute</span></span>           | <span data-ttu-id="0aee9-108">type</span><span class="sxs-lookup"><span data-stu-id="0aee9-108">Type</span></span>                       | <span data-ttu-id="0aee9-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0aee9-109">Required</span></span>       | <span data-ttu-id="0aee9-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aee9-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="0aee9-111">**path**</span><span class="sxs-lookup"><span data-stu-id="0aee9-111">**path**</span></span><br/> | <span data-ttu-id="0aee9-112">pathname string</span><span class="sxs-lookup"><span data-stu-id="0aee9-112">pathname string</span></span><br/> | <span data-ttu-id="0aee9-113">Ja</span><span class="sxs-lookup"><span data-stu-id="0aee9-113">Yes</span></span><br/> | <span data-ttu-id="0aee9-114">Datei und Pfad der XSD-Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="0aee9-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="0aee9-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0aee9-115">Child elements</span></span>



| <span data-ttu-id="0aee9-116">Element</span><span class="sxs-lookup"><span data-stu-id="0aee9-116">Element</span></span>                               | <span data-ttu-id="0aee9-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aee9-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="0aee9-118">**typeUri**</span><span class="sxs-lookup"><span data-stu-id="0aee9-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="0aee9-119">Gibt einen Typ an, der aus einer XSD-Datei enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="0aee9-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="0aee9-120">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="0aee9-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="0aee9-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0aee9-121">Parent elements</span></span>



| <span data-ttu-id="0aee9-122">Element</span><span class="sxs-lookup"><span data-stu-id="0aee9-122">Element</span></span>                                     | <span data-ttu-id="0aee9-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0aee9-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0aee9-124">**wsdCodeGen**</span><span class="sxs-lookup"><span data-stu-id="0aee9-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="0aee9-125">Das Stammelement einer XML-Skriptdatei des WSDAPI-Codegenerators.</span><span class="sxs-lookup"><span data-stu-id="0aee9-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0aee9-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0aee9-126">Remarks</span></span>

<span data-ttu-id="0aee9-127">Die Dateinamenzeichenfolge sollte auch vollständige Pfadinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0aee9-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="0aee9-128">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0aee9-128">Element information</span></span>



| <span data-ttu-id="0aee9-129">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="0aee9-129">Label</span></span> | <span data-ttu-id="0aee9-130">Wert</span><span class="sxs-lookup"><span data-stu-id="0aee9-130">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="0aee9-131">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="0aee9-131">Minimum supported system</span></span><br/> | <span data-ttu-id="0aee9-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0aee9-132">Windows Vista</span></span> |
| <span data-ttu-id="0aee9-133">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="0aee9-133">Can be empty</span></span>                        | <span data-ttu-id="0aee9-134">Ja</span><span class="sxs-lookup"><span data-stu-id="0aee9-134">Yes</span></span>           |



 

 




