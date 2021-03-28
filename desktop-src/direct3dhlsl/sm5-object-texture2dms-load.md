---
title: 'Texture2DMS:: Load (int, int)-Funktion'
description: 'Ruft einen Wert ab. | Texture2DMS:: Load (int, int)-Funktion'
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Load-Funktion DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d9c86bea7d914dd5975105a00a64789864a1fbd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981592"
---
# <a name="texture2dmsloadintint-function"></a><span data-ttu-id="1af90-105">Texture2DMS:: Load (int, int)-Funktion</span><span class="sxs-lookup"><span data-stu-id="1af90-105">Texture2DMS::Load(int,int) function</span></span>

<span data-ttu-id="1af90-106">Ruft einen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="1af90-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1af90-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1af90-107">Syntax</span></span>

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="1af90-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1af90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1af90-109">*Koord* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1af90-109">*coord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1af90-110">Typ: **int2**</span><span class="sxs-lookup"><span data-stu-id="1af90-110">Type: **int2**</span></span>

<span data-ttu-id="1af90-111">Der Eingabe Speicherort.</span><span class="sxs-lookup"><span data-stu-id="1af90-111">The input location.</span></span>

</dd> <dt>

<span data-ttu-id="1af90-112">*sampleingedex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1af90-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1af90-113">Typ: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="1af90-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="1af90-114">Der Beispiel Index.</span><span class="sxs-lookup"><span data-stu-id="1af90-114">The sample index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1af90-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1af90-115">Return value</span></span>

<span data-ttu-id="1af90-116">Typ: **T**</span><span class="sxs-lookup"><span data-stu-id="1af90-116">Type: **T**</span></span>

<span data-ttu-id="1af90-117">Ein-Wert, dessen Typ mit dem Typ der Textur Vorlage übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="1af90-117">One value, whose type matches the texture template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1af90-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1af90-118">Remarks</span></span>

<span data-ttu-id="1af90-119">Dies ist eine Liste der überladenen Versionen dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="1af90-119">This is a list of the overloaded versions of this method.</span></span>


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



<span data-ttu-id="1af90-120">Diese Funktion wird für die folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1af90-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="1af90-121">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="1af90-121">Vertex</span></span> | <span data-ttu-id="1af90-122">Hülle</span><span class="sxs-lookup"><span data-stu-id="1af90-122">Hull</span></span> | <span data-ttu-id="1af90-123">Domain</span><span class="sxs-lookup"><span data-stu-id="1af90-123">Domain</span></span> | <span data-ttu-id="1af90-124">Geometrie</span><span class="sxs-lookup"><span data-stu-id="1af90-124">Geometry</span></span> | <span data-ttu-id="1af90-125">Pixel</span><span class="sxs-lookup"><span data-stu-id="1af90-125">Pixel</span></span> | <span data-ttu-id="1af90-126">Compute</span><span class="sxs-lookup"><span data-stu-id="1af90-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="1af90-127">x</span><span class="sxs-lookup"><span data-stu-id="1af90-127">x</span></span>     | <span data-ttu-id="1af90-128">x</span><span class="sxs-lookup"><span data-stu-id="1af90-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1af90-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1af90-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af90-130">Lade Methoden</span><span class="sxs-lookup"><span data-stu-id="1af90-130">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="1af90-131">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="1af90-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
