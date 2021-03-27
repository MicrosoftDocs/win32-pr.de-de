---
title: Textur-Typ
description: Verwenden Sie die folgende Syntax, um eine Textur Variable zu deklarieren.
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- Textur Type HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2020
ms.locfileid: "103723984"
---
# <a name="texture-type"></a><span data-ttu-id="d26a6-104">Textur-Typ</span><span class="sxs-lookup"><span data-stu-id="d26a6-104">Texture type</span></span>

<span data-ttu-id="d26a6-105">Verwenden Sie die folgende Syntax, um eine Textur Variable zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="d26a6-105">Use the following syntax to declare a texture variable.</span></span>

|                |
|----------------|
| <span data-ttu-id="d26a6-106">**Typname;**</span><span class="sxs-lookup"><span data-stu-id="d26a6-106">**Type Name;**</span></span> |

## <a name="parameters"></a><span data-ttu-id="d26a6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d26a6-107">Parameters</span></span>
| <span data-ttu-id="d26a6-108">Element</span><span class="sxs-lookup"><span data-stu-id="d26a6-108">Item</span></span>                                                                                     | <span data-ttu-id="d26a6-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d26a6-109">Description</span></span>                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d26a6-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Sorte**</span><span class="sxs-lookup"><span data-stu-id="d26a6-110"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span><br/> | <span data-ttu-id="d26a6-111">Einer der folgenden Typen: Textur (nicht typisiert, aus Gründen der Abwärtskompatibilität), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, texturecube.</span><span class="sxs-lookup"><span data-stu-id="d26a6-111">One of the following types: texture (untyped, for backwards compatibility), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube.</span></span> <span data-ttu-id="d26a6-112">Die Elementgröße muss in 4 32-Bit-Mengen passen.</span><span class="sxs-lookup"><span data-stu-id="d26a6-112">The element size must fit into 4 32-bit quantities.</span></span><br/> |
| <span data-ttu-id="d26a6-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**</span><span class="sxs-lookup"><span data-stu-id="d26a6-113"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name**</span></span><br/> | <span data-ttu-id="d26a6-114">Eine ASCII-Zeichenfolge, die den Variablennamen eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d26a6-114">An ASCII string that uniquely identifies the variable name.</span></span><br/>                                                                                                                                                   |
## <a name="remarks"></a><span data-ttu-id="d26a6-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d26a6-115">Remarks</span></span>

<span data-ttu-id="d26a6-116">Die Verwendung einer Textur besteht aus drei Teilen.</span><span class="sxs-lookup"><span data-stu-id="d26a6-116">There are three parts to using a texture.</span></span>

1.  <span data-ttu-id="d26a6-117">Deklarieren einer Textur Variablen.</span><span class="sxs-lookup"><span data-stu-id="d26a6-117">Declaring a texture variable.</span></span> <span data-ttu-id="d26a6-118">Dies erfolgt mit der oben gezeigten Syntax.</span><span class="sxs-lookup"><span data-stu-id="d26a6-118">This is done with the syntax shown above.</span></span> <span data-ttu-id="d26a6-119">Dies sind z. b. gültige Deklarationen.</span><span class="sxs-lookup"><span data-stu-id="d26a6-119">For example, these are valid declarations.</span></span>

    ```
    texture g_MeshTexture;
    ```

    <span data-ttu-id="d26a6-120">\- oder -</span><span class="sxs-lookup"><span data-stu-id="d26a6-120">\- or -</span></span>

    ```
    Texture2D g_MeshTexture;
    ```

2.  <span data-ttu-id="d26a6-121">Deklarieren und Initialisieren eines samplerobjekts.</span><span class="sxs-lookup"><span data-stu-id="d26a6-121">Declaring and initializing a sampler object.</span></span> <span data-ttu-id="d26a6-122">Dies erfolgt mit einer etwas anderen Syntax in Direct3D 9 und Direct3D 10.</span><span class="sxs-lookup"><span data-stu-id="d26a6-122">This is done with slightly different syntax in Direct3D 9 and Direct3D 10.</span></span> <span data-ttu-id="d26a6-123">Ausführliche Informationen zur samplerobjektsyntax finden Sie unter [Sampler-Typ (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="d26a6-123">For details about sampler object syntax, see [Sampler Type (DirectX HLSL)](dx-graphics-hlsl-sampler.md).</span></span>
3.  <span data-ttu-id="d26a6-124">Aufrufen einer Textur Funktion in einem Shader.</span><span class="sxs-lookup"><span data-stu-id="d26a6-124">Invoking a texture function in a shader.</span></span>

<span data-ttu-id="d26a6-125">Unterschiede zwischen Direct3D 9 und Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="d26a6-125">Differences between Direct3D 9 and Direct3D 10:</span></span>

<span data-ttu-id="d26a6-126">Direct3D 9 verwendet systeminterne [Textur Funktionen](dx-graphics-hlsl-intrinsic-functions.md) , um Textur Operationen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d26a6-126">Direct3D 9 uses [intrinsic texture functions](dx-graphics-hlsl-intrinsic-functions.md) to perform texture operations.</span></span> <span data-ttu-id="d26a6-127">Dieses Beispiel basiert auf dem [basichlsl](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) -Beispiel und verwendet [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) zum Durchführen von Textur Stichproben.</span><span class="sxs-lookup"><span data-stu-id="d26a6-127">This example is from the [BasicHLSL Sample](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) and uses [tex2D(s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) to perform texture sampling.</span></span>

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

<span data-ttu-id="d26a6-128">Direct3D 10 verwendet stattdessen vorlagenbasierte [Textur Objekte](dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="d26a6-128">Direct3D 10 uses [templated texture objects](dx-graphics-hlsl-to-type.md) instead.</span></span> <span data-ttu-id="d26a6-129">Im folgenden finden Sie ein Beispiel für die äquivalente Textur Operation.</span><span class="sxs-lookup"><span data-stu-id="d26a6-129">Here is an example of the equivalent texture operation.</span></span>

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a><span data-ttu-id="d26a6-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d26a6-130">See also</span></span>

[<span data-ttu-id="d26a6-131">Datentypen (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d26a6-131">Data Types (DirectX HLSL)</span></span>](dx-graphics-hlsl-data-types.md)
