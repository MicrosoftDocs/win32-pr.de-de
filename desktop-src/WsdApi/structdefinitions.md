---
description: Generiert C-Strukturdefinitionen für bekannte Typen.
ms.assetid: 38ba2e8a-d5b1-47b2-b410-ae161f5039bf
title: structDefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f680db18b06253362f932cc7d34d5b85f7c1b5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996457"
---
# <a name="structdefinitions-element"></a><span data-ttu-id="84586-103">structDefinitions-Element</span><span class="sxs-lookup"><span data-stu-id="84586-103">structDefinitions element</span></span>

<span data-ttu-id="84586-104">Generiert C-Strukturdefinitionen für bekannte Typen.</span><span class="sxs-lookup"><span data-stu-id="84586-104">Generates C structure definitions for known types.</span></span>

## <a name="usage"></a><span data-ttu-id="84586-105">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="84586-105">Usage</span></span>

``` syntax
<structDefinitions/>
```

## <a name="attributes"></a><span data-ttu-id="84586-106">Attribute</span><span class="sxs-lookup"><span data-stu-id="84586-106">Attributes</span></span>

<span data-ttu-id="84586-107">Es gibt keine Attribute.</span><span class="sxs-lookup"><span data-stu-id="84586-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="84586-108">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="84586-108">Child elements</span></span>

<span data-ttu-id="84586-109">Es gibt keine untergeordneten Elemente.</span><span class="sxs-lookup"><span data-stu-id="84586-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="84586-110">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="84586-110">Parent elements</span></span>



| <span data-ttu-id="84586-111">Element</span><span class="sxs-lookup"><span data-stu-id="84586-111">Element</span></span>                         | <span data-ttu-id="84586-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84586-112">Description</span></span>                                                    |
|---------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="84586-113">**Datei**</span><span class="sxs-lookup"><span data-stu-id="84586-113">**file**</span></span>](file.md)<br/> | <span data-ttu-id="84586-114">Gibt eine Datei aus dem Codegenerator aus.</span><span class="sxs-lookup"><span data-stu-id="84586-114">Outputs a file from the code generator.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="84586-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="84586-115">Remarks</span></span>

<span data-ttu-id="84586-116">Auf Strukturen für bekannte Typen wird von einem Großteil des generierten Codes und von Anwendungscode verwiesen.</span><span class="sxs-lookup"><span data-stu-id="84586-116">Structures for known types are referenced by much of the generated code and by application code.</span></span> <span data-ttu-id="84586-117">Dieses Element wird verwendet, um Includedateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="84586-117">This element is used to generate include files.</span></span> <span data-ttu-id="84586-118">Dieses Element sollte nach einem [**structDeclarations-Element**](structdeclarations.md) auftreten, damit Verweise zwischen Strukturen ordnungsgemäß behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="84586-118">This element should occur after a [**structDeclarations**](structdeclarations.md) element so that references between structures are handled properly.</span></span>

## <a name="element-information"></a><span data-ttu-id="84586-119">Elementinformationen</span><span class="sxs-lookup"><span data-stu-id="84586-119">Element information</span></span>



| <span data-ttu-id="84586-120">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="84586-120">Label</span></span> | <span data-ttu-id="84586-121">Wert</span><span class="sxs-lookup"><span data-stu-id="84586-121">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="84586-122">Unterstützte Mindestversion (System)</span><span class="sxs-lookup"><span data-stu-id="84586-122">Minimum supported system</span></span><br/> | <span data-ttu-id="84586-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84586-123">Windows Vista</span></span> |
| <span data-ttu-id="84586-124">Kann leer bleiben</span><span class="sxs-lookup"><span data-stu-id="84586-124">Can be empty</span></span>                        | <span data-ttu-id="84586-125">Ja</span><span class="sxs-lookup"><span data-stu-id="84586-125">Yes</span></span>           |



 

 




