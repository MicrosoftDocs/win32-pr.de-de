---
title: DirectML-Konstanten
description: Die folgenden Konstanten werden in `DirectML.h` deklariert.
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
ms.openlocfilehash: ad4ff8c409f79a03cb4021974fe374498926c3e2
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803405"
---
# <a name="directml-constants"></a><span data-ttu-id="f41b1-104">DirectML-Konstanten</span><span class="sxs-lookup"><span data-stu-id="f41b1-104">DirectML constants</span></span>

<span data-ttu-id="f41b1-105">Die folgenden Konstanten werden in `DirectML.h` deklariert.</span><span class="sxs-lookup"><span data-stu-id="f41b1-105">The following constants are declared in `DirectML.h`.</span></span>

| <span data-ttu-id="f41b1-106">Konstante</span><span class="sxs-lookup"><span data-stu-id="f41b1-106">Constant</span></span> | <span data-ttu-id="f41b1-107">Wert</span><span class="sxs-lookup"><span data-stu-id="f41b1-107">Value</span></span> | <span data-ttu-id="f41b1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f41b1-108">Description</span></span> |
|-|-|-|
| <span data-ttu-id="f41b1-109">DML_TENSOR_DIMENSION_COUNT_MAX</span><span class="sxs-lookup"><span data-stu-id="f41b1-109">DML_TENSOR_DIMENSION_COUNT_MAX</span></span> | <span data-ttu-id="f41b1-110">5</span><span class="sxs-lookup"><span data-stu-id="f41b1-110">5</span></span> | <span data-ttu-id="f41b1-111">DirectML-Tensors unterstützen maximal 5 Dimensionen für DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="f41b1-111">DirectML tensors support a maximum of 5 dimensions for DML_TARGET_VERSION < DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="f41b1-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span><span class="sxs-lookup"><span data-stu-id="f41b1-112">DML_TENSOR_DIMENSION_COUNT_MAX1</span></span> | <span data-ttu-id="f41b1-113">8</span><span class="sxs-lookup"><span data-stu-id="f41b1-113">8</span></span> | <span data-ttu-id="f41b1-114">DirectML-Tensoren unterstützen maximal 8 Dimensionen für DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span><span class="sxs-lookup"><span data-stu-id="f41b1-114">DirectML tensors support a maximum of 8 dimensions for DML_TARGET_VERSION >= DML_FEATURE_LEVEL_3_0.</span></span> |
| <span data-ttu-id="f41b1-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="f41b1-115">DML_TEMPORARY_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="f41b1-116">256</span><span class="sxs-lookup"><span data-stu-id="f41b1-116">256</span></span> | <span data-ttu-id="f41b1-117">Temporäre und persistente Puffer müssen über eine Basisadresse verfügen, die auf 256 Bytes ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="f41b1-117">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="f41b1-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="f41b1-118">DML_PERSISTENT_BUFFER_ALIGNMENT</span></span> | <span data-ttu-id="f41b1-119">256</span><span class="sxs-lookup"><span data-stu-id="f41b1-119">256</span></span> | <span data-ttu-id="f41b1-120">Temporäre und persistente Puffer müssen über eine Basisadresse verfügen, die auf 256 Bytes ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="f41b1-120">Temporary and persistent buffers must have a base address that is aligned to 256 bytes.</span></span> |
| <span data-ttu-id="f41b1-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span><span class="sxs-lookup"><span data-stu-id="f41b1-121">DML_MINIMUM_BUFFER_TENSOR_ALIGNMENT</span></span> | <span data-ttu-id="f41b1-122">16</span><span class="sxs-lookup"><span data-stu-id="f41b1-122">16</span></span> | <span data-ttu-id="f41b1-123">Puffer tensors haben eine Mindestanforderung an die Ausrichtung der Basisadresse von 16 Bytes.</span><span class="sxs-lookup"><span data-stu-id="f41b1-123">Buffer tensors have a minimum base address alignment requirement of 16 bytes.</span></span> |

## <a name="requirements"></a><span data-ttu-id="f41b1-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f41b1-124">Requirements</span></span>

| <span data-ttu-id="f41b1-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f41b1-125">Requirement</span></span> | <span data-ttu-id="f41b1-126">Wert</span><span class="sxs-lookup"><span data-stu-id="f41b1-126">Value</span></span> |
|-|-|
| <span data-ttu-id="f41b1-127">Header</span><span class="sxs-lookup"><span data-stu-id="f41b1-127">Header</span></span> | <span data-ttu-id="f41b1-128">DirectML.h</span><span class="sxs-lookup"><span data-stu-id="f41b1-128">DirectML.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="f41b1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f41b1-129">See also</span></span>

* [<span data-ttu-id="f41b1-130">DirectML-Referenz</span><span class="sxs-lookup"><span data-stu-id="f41b1-130">DirectML reference</span></span>](direct3d-directml-reference.md)
* [<span data-ttu-id="f41b1-131">Core-Referenz</span><span class="sxs-lookup"><span data-stu-id="f41b1-131">Core reference</span></span>](direct3d-12-core-reference.md)
* [<span data-ttu-id="f41b1-132">Referenz für Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="f41b1-132">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
