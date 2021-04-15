---
title: 'RWTexture3D:: Operator-Funktion'
description: Gibt eine Ressourcen Variable eines RWTexture3D zurück.
ms.assetid: 0b4ea895-ac34-49e5-80e6-74229c33bfe9
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
ms.openlocfilehash: e41ff4db387c4d0926083419082fd589005d96a6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104976936"
---
# <a name="rwtexture3doperator--function"></a><span data-ttu-id="75291-104">RWTexture3D:: Operator-Funktion</span><span class="sxs-lookup"><span data-stu-id="75291-104">RWTexture3D::Operator  function</span></span>

<span data-ttu-id="75291-105">Gibt eine Ressourcen Variable eines [**RWTexture3D**](sm5-object-rwtexture3d.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="75291-105">Returns a resource variable of a [**RWTexture3D**](sm5-object-rwtexture3d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="75291-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="75291-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="75291-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="75291-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75291-108">*POS* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75291-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75291-109">Typ: **uint3**</span><span class="sxs-lookup"><span data-stu-id="75291-109">Type: **uint3**</span></span>

<span data-ttu-id="75291-110">Die Indexposition.</span><span class="sxs-lookup"><span data-stu-id="75291-110">The index position.</span></span> <span data-ttu-id="75291-111">Enthält die Koordinaten (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="75291-111">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75291-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75291-112">Return value</span></span>

<span data-ttu-id="75291-113">Typ: **R**</span><span class="sxs-lookup"><span data-stu-id="75291-113">Type: **R**</span></span>

<span data-ttu-id="75291-114">Eine Ressourcen Variable.</span><span class="sxs-lookup"><span data-stu-id="75291-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="75291-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75291-115">Remarks</span></span>

<span data-ttu-id="75291-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="75291-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="75291-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="75291-117">Vertex</span></span> | <span data-ttu-id="75291-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="75291-118">Hull</span></span> | <span data-ttu-id="75291-119">Domain</span><span class="sxs-lookup"><span data-stu-id="75291-119">Domain</span></span> | <span data-ttu-id="75291-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="75291-120">Geometry</span></span> | <span data-ttu-id="75291-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="75291-121">Pixel</span></span> | <span data-ttu-id="75291-122">Compute</span><span class="sxs-lookup"><span data-stu-id="75291-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="75291-123">x</span><span class="sxs-lookup"><span data-stu-id="75291-123">x</span></span>     | <span data-ttu-id="75291-124">x</span><span class="sxs-lookup"><span data-stu-id="75291-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="75291-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="75291-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75291-126">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="75291-126">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="75291-127">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="75291-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




