---
title: 'Texture2DMS:: Operator-Funktion'
description: Ruft einen Wert aus der Ressource an dem Speicherort ab, der im Beispiel Index 0 angegeben ist.
ms.assetid: 80380D3F-1E71-4C43-A17B-F94F6E5215B1
keywords:
- Operator Function HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6ae7976e6871dc2547ed5c372e1551e5bf0ca148
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104976960"
---
# <a name="texture2dmsoperator--function"></a><span data-ttu-id="a5870-104">Texture2DMS:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="a5870-104">Texture2DMS::Operator  function</span></span>

<span data-ttu-id="a5870-105">Ruft einen Wert aus der Ressource an dem Speicherort ab, der im Beispiel Index 0 angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a5870-105">Retrieves a value from the resource at the location provided at sample index 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5870-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5870-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="a5870-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5870-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5870-108">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5870-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5870-109">Typ: **uint2**</span><span class="sxs-lookup"><span data-stu-id="a5870-109">Type: **uint2**</span></span>

<span data-ttu-id="a5870-110">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="a5870-110">The index position.</span></span> <span data-ttu-id="a5870-111">Enthält die (x, y)-Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="a5870-111">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5870-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5870-112">Return value</span></span>

<span data-ttu-id="a5870-113">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="a5870-113">Type: **R**</span></span>

<span data-ttu-id="a5870-114">Eine schreibgeschützte Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="a5870-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5870-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5870-115">Remarks</span></span>

<span data-ttu-id="a5870-116">Informationen zum Auswählen eines bestimmten Beispiels finden Sie im [**Beispiel. \[Operator \] . \[ \]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="a5870-116">To select a particular sample, refer to [**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md).</span></span>

<span data-ttu-id="a5870-117">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a5870-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a5870-118">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="a5870-118">Vertex</span></span> | <span data-ttu-id="a5870-119">Hülle</span><span class="sxs-lookup"><span data-stu-id="a5870-119">Hull</span></span> | <span data-ttu-id="a5870-120">Domain</span><span class="sxs-lookup"><span data-stu-id="a5870-120">Domain</span></span> | <span data-ttu-id="a5870-121">Geometrie</span><span class="sxs-lookup"><span data-stu-id="a5870-121">Geometry</span></span> | <span data-ttu-id="a5870-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="a5870-122">Pixel</span></span> | <span data-ttu-id="a5870-123">Compute</span><span class="sxs-lookup"><span data-stu-id="a5870-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a5870-124">x</span><span class="sxs-lookup"><span data-stu-id="a5870-124">x</span></span>      | <span data-ttu-id="a5870-125">x</span><span class="sxs-lookup"><span data-stu-id="a5870-125">x</span></span>    | <span data-ttu-id="a5870-126">x</span><span class="sxs-lookup"><span data-stu-id="a5870-126">x</span></span>      | <span data-ttu-id="a5870-127">x</span><span class="sxs-lookup"><span data-stu-id="a5870-127">x</span></span>        | <span data-ttu-id="a5870-128">x</span><span class="sxs-lookup"><span data-stu-id="a5870-128">x</span></span>     | <span data-ttu-id="a5870-129">x</span><span class="sxs-lookup"><span data-stu-id="a5870-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a5870-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a5870-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5870-131">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="a5870-131">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="a5870-132">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="a5870-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




