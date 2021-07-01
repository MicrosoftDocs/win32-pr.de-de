---
title: Append (DirectX HLSL Stream-Output Object)
description: Fügen Sie geometry-shader-output-Daten an einen vorhandenen Stream an.
ms.assetid: 7df51383-7fc7-4a6f-aaa2-6c929f0443a3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 19d767f3c501cc42e21bbc44a196ba08cd6f1883
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120185"
---
# <a name="append-directx-hlsl-stream-output-object"></a><span data-ttu-id="5b2fa-103">Append (DirectX HLSL Stream-Output Object)</span><span class="sxs-lookup"><span data-stu-id="5b2fa-103">Append (DirectX HLSL Stream-Output Object)</span></span>

<span data-ttu-id="5b2fa-104">Fügen Sie geometry-shader-output-Daten an einen vorhandenen Stream an.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-104">Append geometry-shader-output data to an existing stream.</span></span>

<span data-ttu-id="5b2fa-105">Append( *StreamDataType*);</span><span class="sxs-lookup"><span data-stu-id="5b2fa-105">Append( *StreamDataType*);</span></span>



 

## <a name="parameters"></a><span data-ttu-id="5b2fa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5b2fa-106">Parameters</span></span>



| <span data-ttu-id="5b2fa-107">Element</span><span class="sxs-lookup"><span data-stu-id="5b2fa-107">Item</span></span>                                                                                                                             | <span data-ttu-id="5b2fa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5b2fa-108">Description</span></span>                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2fa-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span><span class="sxs-lookup"><span data-stu-id="5b2fa-109"><span id="StreamDataType"></span><span id="streamdatatype"></span><span id="STREAMDATATYPE"></span>**StreamDataType**</span></span><br/> | <span data-ttu-id="5b2fa-110">Eine Dateneingabebeschreibung.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-110">A data input description.</span></span> <span data-ttu-id="5b2fa-111">Diese Beschreibung muss mit dem stream-object-Vorlagenparameter namens [DataType übereinstimmen.](dx-graphics-hlsl-so-type.md)</span><span class="sxs-lookup"><span data-stu-id="5b2fa-111">This description must match the stream-object template parameter called [DataType](dx-graphics-hlsl-so-type.md).</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="5b2fa-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5b2fa-112">Return Value</span></span>

<span data-ttu-id="5b2fa-113">Keine</span><span class="sxs-lookup"><span data-stu-id="5b2fa-113">None</span></span>

## <a name="example"></a><span data-ttu-id="5b2fa-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5b2fa-114">Example</span></span>

<span data-ttu-id="5b2fa-115">Dieser Codeausschnitt (aus dem [CubeMapGS-Beispiel)](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)zeigt ein partielles Beispiel für das Anfügen von Dreiecksstreifenprimitiven an ein Streamausgabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-115">This code snippet (from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)) shows a partial example of appending triangle strip primitives to a stream-output object.</span></span>


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



## <a name="minimum-shader-model"></a><span data-ttu-id="5b2fa-116">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5b2fa-116">Minimum Shader Model</span></span>

<span data-ttu-id="5b2fa-117">Diese Funktion wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5b2fa-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="5b2fa-118">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="5b2fa-118">Shader Model</span></span>                                              | <span data-ttu-id="5b2fa-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="5b2fa-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5b2fa-120">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="5b2fa-120">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5b2fa-121">Ja</span><span class="sxs-lookup"><span data-stu-id="5b2fa-121">yes</span></span>       |
| [<span data-ttu-id="5b2fa-122">Shadermodell 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b2fa-122">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5b2fa-123">Nein</span><span class="sxs-lookup"><span data-stu-id="5b2fa-123">no</span></span>        |
| [<span data-ttu-id="5b2fa-124">Shadermodell 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b2fa-124">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5b2fa-125">Nein</span><span class="sxs-lookup"><span data-stu-id="5b2fa-125">no</span></span>        |
| [<span data-ttu-id="5b2fa-126">Shadermodell 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5b2fa-126">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5b2fa-127">Nein</span><span class="sxs-lookup"><span data-stu-id="5b2fa-127">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5b2fa-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5b2fa-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b2fa-129">Stream-Output-Objekt</span><span class="sxs-lookup"><span data-stu-id="5b2fa-129">Stream-Output Object</span></span>](dx-graphics-hlsl-so-type.md)
</dt> </dl>

 

 





