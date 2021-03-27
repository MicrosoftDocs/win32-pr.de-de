---
title: Processisolinetess Factors-Funktion
description: Generiert die gerundeten Mosaik Faktoren für eine Isolationsstufe.
ms.assetid: 0816b3e0-cb03-4a7a-9732-e84c637b3d48
keywords:
- Processisolinetess Factors-Funktion HLSL
topic_type:
- apiref
api_name:
- ProcessIsolineTessFactors
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 10da0e5bf0f2138c57da3fcfe962bc6a88800068
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718821"
---
# <a name="processisolinetessfactors-function"></a><span data-ttu-id="c7d1a-104">Processisolinetess Factors-Funktion</span><span class="sxs-lookup"><span data-stu-id="c7d1a-104">ProcessIsolineTessFactors function</span></span>

<span data-ttu-id="c7d1a-105">Generiert die gerundeten Mosaik Faktoren für eine Isolationsstufe.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-105">Generates the rounded tessellation factors for an isoline.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7d1a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7d1a-106">Syntax</span></span>

``` syntax
void ProcessIsolineTessFactors(
  in  float RawDetailFactor,
  in  float RawDensityFactor,
  out float RoundedDetailFactor,
  out float RoundedDensityFactor
);
```

## <a name="parameters"></a><span data-ttu-id="c7d1a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7d1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7d1a-108">*Rawdetailfactor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7d1a-108">*RawDetailFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d1a-109">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c7d1a-109">Type: **float**</span></span>

<span data-ttu-id="c7d1a-110">Der gewünschte Detail Faktor.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-110">The desired detail factor.</span></span>

</dd> <dt>

<span data-ttu-id="c7d1a-111">*Rawdensityfactor* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c7d1a-111">*RawDensityFactor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d1a-112">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c7d1a-112">Type: **float**</span></span>

<span data-ttu-id="c7d1a-113">Der gewünschte Dichte Faktor.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-113">The desired density factor.</span></span>

</dd> <dt>

<span data-ttu-id="c7d1a-114">*Rounabddetailfactor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c7d1a-114">*RoundedDetailFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d1a-115">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c7d1a-115">Type: **float**</span></span>

<span data-ttu-id="c7d1a-116">Der abgerundete Detail Faktor wurde an einen Bereich geklemmt, der vom Mosaik verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-116">The rounded detail factor clamped to a range that can be used by the tessellator.</span></span>

</dd> <dt>

<span data-ttu-id="c7d1a-117">*Rounzerddensityfactor* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c7d1a-117">*RoundedDensityFactor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7d1a-118">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="c7d1a-118">Type: **float**</span></span>

<span data-ttu-id="c7d1a-119">Der Faktor für die abgerundete Dichte wurde an eine rangegeklammert, die vom Mosaik Prozess verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-119">The rounded density factor clamped to a rangethat can be used by the tessellator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7d1a-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c7d1a-120">Return value</span></span>

<span data-ttu-id="c7d1a-121">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7d1a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7d1a-122">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="c7d1a-123">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c7d1a-123">Minimum Shader Model</span></span>

<span data-ttu-id="c7d1a-124">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7d1a-124">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c7d1a-125">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c7d1a-125">Shader Model</span></span>                                                                | <span data-ttu-id="c7d1a-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c7d1a-126">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c7d1a-127">[Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="c7d1a-127">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="c7d1a-128">ja</span><span class="sxs-lookup"><span data-stu-id="c7d1a-128">yes</span></span>       |



 

<span data-ttu-id="c7d1a-129">Diese Funktion wird in den folgenden Typen von Shadern unterstützt:</span><span class="sxs-lookup"><span data-stu-id="c7d1a-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="c7d1a-130">Scheitelpunkt</span><span class="sxs-lookup"><span data-stu-id="c7d1a-130">Vertex</span></span> | <span data-ttu-id="c7d1a-131">Hülle</span><span class="sxs-lookup"><span data-stu-id="c7d1a-131">Hull</span></span> | <span data-ttu-id="c7d1a-132">Domain</span><span class="sxs-lookup"><span data-stu-id="c7d1a-132">Domain</span></span> | <span data-ttu-id="c7d1a-133">Geometrie</span><span class="sxs-lookup"><span data-stu-id="c7d1a-133">Geometry</span></span> | <span data-ttu-id="c7d1a-134">Pixel</span><span class="sxs-lookup"><span data-stu-id="c7d1a-134">Pixel</span></span> | <span data-ttu-id="c7d1a-135">Compute</span><span class="sxs-lookup"><span data-stu-id="c7d1a-135">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="c7d1a-136">x</span><span class="sxs-lookup"><span data-stu-id="c7d1a-136">x</span></span>    |        |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="c7d1a-137">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7d1a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d1a-138">Intrinsische Funktionen</span><span class="sxs-lookup"><span data-stu-id="c7d1a-138">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="c7d1a-139">Shader-Modell 5</span><span class="sxs-lookup"><span data-stu-id="c7d1a-139">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




