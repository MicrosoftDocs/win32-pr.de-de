---
title: Anfügen (DirectX HLSL Stream-Output-Objekt)
description: Fügen Sie Geometry-Shader-Output-Daten an einen vorhandenen Datenstrom an.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 97ab88961b22529accb4402fc2bd095ede5275c1
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "104313889"
---
# <a name="append-directx-hlsl-stream-output-object"></a><span data-ttu-id="b05c1-103">Anfügen (DirectX HLSL Stream-Output-Objekt)</span><span class="sxs-lookup"><span data-stu-id="b05c1-103">Append (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="b05c1-104">Fügen Sie Geometry-Shader-Output-Daten an einen vorhandenen Datenstrom an.</span><span class="sxs-lookup"><span data-stu-id="b05c1-104">Append geometry-shader-output data to an existing stream.</span></span>



|                            |
|----------------------------|
| <span data-ttu-id="b05c1-105">Append ( *streamdatatype*);</span><span class="sxs-lookup"><span data-stu-id="b05c1-105">Append( *StreamDataType*);</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="b05c1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b05c1-106">Parameters</span></span>



| <span data-ttu-id="b05c1-107">Element</span><span class="sxs-lookup"><span data-stu-id="b05c1-107">Item</span></span>                                                                                                                             | <span data-ttu-id="b05c1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b05c1-108">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b05c1-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**Streamdatatype**</span><span class="sxs-lookup"><span data-stu-id="b05c1-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span></span><br/> | <span data-ttu-id="b05c1-110">Eine Beschreibung der Dateneingabe.</span><span class="sxs-lookup"><span data-stu-id="b05c1-110">A data input description.</span></span> <span data-ttu-id="b05c1-111">Diese Beschreibung muss mit dem Stream-Object-Vorlagen Parameter namens [DataType](dx-graphics-hlsl-so-type.md)identisch sein.</span><span class="sxs-lookup"><span data-stu-id="b05c1-111">This description must match the stream-object template parameter called [DataType](dx-graphics-hlsl-so-type.md).</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="b05c1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b05c1-112">Return Value</span></span>

<span data-ttu-id="b05c1-113">Keine</span><span class="sxs-lookup"><span data-stu-id="b05c1-113">None</span></span>

## <a name="example"></a><span data-ttu-id="b05c1-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b05c1-114">Example</span></span>

<span data-ttu-id="b05c1-115">Dieser Code Ausschnitt (aus dem [cubemapgs-Beispiel](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) zeigt ein partielles Beispiel für das Anfügen von Dreiecks leisten primitiven an ein Stream-Output-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b05c1-115">This code snippet (from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) shows a partial example of appending triangle strip primitives to a stream-output object.</span></span>


```
[maxvertexcount(18)]
void GS_CubeMap( triangle GS_CUBEMAP_IN input[3], 
                 inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream )
{
    for( int f = 0; f < 6; ++f )
    {
        // Compute screen coordinates
        PS_CUBEMAP_IN output;
        output.RTIndex = f;
        for( int v = 0; v < 3; v++ )
        {
            output.Pos = mul( input[v].Pos, g_mViewCM[f] );
            output.Pos = mul( output.Pos, mProj );
            output.Tex = input[v].Tex;
            CubeMapStream.Append( output );
        }
        CubeMapStream.RestartStrip();
    }
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="b05c1-116">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="b05c1-116">Minimum Shader Model</span></span>

<span data-ttu-id="b05c1-117">Diese Funktion wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b05c1-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b05c1-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="b05c1-118">Shader Model</span></span>                                              | <span data-ttu-id="b05c1-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="b05c1-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b05c1-120">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="b05c1-120">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b05c1-121">ja</span><span class="sxs-lookup"><span data-stu-id="b05c1-121">yes</span></span>       |
| [<span data-ttu-id="b05c1-122">Shader-Modell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b05c1-122">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b05c1-123">nein</span><span class="sxs-lookup"><span data-stu-id="b05c1-123">no</span></span>        |
| [<span data-ttu-id="b05c1-124">Shader-Modell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b05c1-124">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b05c1-125">nein</span><span class="sxs-lookup"><span data-stu-id="b05c1-125">no</span></span>        |
| [<span data-ttu-id="b05c1-126">Shader-Modell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b05c1-126">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b05c1-127">nein</span><span class="sxs-lookup"><span data-stu-id="b05c1-127">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b05c1-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b05c1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b05c1-129">Stream-Output-Objekt</span><span class="sxs-lookup"><span data-stu-id="b05c1-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





