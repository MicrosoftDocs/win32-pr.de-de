---
title: 'RWTexture1D:: Load (int)-Funktion'
description: 'Liest Textur Daten. | RWTexture1D:: Load (int)-Funktion'
ms.assetid: AA5E324E-A2C0-45C5-92A8-E4DBC4EB684C
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
ms.openlocfilehash: e78cd12502ada91e48df1ce88be6a19fb714327f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353118"
---
# <a name="rwtexture1dloadint-function"></a><span data-ttu-id="83610-105">RWTexture1D:: Load (int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="83610-105">RWTexture1D::Load(int) function</span></span>

<span data-ttu-id="83610-106">Liest Textur Daten.</span><span class="sxs-lookup"><span data-stu-id="83610-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="83610-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="83610-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="83610-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="83610-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83610-109">*Speicherort* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="83610-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83610-110">Typ: **int**</span><span class="sxs-lookup"><span data-stu-id="83610-110">Type: **int**</span></span>

<span data-ttu-id="83610-111">Der Speicherort der Textur.</span><span class="sxs-lookup"><span data-stu-id="83610-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83610-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83610-112">Return value</span></span>

<span data-ttu-id="83610-113">Typ:</span><span class="sxs-lookup"><span data-stu-id="83610-113">Type:</span></span>

<span data-ttu-id="83610-114">Der Rückgabetyp entspricht dem Typ in der Deklaration für das [**RWTexture1D**](sm5-object-rwtexture1d.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="83610-114">The return type matches the type in the declaration for the [**RWTexture1D**](sm5-object-rwtexture1d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="83610-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83610-115">Remarks</span></span>

<span data-ttu-id="83610-116">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="83610-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="83610-117">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="83610-117">Vertex</span></span> | <span data-ttu-id="83610-118">Hülle</span><span class="sxs-lookup"><span data-stu-id="83610-118">Hull</span></span> | <span data-ttu-id="83610-119">Domain</span><span class="sxs-lookup"><span data-stu-id="83610-119">Domain</span></span> | <span data-ttu-id="83610-120">Geometrie</span><span class="sxs-lookup"><span data-stu-id="83610-120">Geometry</span></span> | <span data-ttu-id="83610-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="83610-121">Pixel</span></span> | <span data-ttu-id="83610-122">Compute</span><span class="sxs-lookup"><span data-stu-id="83610-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="83610-123">x</span><span class="sxs-lookup"><span data-stu-id="83610-123">x</span></span>     | <span data-ttu-id="83610-124">x</span><span class="sxs-lookup"><span data-stu-id="83610-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="83610-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="83610-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83610-126">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="83610-126">Load methods</span></span>](rwtexture1d-load.md)
</dt> </dl>

 

 




