---
title: Geometry-Shader-Objekt
description: Ein geometry-shader-Objekt verarbeitet ganze Primitive. Verwenden Sie die folgende Syntax, um ein geometry-shader-Objekt zu deklarieren.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- maxvertexcount (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e06bbc184a4b5f82d5edaaf7fdbfbd55f1906f12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120615"
---
# <a name="geometry-shader-object"></a><span data-ttu-id="fdf70-105">Geometry-Shader-Objekt</span><span class="sxs-lookup"><span data-stu-id="fdf70-105">Geometry-Shader Object</span></span>

<span data-ttu-id="fdf70-106">Ein geometry-shader-Objekt verarbeitet ganze Primitive.</span><span class="sxs-lookup"><span data-stu-id="fdf70-106">A geometry-shader object processes entire primitives.</span></span> <span data-ttu-id="fdf70-107">Verwenden Sie die folgende Syntax, um ein geometry-shader-Objekt zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="fdf70-107">Use the following syntax to declare a geometry-shader object.</span></span>

<span data-ttu-id="fdf70-108">\[maxvertexcount(*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements \]*, inout *StreamOutputObject* );</span><span class="sxs-lookup"><span data-stu-id="fdf70-108">\[maxvertexcount(*NumVerts*)\] void *ShaderName* (   *PrimitiveType DataType Name \[ NumElements \]*,   inout *StreamOutputObject*  );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="fdf70-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdf70-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdf70-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span><span class="sxs-lookup"><span data-stu-id="fdf70-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span></span>
</dt> <dd>

<span data-ttu-id="fdf70-111">\[in \] Deklaration für die maximale Anzahl der zu erstellenden Scheitelzeichen.</span><span class="sxs-lookup"><span data-stu-id="fdf70-111">\[in\] Declaration for the maximum number of vertices to create.</span></span>

-   <span data-ttu-id="fdf70-112">\[maxvertexcount() \] – erforderliches Schlüsselwort; Klammern und Klammern sind erforderliche Zeichen für die richtige Syntax.</span><span class="sxs-lookup"><span data-stu-id="fdf70-112">\[maxvertexcount()\] - required keyword; brackets and parenthesis are required characters for correct syntax.</span></span>
-   <span data-ttu-id="fdf70-113">*NumVerts:* Eine ganzzahlige Zahl, die die Anzahl der Scheitelzeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="fdf70-113">*NumVerts* - An integer number representing the number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="fdf70-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span><span class="sxs-lookup"><span data-stu-id="fdf70-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span></span>
</dt> <dd>

<span data-ttu-id="fdf70-115">\[in \] Eine ASCII-Zeichenfolge, die einen eindeutigen Namen für die geometry-shader-Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="fdf70-115">\[in\] An ASCII string that contains a unique name for the geometry-shader function.</span></span>

</dd> <dt>

<span data-ttu-id="fdf70-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span><span class="sxs-lookup"><span data-stu-id="fdf70-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span></span>
</dt> <dd>

<span data-ttu-id="fdf70-117">*PrimitiveType:* Primitiver Typ, der die Reihenfolge der primitiven Daten bestimmt.</span><span class="sxs-lookup"><span data-stu-id="fdf70-117">*PrimitiveType* - Primitive type, which determines the order of the primitive data.</span></span>



| <span data-ttu-id="fdf70-118">Primitiver Typ</span><span class="sxs-lookup"><span data-stu-id="fdf70-118">Primitive Type</span></span> | <span data-ttu-id="fdf70-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdf70-119">Description</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="fdf70-120">*Punkt*</span><span class="sxs-lookup"><span data-stu-id="fdf70-120">*point*</span></span>        | <span data-ttu-id="fdf70-121">Punktliste</span><span class="sxs-lookup"><span data-stu-id="fdf70-121">Point list</span></span>                                                    |
| <span data-ttu-id="fdf70-122">*Linie*</span><span class="sxs-lookup"><span data-stu-id="fdf70-122">*line*</span></span>         | <span data-ttu-id="fdf70-123">Zeilenliste oder Linienstreifen</span><span class="sxs-lookup"><span data-stu-id="fdf70-123">Line list or line strip</span></span>                                       |
| <span data-ttu-id="fdf70-124">*Dreieck*</span><span class="sxs-lookup"><span data-stu-id="fdf70-124">*triangle*</span></span>     | <span data-ttu-id="fdf70-125">Dreiecksliste oder Dreiecksstreifen</span><span class="sxs-lookup"><span data-stu-id="fdf70-125">Triangle list or triangle strip</span></span>                               |
| <span data-ttu-id="fdf70-126">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="fdf70-126">*lineadj*</span></span>      | <span data-ttu-id="fdf70-127">Zeilenliste mit Adjacency oder Zeilenstreifen mit Adjacency</span><span class="sxs-lookup"><span data-stu-id="fdf70-127">Line list with adjacency or line strip with adjacency</span></span>         |
| <span data-ttu-id="fdf70-128">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="fdf70-128">*triangleadj*</span></span>  | <span data-ttu-id="fdf70-129">Dreiecksliste mit Adjacency oder Dreiecksstreifen mit Adjacency</span><span class="sxs-lookup"><span data-stu-id="fdf70-129">Triangle list with adjacency or triangle strip with adjacency</span></span> |



 

<span data-ttu-id="fdf70-130">*DataType*  -  \[ in \] Ein Eingabedatentyp; kann ein beliebiger [HLSL-Datentyp sein.](dx-graphics-hlsl-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="fdf70-130">*DataType* - \[in\] An input data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span>

<span data-ttu-id="fdf70-131">*Name* – Argumentname; dies ist eine ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fdf70-131">*Name* - Argument name; this is an ASCII string.</span></span>

<span data-ttu-id="fdf70-132">*NumElements:* Arraygröße der Eingabe, die vom *PrimitiveType* abhängt, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="fdf70-132">*NumElements* - Array size of the input, which depends on the *PrimitiveType* as shown in the following table.</span></span>

| <span data-ttu-id="fdf70-133">Primitiver Typ</span><span class="sxs-lookup"><span data-stu-id="fdf70-133">Primitive Type</span></span> | <span data-ttu-id="fdf70-134">NumElements</span><span class="sxs-lookup"><span data-stu-id="fdf70-134">NumElements</span></span>                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf70-135">*Punkt*</span><span class="sxs-lookup"><span data-stu-id="fdf70-135">*point*</span></span>        | <span data-ttu-id="fdf70-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="fdf70-136">\[1\]</span></span><br/> <span data-ttu-id="fdf70-137">Sie arbeiten nur an einem Punkt nach dem anderen.</span><span class="sxs-lookup"><span data-stu-id="fdf70-137">You operate on only one point at a time.</span></span><br/>                                         |
| <span data-ttu-id="fdf70-138">*Linie*</span><span class="sxs-lookup"><span data-stu-id="fdf70-138">*line*</span></span>         | <span data-ttu-id="fdf70-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="fdf70-139">\[2\]</span></span><br/> <span data-ttu-id="fdf70-140">Eine Zeile erfordert zwei Scheitellinien.</span><span class="sxs-lookup"><span data-stu-id="fdf70-140">A line requires two vertices.</span></span><br/>                                                    |
| <span data-ttu-id="fdf70-141">*Dreieck*</span><span class="sxs-lookup"><span data-stu-id="fdf70-141">*triangle*</span></span>     | <span data-ttu-id="fdf70-142">\[3\]</span><span class="sxs-lookup"><span data-stu-id="fdf70-142">\[3\]</span></span><br/> <span data-ttu-id="fdf70-143">Ein Dreieck erfordert drei Scheitelungen.</span><span class="sxs-lookup"><span data-stu-id="fdf70-143">A triangle requires three vertices.</span></span><br/>                                              |
| <span data-ttu-id="fdf70-144">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="fdf70-144">*lineadj*</span></span>      | <span data-ttu-id="fdf70-145">\[4\]</span><span class="sxs-lookup"><span data-stu-id="fdf70-145">\[4\]</span></span><br/> <span data-ttu-id="fdf70-146">Ein lineadj hat zwei Enden; daher sind vier Scheitelungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fdf70-146">A lineadj has two ends; therefore, it requires four vertices.</span></span><br/>                    |
| <span data-ttu-id="fdf70-147">*triangleadj*</span><span class="sxs-lookup"><span data-stu-id="fdf70-147">*triangleadj*</span></span>  | <span data-ttu-id="fdf70-148">\[6\]</span><span class="sxs-lookup"><span data-stu-id="fdf70-148">\[6\]</span></span><br/> <span data-ttu-id="fdf70-149">Ein Dreieckadj grenzt an drei weitere Dreiecke; daher sind sechs Scheiteltices erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fdf70-149">A triangleadj borders three more triangles; therefore, it requires six vertices.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fdf70-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span><span class="sxs-lookup"><span data-stu-id="fdf70-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span></span>
</dt> <dd>

<span data-ttu-id="fdf70-151">Die Deklaration des [Streamausgabeobjekts](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="fdf70-151">The declaration of the [stream-output object](dx-graphics-hlsl-so-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdf70-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fdf70-152">Return Value</span></span>

<span data-ttu-id="fdf70-153">Keine</span><span class="sxs-lookup"><span data-stu-id="fdf70-153">None</span></span>

## <a name="remarks"></a><span data-ttu-id="fdf70-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fdf70-154">Remarks</span></span>

<span data-ttu-id="fdf70-155">Das folgende Diagramm zeigt die verschiedenen primitiven Typen für ein Geometrie-Shaderobjekt.</span><span class="sxs-lookup"><span data-stu-id="fdf70-155">The following diagram shows the various primitive types for a geometry shader object.</span></span>

![Abbildung der verschiedenen primitiven Typen für ein Geometrie-Shaderobjekt](images/d3d11-gsinputs1.png)

<span data-ttu-id="fdf70-157">Das folgende Diagramm zeigt Geometry-Shaderaufrufe.</span><span class="sxs-lookup"><span data-stu-id="fdf70-157">The following diagram shows geometry shader invocations.</span></span>

![Abbildung von Geometry-Shaderaufrufen](images/d3d11-gsinputs2.png)

## <a name="examples"></a><span data-ttu-id="fdf70-159">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdf70-159">Examples</span></span>

<span data-ttu-id="fdf70-160">Dieses Beispiel ist aus Übung 1 des [Direct3D 10 Shader Model 4.0 Workshop.](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="fdf70-160">This example is from exercise 1 from the [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span></span>


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a><span data-ttu-id="fdf70-161">Minimales Shadermodell</span><span class="sxs-lookup"><span data-stu-id="fdf70-161">Minimum Shader Model</span></span>

<span data-ttu-id="fdf70-162">Dieses Objekt wird in den folgenden Shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fdf70-162">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="fdf70-163">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="fdf70-163">Shader Model</span></span>                                                        | <span data-ttu-id="fdf70-164">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="fdf70-164">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="fdf70-165">[Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher– Shadermodelle</span><span class="sxs-lookup"><span data-stu-id="fdf70-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="fdf70-166">Ja</span><span class="sxs-lookup"><span data-stu-id="fdf70-166">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="fdf70-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fdf70-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdf70-168">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="fdf70-168">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





