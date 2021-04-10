---
description: Gibt eine XSD-Datei an, die für Vertragsinformationen verarbeitet werden soll.
ms.assetid: 6fe40e77-d23f-4ae9-a4d6-1f567a0fffe7
title: XSD-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9628a078129446f51729c92c447f8da5736dab88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865336"
---
# <a name="xsd-element"></a><span data-ttu-id="0b7f1-103">XSD-Element</span><span class="sxs-lookup"><span data-stu-id="0b7f1-103">xsd element</span></span>

<span data-ttu-id="0b7f1-104">Gibt eine XSD-Datei an, die für Vertragsinformationen verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-104">Specifies an XSD file to process for contract information.</span></span>

## <a name="usage"></a><span data-ttu-id="0b7f1-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="0b7f1-105">Usage</span></span>

``` syntax
<xsd
  path = "pathname string">
  child elements
</xsd>
```

## <a name="attributes"></a><span data-ttu-id="0b7f1-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="0b7f1-106">Attributes</span></span>



| <span data-ttu-id="0b7f1-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="0b7f1-107">Attribute</span></span>           | <span data-ttu-id="0b7f1-108">type</span><span class="sxs-lookup"><span data-stu-id="0b7f1-108">Type</span></span>                       | <span data-ttu-id="0b7f1-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0b7f1-109">Required</span></span>       | <span data-ttu-id="0b7f1-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b7f1-110">Description</span></span>                                                 |
|---------------------|----------------------------|----------------|-------------------------------------------------------------|
| <span data-ttu-id="0b7f1-111">**path**</span><span class="sxs-lookup"><span data-stu-id="0b7f1-111">**path**</span></span><br/> | <span data-ttu-id="0b7f1-112">Pfadnamen-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="0b7f1-112">pathname string</span></span><br/> | <span data-ttu-id="0b7f1-113">Ja</span><span class="sxs-lookup"><span data-stu-id="0b7f1-113">Yes</span></span><br/> | <span data-ttu-id="0b7f1-114">Die Datei und der Pfad der XSD-Eingabedatei.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-114">File and path of the XSD input file.</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="0b7f1-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b7f1-115">Child elements</span></span>



| <span data-ttu-id="0b7f1-116">Element</span><span class="sxs-lookup"><span data-stu-id="0b7f1-116">Element</span></span>                               | <span data-ttu-id="0b7f1-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b7f1-117">Description</span></span>                                                          |
|---------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="0b7f1-118">**TypeUri**</span><span class="sxs-lookup"><span data-stu-id="0b7f1-118">**typeUri**</span></span>](typeuri.md)<br/> | <span data-ttu-id="0b7f1-119">Gibt einen Typ an, der aus einer XSD-Datei aufgenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-119">Specifies a type to include from an XSD file.</span></span><br/> <br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="0b7f1-120">Sequenz untergeordneter Elemente</span><span class="sxs-lookup"><span data-stu-id="0b7f1-120">Child element sequence</span></span>

``` syntax
typeUri*
```

## <a name="parent-elements"></a><span data-ttu-id="0b7f1-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b7f1-121">Parent elements</span></span>



| <span data-ttu-id="0b7f1-122">Element</span><span class="sxs-lookup"><span data-stu-id="0b7f1-122">Element</span></span>                                     | <span data-ttu-id="0b7f1-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0b7f1-123">Description</span></span>                                                                          |
|---------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b7f1-124">**wsdcodegen**</span><span class="sxs-lookup"><span data-stu-id="0b7f1-124">**wsdCodeGen**</span></span>](wsdcodegen.md)<br/> | <span data-ttu-id="0b7f1-125">Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-125">The root element of an WSDAPI code generator XML script file.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0b7f1-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0b7f1-126">Remarks</span></span>

<span data-ttu-id="0b7f1-127">Die Dateinamen Zeichenfolge sollte auch Informationen zum kompletten Pfad enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-127">The filename string should include complete path information as well.</span></span>

## <a name="element-information"></a><span data-ttu-id="0b7f1-128">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="0b7f1-128">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="0b7f1-129">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="0b7f1-129">Minimum supported system</span></span><br/> | <span data-ttu-id="0b7f1-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b7f1-130">Windows Vista</span></span> |
| <span data-ttu-id="0b7f1-131">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="0b7f1-131">Can be empty</span></span>                        | <span data-ttu-id="0b7f1-132">Ja</span><span class="sxs-lookup"><span data-stu-id="0b7f1-132">Yes</span></span>           |



 

 




