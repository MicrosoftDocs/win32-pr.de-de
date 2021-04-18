---
title: DirectML-Konstanten
description: Die folgenden Konstanten werden in deklariert `DirectML.h` .
keywords:
- Konstanten
topic_type:
- apiref
api_name:
- DirectML constants
api_location:
- DirectML.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/04/2020
ms.openlocfilehash: d6c3791812f3ac1191f1959150bd5ac7059c54fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106371882"
---
# <a name="directml-constants"></a><span data-ttu-id="0abd7-104">DirectML-Konstanten</span><span class="sxs-lookup"><span data-stu-id="0abd7-104">DirectML constants</span></span>

<span data-ttu-id="0abd7-105">Die folgenden Konstanten werden in deklariert `DirectML.h` .</span><span class="sxs-lookup"><span data-stu-id="0abd7-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="0abd7-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="0abd7-106">Constant</span></span> | <span data-ttu-id="0abd7-107">Wert</span><span class="sxs-lookup"><span data-stu-id="0abd7-107">Value</span></span> | <span data-ttu-id="0abd7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0abd7-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="0abd7-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="0abd7-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="0abd7-110">5</span><span class="sxs-lookup"><span data-stu-id="0abd7-110">5</span></span> | <span data-ttu-id="0abd7-111">Directml-Tensoren unterstützen für DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0 maximal 5 Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="0abd7-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="0abd7-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="0abd7-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="0abd7-113">8</span><span class="sxs-lookup"><span data-stu-id="0abd7-113">8</span></span> | <span data-ttu-id="0abd7-114">Directml-Tensoren unterstützen für DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0 maximal 8 Dimensionen.</span><span class="sxs-lookup"><span data-stu-id="0abd7-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="0abd7-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="0abd7-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="0abd7-116">256</span><span class="sxs-lookup"><span data-stu-id="0abd7-116">256</span></span> | <span data-ttu-id="0abd7-117">Temporäre und permanente Puffer müssen eine Basisadresse aufweisen, die auf 256 Bytes ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="0abd7-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="0abd7-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="0abd7-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="0abd7-119">256</span><span class="sxs-lookup"><span data-stu-id="0abd7-119">256</span></span> | <span data-ttu-id="0abd7-120">Temporäre und permanente Puffer müssen eine Basisadresse aufweisen, die auf 256 Bytes ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="0abd7-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="0abd7-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="0abd7-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="0abd7-122">16</span><span class="sxs-lookup"><span data-stu-id="0abd7-122">16</span></span> | <span data-ttu-id="0abd7-123">Puffer-Tensoren haben eine minimale Basisadressen-Ausrichtungs Anforderung von 16 Bytes.</span><span class="sxs-lookup"><span data-stu-id="0abd7-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="0abd7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0abd7-124">Requirements</span></span>

| <span data-ttu-id="0abd7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0abd7-125">Requirement</span></span> | <span data-ttu-id="0abd7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0abd7-126">Value</span></span> |
|-|-|
| <span data-ttu-id="0abd7-127">Header</span><span class="sxs-lookup"><span data-stu-id="0abd7-127">Header</span></span> | <span data-ttu-id="0abd7-128">D3D12. h</span><span class="sxs-lookup"><span data-stu-id="0abd7-128">D3D12.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="0abd7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0abd7-129">See also</span></span>

* [<span data-ttu-id="0abd7-130">DirectML-Referenz</span><span class="sxs-lookup"><span data-stu-id="0abd7-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="0abd7-131">Core-Referenz</span><span class="sxs-lookup"><span data-stu-id="0abd7-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="0abd7-132">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0abd7-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
