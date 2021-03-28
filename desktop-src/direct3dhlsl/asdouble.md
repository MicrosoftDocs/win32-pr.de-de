---
title: AsDouble-Funktion
description: Interpretiert einen Umwandlungs Wert (2 32-Bit-Werte) in einen Double-Wert um.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- AsDouble-Funktion HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa2c83ee01739a2e2ee9595d0a26e1bdb80fef1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038141"
---
# <a name="asdouble-function"></a><span data-ttu-id="242ff-104">AsDouble-Funktion</span><span class="sxs-lookup"><span data-stu-id="242ff-104">asdouble function</span></span>

<span data-ttu-id="242ff-105">Interpretiert einen Umwandlungs Wert (2 32-Bit-Werte) in einen Double-Wert um.</span><span class="sxs-lookup"><span data-stu-id="242ff-105">Reinterprets a cast value (two 32-bit values) into a double.</span></span>

## <a name="syntax"></a><span data-ttu-id="242ff-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="242ff-106">Syntax</span></span>

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="242ff-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="242ff-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="242ff-108">*lowbits* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="242ff-108">*lowbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="242ff-109">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="242ff-109">Type: **uint**</span></span>

<span data-ttu-id="242ff-110">Das niedrige 32-Bit-Muster des Eingabe Werts.</span><span class="sxs-lookup"><span data-stu-id="242ff-110">The low 32-bit pattern of the input value.</span></span>

</dd> <dt>

<span data-ttu-id="242ff-111">*highbits* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="242ff-111">*highbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="242ff-112">Typ: **uint**</span><span class="sxs-lookup"><span data-stu-id="242ff-112">Type: **uint**</span></span>

<span data-ttu-id="242ff-113">Das High 32-Bit-Muster des Eingabe Werts.</span><span class="sxs-lookup"><span data-stu-id="242ff-113">The high 32-bit pattern of the input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="242ff-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="242ff-114">Return value</span></span>

<span data-ttu-id="242ff-115">Typ: **Double**</span><span class="sxs-lookup"><span data-stu-id="242ff-115">Type: **double**</span></span>

<span data-ttu-id="242ff-116">Die Eingabe (2 32-Bit-Werte) wird als Double-Wert umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="242ff-116">The input (two 32-bit values) recast as a double.</span></span>

## <a name="remarks"></a><span data-ttu-id="242ff-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="242ff-117">Remarks</span></span>

<span data-ttu-id="242ff-118">Außerdem ist die folgende überladene Version verfügbar:</span><span class="sxs-lookup"><span data-stu-id="242ff-118">The following overloaded version is also available:</span></span>

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

<span data-ttu-id="242ff-119">Wenn der Eingabe Wert 2 32-Bit-Komponenten ist, enthält der Rückgabetyp einen Double-Wert.</span><span class="sxs-lookup"><span data-stu-id="242ff-119">If the input value is two 32-bit components, the return type will contain one double.</span></span> <span data-ttu-id="242ff-120">Wenn der Eingabe Wert 4 32-Bit-Komponenten ist, enthält der Rückgabetyp zwei Double-Werte.</span><span class="sxs-lookup"><span data-stu-id="242ff-120">If the input value is four 32-bit components, the return type will contain two doubles.</span></span> <span data-ttu-id="242ff-121">Wenn der Eingabe Wert ein 64-Bit-Typ ist, hat der zurückgegebene Wert die gleiche Anzahl von Komponenten wie der Eingabe Wert.</span><span class="sxs-lookup"><span data-stu-id="242ff-121">If the input value is a 64-bit type, the returned value will have the same number of components as the input value.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="242ff-122">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="242ff-122">Minimum Shader Model</span></span>

<span data-ttu-id="242ff-123">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="242ff-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="242ff-124">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="242ff-124">Shader Model</span></span>                                                                | <span data-ttu-id="242ff-125">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="242ff-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="242ff-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="242ff-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="242ff-127">ja</span><span class="sxs-lookup"><span data-stu-id="242ff-127">yes</span></span>       |



 

<span data-ttu-id="242ff-128">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="242ff-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="242ff-129">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="242ff-129">Vertex</span></span> | <span data-ttu-id="242ff-130">Hülle</span><span class="sxs-lookup"><span data-stu-id="242ff-130">Hull</span></span> | <span data-ttu-id="242ff-131">Domain</span><span class="sxs-lookup"><span data-stu-id="242ff-131">Domain</span></span> | <span data-ttu-id="242ff-132">Geometrie</span><span class="sxs-lookup"><span data-stu-id="242ff-132">Geometry</span></span> | <span data-ttu-id="242ff-133">Pixel</span><span class="sxs-lookup"><span data-stu-id="242ff-133">Pixel</span></span> | <span data-ttu-id="242ff-134">Compute</span><span class="sxs-lookup"><span data-stu-id="242ff-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="242ff-135">x</span><span class="sxs-lookup"><span data-stu-id="242ff-135">x</span></span>      | <span data-ttu-id="242ff-136">x</span><span class="sxs-lookup"><span data-stu-id="242ff-136">x</span></span>    | <span data-ttu-id="242ff-137">x</span><span class="sxs-lookup"><span data-stu-id="242ff-137">x</span></span>      | <span data-ttu-id="242ff-138">x</span><span class="sxs-lookup"><span data-stu-id="242ff-138">x</span></span>        | <span data-ttu-id="242ff-139">x</span><span class="sxs-lookup"><span data-stu-id="242ff-139">x</span></span>     | <span data-ttu-id="242ff-140">x</span><span class="sxs-lookup"><span data-stu-id="242ff-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="242ff-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="242ff-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="242ff-142">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="242ff-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="242ff-143">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="242ff-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




