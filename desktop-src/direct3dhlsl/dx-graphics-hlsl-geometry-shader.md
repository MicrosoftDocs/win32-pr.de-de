---
title: Geometry-Shader-Objekt
description: Ein Geometry-Shader-Objekt verarbeitet ganze primitive. Verwenden Sie die folgende Syntax, um ein Geometry-Shader-Objekt zu deklarieren.
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
ms.openlocfilehash: dadb0e8bb3ddda16305ac701b34523668bd9c1a5
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "103719752"
---
# <a name="geometry-shader-object"></a><span data-ttu-id="c3615-105">Geometry-Shader-Objekt</span><span class="sxs-lookup"><span data-stu-id="c3615-105">Geometry-Shader Object</span></span>

<span data-ttu-id="c3615-106">Ein Geometry-Shader-Objekt verarbeitet ganze primitive.</span><span class="sxs-lookup"><span data-stu-id="c3615-106">A geometry-shader object processes entire primitives.</span></span> <span data-ttu-id="c3615-107">Verwenden Sie die folgende Syntax, um ein Geometry-Shader-Objekt zu deklarieren.</span><span class="sxs-lookup"><span data-stu-id="c3615-107">Use the following syntax to declare a geometry-shader object.</span></span>



|                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3615-108">\[maxvertexcount (*numverts*) \] void *shadername* ( *PrimitiveType DataType Name \[ numElements \]*, INOUT *streamoutputobject* );</span><span class="sxs-lookup"><span data-stu-id="c3615-108">\[maxvertexcount(*NumVerts*)\] void *ShaderName* (   *PrimitiveType DataType Name \[ NumElements \]*,   inout *StreamOutputObject*  );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="c3615-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3615-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3615-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount (*numverts*)\]</span><span class="sxs-lookup"><span data-stu-id="c3615-110"><span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]</span></span>
</dt> <dd>

<span data-ttu-id="c3615-111">\[in \] der Deklaration für die maximale Anzahl der zu erstellenden Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="c3615-111">\[in\] Declaration for the maximum number of vertices to create.</span></span>

-   <span data-ttu-id="c3615-112">\[maxvertexcount () \] : Erforderliches Schlüsselwort; eckige Klammern und Klammer sind erforderliche Zeichen für die korrekte Syntax.</span><span class="sxs-lookup"><span data-stu-id="c3615-112">\[maxvertexcount()\] - required keyword; brackets and parenthesis are required characters for correct syntax.</span></span>
-   <span data-ttu-id="c3615-113">*Numverts* -eine ganzzahlige Zahl, die die Anzahl der Vertices darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3615-113">*NumVerts* - An integer number representing the number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="c3615-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*Shadername*</span><span class="sxs-lookup"><span data-stu-id="c3615-114"><span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*</span></span>
</dt> <dd>

<span data-ttu-id="c3615-115">\[in \] einer ASCII-Zeichenfolge, die einen eindeutigen Namen für die Geometry-Shader-Funktion enthält.</span><span class="sxs-lookup"><span data-stu-id="c3615-115">\[in\] An ASCII string that contains a unique name for the geometry-shader function.</span></span>

</dd> <dt>

<span data-ttu-id="c3615-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ numElements \]*</span><span class="sxs-lookup"><span data-stu-id="c3615-116"><span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*</span></span>
</dt> <dd>

<span data-ttu-id="c3615-117">*PrimitiveType* : primitiver Typ, der die Reihenfolge der primitiven Daten bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c3615-117">*PrimitiveType* - Primitive type, which determines the order of the primitive data.</span></span>



| <span data-ttu-id="c3615-118">Primitiver Typ</span><span class="sxs-lookup"><span data-stu-id="c3615-118">Primitive Type</span></span> | <span data-ttu-id="c3615-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3615-119">Description</span></span>                                                   |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="c3615-120">*Punkt*</span><span class="sxs-lookup"><span data-stu-id="c3615-120">*point*</span></span>        | <span data-ttu-id="c3615-121">Punkt Liste</span><span class="sxs-lookup"><span data-stu-id="c3615-121">Point list</span></span>                                                    |
| <span data-ttu-id="c3615-122">*Stimmen*</span><span class="sxs-lookup"><span data-stu-id="c3615-122">*line*</span></span>         | <span data-ttu-id="c3615-123">Zeilen-oder Zeilen Streifen</span><span class="sxs-lookup"><span data-stu-id="c3615-123">Line list or line strip</span></span>                                       |
| <span data-ttu-id="c3615-124">*Triangle*</span><span class="sxs-lookup"><span data-stu-id="c3615-124">*triangle*</span></span>     | <span data-ttu-id="c3615-125">Dreiecks Liste oder Dreiecks Leiste</span><span class="sxs-lookup"><span data-stu-id="c3615-125">Triangle list or triangle strip</span></span>                               |
| <span data-ttu-id="c3615-126">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="c3615-126">*lineadj*</span></span>      | <span data-ttu-id="c3615-127">Zeilen Liste mit der Nähe oder dem Zeilen Streifen mit der Nähe</span><span class="sxs-lookup"><span data-stu-id="c3615-127">Line list with adjacency or line strip with adjacency</span></span>         |
| <span data-ttu-id="c3615-128">*"-adangleadj"*</span><span class="sxs-lookup"><span data-stu-id="c3615-128">*triangleadj*</span></span>  | <span data-ttu-id="c3615-129">Dreiecks Liste mit der Nähe oder dem Dreiecks Streifen mit der Nähe</span><span class="sxs-lookup"><span data-stu-id="c3615-129">Triangle list with adjacency or triangle strip with adjacency</span></span> |



 

<span data-ttu-id="c3615-130">*DataType*  -  \[ in \] einem Eingabe Datentyp kann ein beliebiger [HLSL-Datentyp](dx-graphics-hlsl-data-types.md)sein.</span><span class="sxs-lookup"><span data-stu-id="c3615-130">*DataType* - \[in\] An input data type; can be any [HLSL data type](dx-graphics-hlsl-data-types.md).</span></span>

<span data-ttu-id="c3615-131">*Name* : Argument Name; Dies ist eine ASCII-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c3615-131">*Name* - Argument name; this is an ASCII string.</span></span>

<span data-ttu-id="c3615-132">*NumElements* : Array Größe der Eingabe, die von *PrimitiveType* abhängig ist, wie in der folgenden Tabelle gezeigt.</span><span class="sxs-lookup"><span data-stu-id="c3615-132">*NumElements* - Array size of the input, which depends on the *PrimitiveType* as shown in the following table.</span></span>

| <span data-ttu-id="c3615-133">Primitiver Typ</span><span class="sxs-lookup"><span data-stu-id="c3615-133">Primitive Type</span></span> | <span data-ttu-id="c3615-134">NumElements</span><span class="sxs-lookup"><span data-stu-id="c3615-134">NumElements</span></span>                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3615-135">*Punkt*</span><span class="sxs-lookup"><span data-stu-id="c3615-135">*point*</span></span>        | <span data-ttu-id="c3615-136">\[1\]</span><span class="sxs-lookup"><span data-stu-id="c3615-136">\[1\]</span></span><br/> <span data-ttu-id="c3615-137">Sie arbeiten jeweils nur auf einem Punkt.</span><span class="sxs-lookup"><span data-stu-id="c3615-137">You operate on only one point at a time.</span></span><br/>                                         |
| <span data-ttu-id="c3615-138">*Stimmen*</span><span class="sxs-lookup"><span data-stu-id="c3615-138">*line*</span></span>         | <span data-ttu-id="c3615-139">\[2\]</span><span class="sxs-lookup"><span data-stu-id="c3615-139">\[2\]</span></span><br/> <span data-ttu-id="c3615-140">Eine Zeile erfordert zwei Vertices.</span><span class="sxs-lookup"><span data-stu-id="c3615-140">A line requires two vertices.</span></span><br/>                                                    |
| <span data-ttu-id="c3615-141">*Triangle*</span><span class="sxs-lookup"><span data-stu-id="c3615-141">*triangle*</span></span>     | <span data-ttu-id="c3615-142">\[3\]</span><span class="sxs-lookup"><span data-stu-id="c3615-142">\[3\]</span></span><br/> <span data-ttu-id="c3615-143">Ein Dreieck erfordert drei Vertices.</span><span class="sxs-lookup"><span data-stu-id="c3615-143">A triangle requires three vertices.</span></span><br/>                                              |
| <span data-ttu-id="c3615-144">*lineadj*</span><span class="sxs-lookup"><span data-stu-id="c3615-144">*lineadj*</span></span>      | <span data-ttu-id="c3615-145">\[4\]</span><span class="sxs-lookup"><span data-stu-id="c3615-145">\[4\]</span></span><br/> <span data-ttu-id="c3615-146">Ein lineadj hat zwei Ende. Daher sind vier Vertices erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3615-146">A lineadj has two ends; therefore, it requires four vertices.</span></span><br/>                    |
| <span data-ttu-id="c3615-147">*"-adangleadj"*</span><span class="sxs-lookup"><span data-stu-id="c3615-147">*triangleadj*</span></span>  | <span data-ttu-id="c3615-148">\[6\]</span><span class="sxs-lookup"><span data-stu-id="c3615-148">\[6\]</span></span><br/> <span data-ttu-id="c3615-149">Ein "dreiangleadj"-Rahmen drei weitere Dreiecke Daher sind sechs Vertices erforderlich.</span><span class="sxs-lookup"><span data-stu-id="c3615-149">A triangleadj borders three more triangles; therefore, it requires six vertices.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c3615-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*Streamoutputobject*</span><span class="sxs-lookup"><span data-stu-id="c3615-150"><span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*</span></span>
</dt> <dd>

<span data-ttu-id="c3615-151">Die Deklaration des [Stream-Output-Objekts](dx-graphics-hlsl-so-type.md).</span><span class="sxs-lookup"><span data-stu-id="c3615-151">The declaration of the [stream-output object](dx-graphics-hlsl-so-type.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3615-152">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c3615-152">Return Value</span></span>

<span data-ttu-id="c3615-153">Keine</span><span class="sxs-lookup"><span data-stu-id="c3615-153">None</span></span>

## <a name="remarks"></a><span data-ttu-id="c3615-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3615-154">Remarks</span></span>

<span data-ttu-id="c3615-155">Das folgende Diagramm zeigt die verschiedenen primitiven Typen für ein Geometry-Shader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c3615-155">The following diagram shows the various primitive types for a geometry shader object.</span></span>

![Darstellung der verschiedenen primitiven Typen für ein Geometry-Shader-Objekt](images/d3d11-gsinputs1.png)

<span data-ttu-id="c3615-157">Das folgende Diagramm zeigt die Geometrie-Shader-Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="c3615-157">The following diagram shows geometry shader invocations.</span></span>

![Abbildung der Geometrie-Shader-Aufrufe](images/d3d11-gsinputs2.png)

## <a name="examples"></a><span data-ttu-id="c3615-159">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3615-159">Examples</span></span>

<span data-ttu-id="c3615-160">Dieses Beispiel basiert auf Übung 1 aus dem [Direct3D 10-Shader Model 4,0-Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="c3615-160">This example is from exercise 1 from the [Direct3D 10 Shader Model 4.0 Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).</span></span>


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



## <a name="minimum-shader-model"></a><span data-ttu-id="c3615-161">Minimaler Shader-Modell</span><span class="sxs-lookup"><span data-stu-id="c3615-161">Minimum Shader Model</span></span>

<span data-ttu-id="c3615-162">Dieses Objekt wird in den folgenden shadermodellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c3615-162">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="c3615-163">Shadermodell</span><span class="sxs-lookup"><span data-stu-id="c3615-163">Shader Model</span></span>                                                        | <span data-ttu-id="c3615-164">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="c3615-164">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="c3615-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle</span><span class="sxs-lookup"><span data-stu-id="c3615-165">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="c3615-166">ja</span><span class="sxs-lookup"><span data-stu-id="c3615-166">yes</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="c3615-167">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c3615-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3615-168">Shadermodell 4</span><span class="sxs-lookup"><span data-stu-id="c3615-168">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





