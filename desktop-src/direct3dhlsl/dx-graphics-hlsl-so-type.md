---
title: Stream-Output-Objekt
description: Ein Stream-Output-Objekt ist ein Vorlagen Objekt, das Daten aus der Geometrie-Shader-Stufe streamt. Verwenden Sie die folgende Syntax, um ein Stream-Output-Objekt zu deklarieren.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98063ddb45633dda6c897abf0f82f29a394c3f95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390469"
---
# <a name="stream-output-object"></a><span data-ttu-id="62676-104">Stream-Output-Objekt</span><span class="sxs-lookup"><span data-stu-id="62676-104">Stream-Output Object</span></span>

<span data-ttu-id="62676-105">Ein Stream-Output-Objekt ist ein Vorlagen Objekt, das Daten aus der [Geometrie-Shader-Stufe](/previous-versions//bb205146(v=vs.85))streamt.</span><span class="sxs-lookup"><span data-stu-id="62676-105">A stream-output object is a templated object that streams data out of the [geometry-shader stage](/previous-versions//bb205146(v=vs.85)).</span></span> <span data-ttu-id="62676-106">Verwenden Sie die folgende Syntax, um ein Stream-Output-Objekt zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="62676-106">Use the following syntax to declare a stream-output object.</span></span>



| <span data-ttu-id="62676-107">INOUT *streamoutputobject* < *DataType* >  *Name;*</span><span class="sxs-lookup"><span data-stu-id="62676-107">inout *StreamOutputObject*<*DataType*> *Name;*</span></span> |
|------------------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="62676-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="62676-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62676-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*Streamoutputobject*  <  *DataType*  >    *Name*</span><span class="sxs-lookup"><span data-stu-id="62676-109"><span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject* < *DataType* >   *Name*</span></span>
</dt> <dd>

<span data-ttu-id="62676-110">Die Deklaration des Stream-Output-Objekts (so).</span><span class="sxs-lookup"><span data-stu-id="62676-110">The stream-output object (SO) declaration.</span></span>



| <span data-ttu-id="62676-111">Stream-Output von Objekttypen</span><span class="sxs-lookup"><span data-stu-id="62676-111">Stream-Output Object Types</span></span> | <span data-ttu-id="62676-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62676-112">Description</span></span>                       |
|----------------------------|-----------------------------------|
| <span data-ttu-id="62676-113">*Pointstream*</span><span class="sxs-lookup"><span data-stu-id="62676-113">*PointStream*</span></span>              | <span data-ttu-id="62676-114">Eine Sequenz von Punkt primitiven</span><span class="sxs-lookup"><span data-stu-id="62676-114">A sequence of point primitives</span></span>    |
| <span data-ttu-id="62676-115">*LineStream*</span><span class="sxs-lookup"><span data-stu-id="62676-115">*LineStream*</span></span>               | <span data-ttu-id="62676-116">Eine Sequenz von Zeilen primitiven</span><span class="sxs-lookup"><span data-stu-id="62676-116">A sequence of line primitives</span></span>     |
| <span data-ttu-id="62676-117">*"Test-Stream"*</span><span class="sxs-lookup"><span data-stu-id="62676-117">*TriangleStream*</span></span>           | <span data-ttu-id="62676-118">Eine Sequenz von Dreiecks primitiven</span><span class="sxs-lookup"><span data-stu-id="62676-118">A sequence of triangle primitives</span></span> |



 

<span data-ttu-id="62676-119">*DataType* -Output-Datentyp; kann ein beliebiger [HLSL-Datentyp](dx-graphics-hlsl-data-types.md)sein.</span><span class="sxs-lookup"><span data-stu-id="62676-119">*DataType* - Output data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span> <span data-ttu-id="62676-120">Muss von den spitzen Klammern umgeben sein.</span><span class="sxs-lookup"><span data-stu-id="62676-120">Must be surrounded by the angle brackets.</span></span>

<span data-ttu-id="62676-121">*Name* : Variablenname; eine ASCII-Zeichenfolge, die das-Objekt eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="62676-121">*Name* - Variable name; an ASCII string that uniquely identifies the object.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="62676-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="62676-122">Example</span></span>

<span data-ttu-id="62676-123">Dies ist ein Beispiel für eine Datenstrom Ausgabe-Objekt Deklaration, die Dreiecks primitive ausgibt, deren Daten durch die PS- \_ cubemap in der Struktur definiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="62676-123">This is an example of a stream-output object declaration that streams out triangle primitives whose data is defined by the PS\_CUBEMAP\_IN structure.</span></span> <span data-ttu-id="62676-124">Der Geometry-Shader ist auf das Erstellen von 18 Vertices beschränkt.</span><span class="sxs-lookup"><span data-stu-id="62676-124">The geometry-shader is limited to generating 18 vertices.</span></span>


```
struct PS_CUBEMAP_IN
{
    float4 Pos : SV_POSITION;     // Projection coord
    float2 Tex : TEXCOORD0;       // Texture coord
    uint RTIndex : SV_RenderTargetArrayIndex;
};

[maxvertexcount(18)]
void main( inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream, triangle PS_CUBEMAP_INT[3] )
{
    ...
}
```



<span data-ttu-id="62676-125">Dies ist ein Code Ausschnitt aus dem [cubemapgs-Beispiel](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="62676-125">This is a code snippet from the [CubeMapGS Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).</span></span>

## <a name="stream-output-object-methods"></a><span data-ttu-id="62676-126">Stream-Output-Objektmethoden</span><span class="sxs-lookup"><span data-stu-id="62676-126">Stream-Output Object Methods</span></span>

<span data-ttu-id="62676-127">Verwenden Sie die folgende Syntax, um Stream-Output-Object-Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="62676-127">Use the following syntax to call stream-output-object methods.</span></span>


```
Object.Method
```



<span data-ttu-id="62676-128">Die folgenden Methoden werden implementiert.</span><span class="sxs-lookup"><span data-stu-id="62676-128">The following methods are implemented.</span></span>



| <span data-ttu-id="62676-129">Methoden</span><span class="sxs-lookup"><span data-stu-id="62676-129">Methods</span></span>                                              | <span data-ttu-id="62676-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62676-130">Description</span></span>                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="62676-131">Append</span><span class="sxs-lookup"><span data-stu-id="62676-131">Append</span></span>](dx-graphics-hlsl-so-append.md)             | <span data-ttu-id="62676-132">Anfügen von Ausgabedaten an einen vorhandenen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="62676-132">Append output data to an existing stream.</span></span>                        |
| [<span data-ttu-id="62676-133">Restartstrip</span><span class="sxs-lookup"><span data-stu-id="62676-133">RestartStrip</span></span>](dx-graphics-hlsl-so-restartstrip.md) | <span data-ttu-id="62676-134">Beenden Sie den aktuellen primitiven Bereich, und starten Sie einen neuen primitiven Strip.</span><span class="sxs-lookup"><span data-stu-id="62676-134">End the current primitive strip and start a new primitive strip.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="62676-135">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="62676-135">Minimum Shader Model</span></span>

<span data-ttu-id="62676-136">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="62676-136">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="62676-137">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="62676-137">Shader Model</span></span>                                                        | <span data-ttu-id="62676-138">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="62676-138">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="62676-139">[Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="62676-139">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="62676-140">ja</span><span class="sxs-lookup"><span data-stu-id="62676-140">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="62676-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="62676-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62676-142">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="62676-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 