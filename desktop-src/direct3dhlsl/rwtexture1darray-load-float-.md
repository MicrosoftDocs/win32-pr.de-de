---
title: 'RWTexture1DArray:: Load (int)-Funktion'
description: 'Liest Textur Daten. | RWTexture1DArray:: Load (int)-Funktion'
ms.assetid: 8A9ABE4A-C9FA-4092-8C2B-24E55645CA64
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
ms.openlocfilehash: 4eb0dcbfe7a465756f865b90d2a39f65784bcd8a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981241"
---
# <a name="rwtexture1darrayloadint-function"></a><span data-ttu-id="c9c3c-105">RWTexture1DArray:: Load (int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="c9c3c-105">RWTexture1DArray::Load(int) function</span></span>

<span data-ttu-id="c9c3c-106">Liest Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="c9c3c-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9c3c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9c3c-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="c9c3c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9c3c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9c3c-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c9c3c-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9c3c-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="c9c3c-110">Type: **int**</span></span>

<span data-ttu-id="c9c3c-111">Der Speicherort der Textur.</span><span class="sxs-lookup"><span data-stu-id="c9c3c-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9c3c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c9c3c-112">Return value</span></span>

<span data-ttu-id="c9c3c-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="c9c3c-113">Type:</span></span>

<span data-ttu-id="c9c3c-114">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="c9c3c-114">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9c3c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9c3c-115">Remarks</span></span>

<span data-ttu-id="c9c3c-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c9c3c-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c9c3c-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c9c3c-117">Vertex</span></span> | <span data-ttu-id="c9c3c-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="c9c3c-118">Hull</span></span> | <span data-ttu-id="c9c3c-119">Domain</span><span class="sxs-lookup"><span data-stu-id="c9c3c-119">Domain</span></span> | <span data-ttu-id="c9c3c-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c9c3c-120">Geometry</span></span> | <span data-ttu-id="c9c3c-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="c9c3c-121">Pixel</span></span> | <span data-ttu-id="c9c3c-122">Compute</span><span class="sxs-lookup"><span data-stu-id="c9c3c-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c9c3c-123">x</span><span class="sxs-lookup"><span data-stu-id="c9c3c-123">x</span></span>     | <span data-ttu-id="c9c3c-124">x</span><span class="sxs-lookup"><span data-stu-id="c9c3c-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c9c3c-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c9c3c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9c3c-126">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="c9c3c-126">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 




