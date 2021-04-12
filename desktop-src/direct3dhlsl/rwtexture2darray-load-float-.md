---
title: 'RWTexture2DArray:: Load (int)-Funktion'
description: 'Liest Textur Daten. | RWTexture2DArray:: Load (int)-Funktion'
ms.assetid: BC247B2A-1744-4E37-A501-22E4A592A32D
keywords:
- Ladefunktion HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b23439d471f4d22c807c8d45bb00c23a7d814e3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352989"
---
# <a name="rwtexture2darrayloadint-function"></a><span data-ttu-id="491dc-105">RWTexture2DArray:: Load (int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="491dc-105">RWTexture2DArray::Load(int) function</span></span>

<span data-ttu-id="491dc-106">Liest Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="491dc-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="491dc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="491dc-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="491dc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="491dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="491dc-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="491dc-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="491dc-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="491dc-110">Type: **int**</span></span>

<span data-ttu-id="491dc-111">Der Speicherort der Textur.</span><span class="sxs-lookup"><span data-stu-id="491dc-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="491dc-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="491dc-112">Return value</span></span>

<span data-ttu-id="491dc-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="491dc-113">Type:</span></span>

<span data-ttu-id="491dc-114">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="491dc-114">The return type matches the type in the declaration for the [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="491dc-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="491dc-115">Remarks</span></span>

<span data-ttu-id="491dc-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="491dc-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="491dc-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="491dc-117">Vertex</span></span> | <span data-ttu-id="491dc-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="491dc-118">Hull</span></span> | <span data-ttu-id="491dc-119">Domain</span><span class="sxs-lookup"><span data-stu-id="491dc-119">Domain</span></span> | <span data-ttu-id="491dc-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="491dc-120">Geometry</span></span> | <span data-ttu-id="491dc-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="491dc-121">Pixel</span></span> | <span data-ttu-id="491dc-122">Compute</span><span class="sxs-lookup"><span data-stu-id="491dc-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="491dc-123">x</span><span class="sxs-lookup"><span data-stu-id="491dc-123">x</span></span>     | <span data-ttu-id="491dc-124">x</span><span class="sxs-lookup"><span data-stu-id="491dc-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="491dc-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="491dc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="491dc-126">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="491dc-126">Load methods</span></span>](rwtexture2darray-load.md)
</dt> </dl>

 

 




