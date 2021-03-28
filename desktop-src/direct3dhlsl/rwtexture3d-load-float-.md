---
title: 'RWTexture3D:: Load (int)-Funktion'
description: 'Liest Textur Daten. | RWTexture3D:: Load (int)-Funktion'
ms.assetid: 93C4FFFF-8695-4BAF-BAE4-A2704332E6A9
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
ms.openlocfilehash: 70f001cbea05f21a96bfbf1b5bdbf43a1d7da07d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353099"
---
# <a name="rwtexture3dloadint-function"></a><span data-ttu-id="b9c70-105">RWTexture3D:: Load (int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="b9c70-105">RWTexture3D::Load(int) function</span></span>

<span data-ttu-id="b9c70-106">Liest Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="b9c70-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9c70-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9c70-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="b9c70-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9c70-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9c70-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9c70-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9c70-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="b9c70-110">Type: **int**</span></span>

<span data-ttu-id="b9c70-111">Der Speicherort der Textur.</span><span class="sxs-lookup"><span data-stu-id="b9c70-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9c70-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9c70-112">Return value</span></span>

<span data-ttu-id="b9c70-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="b9c70-113">Type:</span></span>

<span data-ttu-id="b9c70-114">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWTexture3D**](sm5-object-rwtexture3d.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b9c70-114">The return type matches the type in the declaration for the [**RWTexture3D**](sm5-object-rwtexture3d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9c70-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9c70-115">Remarks</span></span>

<span data-ttu-id="b9c70-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="b9c70-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b9c70-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="b9c70-117">Vertex</span></span> | <span data-ttu-id="b9c70-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="b9c70-118">Hull</span></span> | <span data-ttu-id="b9c70-119">Domain</span><span class="sxs-lookup"><span data-stu-id="b9c70-119">Domain</span></span> | <span data-ttu-id="b9c70-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="b9c70-120">Geometry</span></span> | <span data-ttu-id="b9c70-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="b9c70-121">Pixel</span></span> | <span data-ttu-id="b9c70-122">Compute</span><span class="sxs-lookup"><span data-stu-id="b9c70-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b9c70-123">x</span><span class="sxs-lookup"><span data-stu-id="b9c70-123">x</span></span>     | <span data-ttu-id="b9c70-124">x</span><span class="sxs-lookup"><span data-stu-id="b9c70-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b9c70-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b9c70-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c70-126">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="b9c70-126">Load methods</span></span>](rwtexture3d-load.md)
</dt> </dl>

 

 




