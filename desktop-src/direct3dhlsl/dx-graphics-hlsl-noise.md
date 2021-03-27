---
title: Lautstärke
description: Generiert einen zufälligen Wert mithilfe des Perlin-Rausch-Algorithmus.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- Füll-HLSL
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391248"
---
# <a name="noise"></a><span data-ttu-id="1b992-104">Lautstärke</span><span class="sxs-lookup"><span data-stu-id="1b992-104">noise</span></span>

<span data-ttu-id="1b992-105">Generiert einen zufälligen Wert mithilfe des Perlin-Rausch-Algorithmus.</span><span class="sxs-lookup"><span data-stu-id="1b992-105">Generates a random value using the Perlin-noise algorithm.</span></span>




| <span data-ttu-id="1b992-106">*ret* -Rauschen (*x*)</span><span class="sxs-lookup"><span data-stu-id="1b992-106">*ret* noise(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="1b992-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b992-107">Parameters</span></span>



| <span data-ttu-id="1b992-108">Element</span><span class="sxs-lookup"><span data-stu-id="1b992-108">Item</span></span>                                                   | <span data-ttu-id="1b992-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b992-109">Description</span></span>                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="1b992-110"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="1b992-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="1b992-111">\[in \] einem Gleit Komma Vektor, von dem Perlin-Rauschen generiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b992-111">\[in\] A floating-point vector from which to generate Perlin noise.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="1b992-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b992-112">Return Value</span></span>

<span data-ttu-id="1b992-113">Der Perlin-Rausch Wert innerhalb eines Bereichs zwischen-1 und 1.</span><span class="sxs-lookup"><span data-stu-id="1b992-113">The Perlin noise value within a range between -1 and 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b992-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b992-114">Remarks</span></span>

<span data-ttu-id="1b992-115">Perlin-Rauschwerte ändern sich reibungslos von einem Punkt zu einem anderen als einem Leerzeichen und erstellen dabei natürliche, nach dem Zufallsprinzip generierte Werte.</span><span class="sxs-lookup"><span data-stu-id="1b992-115">Perlin noise values change smoothly from one point to another over a space, creating natural looking, randomly generated values.</span></span> <span data-ttu-id="1b992-116">Sie können Perlin-Rauschen verwenden, um prozedurale Texturen für Effekte wie Rauch und Feuer zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1b992-116">You can use Perlin noise to generate procedural textures for effects like smoke and fire.</span></span>

## <a name="type-description"></a><span data-ttu-id="1b992-117">Typbeschreibung</span><span class="sxs-lookup"><span data-stu-id="1b992-117">Type Description</span></span>



| <span data-ttu-id="1b992-118">Name</span><span class="sxs-lookup"><span data-stu-id="1b992-118">Name</span></span>  | [<span data-ttu-id="1b992-119">**Vorlagentyp**</span><span class="sxs-lookup"><span data-stu-id="1b992-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="1b992-120">**Komponententyp**</span><span class="sxs-lookup"><span data-stu-id="1b992-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="1b992-121">Size</span><span class="sxs-lookup"><span data-stu-id="1b992-121">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="1b992-122">*x*</span><span class="sxs-lookup"><span data-stu-id="1b992-122">*x*</span></span>   | [<span data-ttu-id="1b992-123">**ve**</span><span class="sxs-lookup"><span data-stu-id="1b992-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1b992-124">**Hafen**</span><span class="sxs-lookup"><span data-stu-id="1b992-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1b992-125">any</span><span class="sxs-lookup"><span data-stu-id="1b992-125">any</span></span>  |
| <span data-ttu-id="1b992-126">*TZI*</span><span class="sxs-lookup"><span data-stu-id="1b992-126">*ret*</span></span> | [<span data-ttu-id="1b992-127">**Skalar**</span><span class="sxs-lookup"><span data-stu-id="1b992-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="1b992-128">**float**</span><span class="sxs-lookup"><span data-stu-id="1b992-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="1b992-129">1</span><span class="sxs-lookup"><span data-stu-id="1b992-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1b992-130">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="1b992-130">Minimum Shader Model</span></span>

<span data-ttu-id="1b992-131">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1b992-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1b992-132">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="1b992-132">Shader Model</span></span>                                                                       | <span data-ttu-id="1b992-133">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="1b992-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="1b992-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle</span><span class="sxs-lookup"><span data-stu-id="1b992-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="1b992-135">nein</span><span class="sxs-lookup"><span data-stu-id="1b992-135">no</span></span>                  |
| [<span data-ttu-id="1b992-136">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b992-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="1b992-137">Ja ( \_ nur TX 1 \_ 0)</span><span class="sxs-lookup"><span data-stu-id="1b992-137">yes (tx\_1\_0 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="1b992-138">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1b992-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b992-139">**Intrinsische Funktionen (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="1b992-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

