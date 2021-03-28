---
title: Entwerfen eines Hull-Shaders
description: In diesem Thema wird gezeigt, wie ein Hull-Shader entworfen wird.
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ece816ae33e7f4ecf4d024098e7741f197c423f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993375"
---
# <a name="how-to-design-a-hull-shader"></a><span data-ttu-id="e1e13-103">Gewusst wie: Entwerfen eines Hull-Shaders</span><span class="sxs-lookup"><span data-stu-id="e1e13-103">How To: Design a Hull Shader</span></span>

<span data-ttu-id="e1e13-104">Ein Hull-Shader ist die erste von drei Phasen, die zusammenarbeiten, um Mosaik [zu implementieren (](direct3d-11-advanced-stages-tessellation.md) die beiden anderen Phasen sind der Mosaik-und Domänen-Shader).</span><span class="sxs-lookup"><span data-stu-id="e1e13-104">A hull shader is the first of three stages that work together to implement [tessellation](direct3d-11-advanced-stages-tessellation.md) (the other two stages are the tessellator and a domain shader).</span></span> <span data-ttu-id="e1e13-105">In diesem Thema wird gezeigt, wie ein Hull-Shader entworfen wird.</span><span class="sxs-lookup"><span data-stu-id="e1e13-105">This topics shows how to design a hull shader.</span></span>

<span data-ttu-id="e1e13-106">Ein Hull-Shader erfordert zwei Funktionen: den Haupt-Hull-Shader und eine Patch-konstantenfunktion.</span><span class="sxs-lookup"><span data-stu-id="e1e13-106">A hull shader requires two functions, the main hull shader and a patch constant function.</span></span> <span data-ttu-id="e1e13-107">Der Hull-Shader implementiert Berechnungen für jeden Steuerungspunkt. der Hull-Shader ruft auch die Patch-Konstante Funktion auf, die Berechnungen für die einzelnen Patches implementiert.</span><span class="sxs-lookup"><span data-stu-id="e1e13-107">The hull shader implements calculations on each control point; the hull shader also calls the patch constant function which implements calculations on each patch.</span></span>

<span data-ttu-id="e1e13-108">Nachdem Sie einen Hull-Shader entworfen haben, finden Sie weitere Informationen unter Gewusst [wie: Erstellen](direct3d-11-advanced-stages-hull-shader-create.md) eines Hull-Shaders, um zu erfahren, wie ein Hull-Shader erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e1e13-108">After you have designed a hull shader, see [How To: Create a Hull Shader](direct3d-11-advanced-stages-hull-shader-create.md) to learn how to create a hull shader.</span></span>

<span data-ttu-id="e1e13-109">**So entwerfen Sie einen Hull-Shader**</span><span class="sxs-lookup"><span data-stu-id="e1e13-109">**To design a hull shader**</span></span>

1.  <span data-ttu-id="e1e13-110">Definieren des Hull-Shader-Eingabe Steuer Elements und von Ausgabe Steuerungs Punkten.</span><span class="sxs-lookup"><span data-stu-id="e1e13-110">Define hull shader input control and output control points.</span></span>

    ```
    // Input control point
    struct VS_CONTROL_POINT_OUTPUT
    {
        float3 vPosition : WORLDPOS;
        float2 vUV       : TEXCOORD0;
        float3 vTangent  : TANGENT;
    };

    // Output control point
    struct BEZIER_CONTROL_POINT
    {
        float3 vPosition    : BEZIERPOS;
    };
    ```

    

2.  <span data-ttu-id="e1e13-111">Definiert die Daten der Ausgabe Patch-Konstante.</span><span class="sxs-lookup"><span data-stu-id="e1e13-111">Define output patch constant data.</span></span>

    ```
    // Output patch constant data.
    struct HS_CONSTANT_DATA_OUTPUT
    {
        float Edges[4]        : SV_TessFactor;
        float Inside[2]       : SV_InsideTessFactor;
        
        float3 vTangent[4]    : TANGENT;
        float2 vUV[4]         : TEXCOORD;
        float3 vTanUCorner[4] : TANUCORNER;
        float3 vTanVCorner[4] : TANVCORNER;
        float4 vCWts          : TANWEIGHTS;
    };
    ```

    

    <span data-ttu-id="e1e13-112">Bei einer vierfach Domäne definiert der [SV- \_ tmosaik-Faktor](/windows/desktop/direct3dhlsl/sv-tessfactor) vier Edge-Mosaik Faktoren (um die Ränder zu Mosaik), da der Mosaik-Mosaik Faktor wissen muss, wie viel im Mosaik Prozess festgelegt werden muss.</span><span class="sxs-lookup"><span data-stu-id="e1e13-112">For a quad domain, [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) defines 4 edge tessellation factors (to tessellate the edges), since the fixed function tessellator needs to know how much to tessellate.</span></span> <span data-ttu-id="e1e13-113">Die erforderlichen Ausgaben unterscheiden sich für die Dreiecks-und isolin-Domänen.</span><span class="sxs-lookup"><span data-stu-id="e1e13-113">The required outputs are different for the triangle and isoline domains.</span></span>

    <span data-ttu-id="e1e13-114">Der Mosaik-Mosaik Ausdruck untersucht keine anderen Hull-shaderausgaben, wie z. b. andere patchkonstantendaten oder einen der Steuerungs Punkte.</span><span class="sxs-lookup"><span data-stu-id="e1e13-114">The fixed function tessellator doesn't look at any other hull shader outputs, such as other patch constant data or any of the control points.</span></span> <span data-ttu-id="e1e13-115">Der Domänen-Shader, der für jeden Punkt aufgerufen wird, der vom tmosaik-Debugger generiert wird--wird als Eingabe alle Ausgabe Steuerungs Punkte des Hull-Shader und alle Ausgabe Patch-konstantendaten angezeigt. der Shader wertet den Patch an seinem Speicherort aus.</span><span class="sxs-lookup"><span data-stu-id="e1e13-115">The domain shader -- which is invoked for each point the fixed function tessellator generates -- will see as its input all the hull shader's output control points and all the output patch constant data; the shader evaluates the patch at its location.</span></span>

3.  <span data-ttu-id="e1e13-116">Definieren Sie eine Patch-Konstante Funktion.</span><span class="sxs-lookup"><span data-stu-id="e1e13-116">Define a patch constant function.</span></span> <span data-ttu-id="e1e13-117">Eine Patch-konstantenfunktion wird einmal für jeden Patch ausgeführt, um alle Daten zu berechnen, die für den gesamten Patch konstant sind (im Gegensatz zu den Daten im Rumpf-Shader).</span><span class="sxs-lookup"><span data-stu-id="e1e13-117">A patch constant function executes once for each patch to calculate any data that is constant for the entire patch (as opposed to per-control point data, which is computed in the hull shader).</span></span>

    ```
    
    #define MAX_POINTS 32

    // Patch Constant Function
    HS_CONSTANT_DATA_OUTPUT SubDToBezierConstantsHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip,
        uint PatchID : SV_PrimitiveID )
    {   
        HS_CONSTANT_DATA_OUTPUT Output;

        // Insert code to compute Output here
        
        return Output;
    }
    ```

    

    <span data-ttu-id="e1e13-118">Zu den Eigenschaften der Patch-konstantenfunktion gehören:</span><span class="sxs-lookup"><span data-stu-id="e1e13-118">Properties of the patch constant function include:</span></span>

    -   <span data-ttu-id="e1e13-119">Eine Eingabe gibt eine Variable an, die eine Patch-ID enthält, und wird durch den System Wert **SV \_ primitiveid** identifiziert (siehe [Semantik](../direct3dhlsl/dx-graphics-hlsl-semantics.md) in Shader Model 4).</span><span class="sxs-lookup"><span data-stu-id="e1e13-119">One input specifies a variable containing a patch id, and is identified by the **SV\_PrimitiveID** system value (see [semantics](../direct3dhlsl/dx-graphics-hlsl-semantics.md) in shader model 4).</span></span>
    -   <span data-ttu-id="e1e13-120">Ein Eingabeparameter ist die Eingabe Steuerungs Punkte, die in diesem Beispiel in der **vs- \_ Steuerungs \_ Punkt \_ Ausgabe** deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="e1e13-120">One input parameter is the input control points, declared in **VS\_CONTROL\_POINT\_OUTPUT** in this example.</span></span> <span data-ttu-id="e1e13-121">Eine patchfunktion kann alle Eingabe Steuerungs Punkte für jeden Patch sehen. in diesem Beispiel gibt es 32-Kontrollpunkte pro Patch.</span><span class="sxs-lookup"><span data-stu-id="e1e13-121">A patch function can see all the input control points for each patch, there are 32 control points per patch in this example.</span></span>
    -   <span data-ttu-id="e1e13-122">Die-Funktion muss mindestens pro Patch-Mosaik Faktoren für die Mosaik Stufe berechnen, die mit [SV \_ Tess Factor](/windows/desktop/direct3dhlsl/sv-tessfactor)identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e1e13-122">As a minimum, the function must calculate per-patch tessellation factors for the tessellator stage which are identified with [SV\_TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor).</span></span> <span data-ttu-id="e1e13-123">Für eine Quad-Domäne sind vier Mosaik Faktoren für die Ränder und zwei zusätzliche Faktoren (identifiziert durch [SV \_ insidetess Factor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) erforderlich, um das Mosaik Ende des Patches zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="e1e13-123">A quad domain requires four tessellation factors for the edges and two additional factors (identified by [SV\_InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) for tessellating the inside of the patch.</span></span> <span data-ttu-id="e1e13-124">Der Mosaik-Mosaik Ausdruck untersucht keine anderen Hull-shaderausgaben (z. b. die Patch-konstantendaten oder eines der Steuerpunkte).</span><span class="sxs-lookup"><span data-stu-id="e1e13-124">The fixed function tessellator doesn't look at any other hull shader outputs (such as the patch constant data or any of the control points).</span></span>
    -   <span data-ttu-id="e1e13-125">Die Ausgaben werden normalerweise durch eine-Struktur definiert und in diesem Beispiel durch die **\_ \_ Daten \_ Ausgabe der HS-Konstante** identifiziert. die Struktur hängt vom Domänentyp ab und unterscheidet sich von den Domänen Typen.</span><span class="sxs-lookup"><span data-stu-id="e1e13-125">The outputs are usually defined by a structure and is identified by **HS\_CONSTANT\_DATA\_OUTPUT** in this example; the structure depends on the domain type and would be different for triangle or isoline domains.</span></span>

    <span data-ttu-id="e1e13-126">Ein Domänen-Shader auf der anderen Seite wird für jeden Punkt aufgerufen, den der tmosaik-Debugger generiert hat, und er muss die Ausgabe Steuerungs Punkte und die Ausgabe-Patch-konstantendaten (beides aus dem Hull-Shader) anzeigen, um einen Patch an seinem Speicherort auszuwerten.</span><span class="sxs-lookup"><span data-stu-id="e1e13-126">A domain shader on the other hand is invoked for each point the fixed function tessellator generates and needs to see the output control points and the output patch constant data (both from the hull shader) to evaluate a patch at its location.</span></span>

4.  <span data-ttu-id="e1e13-127">Definieren Sie einen Hull-Shader.</span><span class="sxs-lookup"><span data-stu-id="e1e13-127">Define a hull shader.</span></span> <span data-ttu-id="e1e13-128">Ein Hull-Shader identifiziert die Eigenschaften eines Patches, einschließlich einer Patch-konstantenfunktion.</span><span class="sxs-lookup"><span data-stu-id="e1e13-128">A hull shader identifies the properties of a patch including a patch constant function.</span></span> <span data-ttu-id="e1e13-129">Ein Hull-Shader wird für jeden Ausgabe Steuerungspunkt einmal aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e1e13-129">A hull shader is invoked once for each output control point.</span></span>

    ```
    [domain("quad")]
    [partitioning("integer")]
    [outputtopology("triangle_cw")]
    [outputcontrolpoints(16)]
    [patchconstantfunc("SubDToBezierConstantsHS")]
    BEZIER_CONTROL_POINT SubDToBezierHS( 
        InputPatch<VS_CONTROL_POINT_OUTPUT, MAX_POINTS> ip, 
        uint i : SV_OutputControlPointID,
        uint PatchID : SV_PrimitiveID )
    {
        VS_CONTROL_POINT_OUTPUT Output;

        // Insert code to compute Output here.
        
        return Output;
    }
    ```

    

    <span data-ttu-id="e1e13-130">Ein Hull-Shader verwendet die folgenden Attribute:</span><span class="sxs-lookup"><span data-stu-id="e1e13-130">A hull shader uses the following attributes:</span></span>

    -   <span data-ttu-id="e1e13-131">Ein [Domänen](/windows/desktop/direct3dhlsl/sm5-attributes-domain) Attribut.</span><span class="sxs-lookup"><span data-stu-id="e1e13-131">A [domain](/windows/desktop/direct3dhlsl/sm5-attributes-domain) attribute.</span></span>
    -   <span data-ttu-id="e1e13-132">Ein [Partitionierungs](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) Attribut.</span><span class="sxs-lookup"><span data-stu-id="e1e13-132">A [partitioning](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) attribute.</span></span>
    -   <span data-ttu-id="e1e13-133">Ein [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="e1e13-133">An [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) attribute.</span></span>
    -   <span data-ttu-id="e1e13-134">Ein [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="e1e13-134">An [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) attribute.</span></span>
    -   <span data-ttu-id="e1e13-135">Ein [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) -Attribut.</span><span class="sxs-lookup"><span data-stu-id="e1e13-135">A [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) attribute.</span></span> <span data-ttu-id="e1e13-136">Ein Hull-Shader berechnet Ausgabe Steuerungs Punkte, es gibt in diesem Beispiel 16 Ausgabe Bezier-Steuerungs Punkte.</span><span class="sxs-lookup"><span data-stu-id="e1e13-136">A hull shader calculates output control points, there are 16 output Bezier control points in this example.</span></span>

<span data-ttu-id="e1e13-137">Alle Eingabe Steuerungs Punkte (die durch die **vs- \_ Steuerungs \_ Punkt \_ Ausgabe** identifiziert werden) sind für jeden Hull-Shader-Aufruf sichtbar.</span><span class="sxs-lookup"><span data-stu-id="e1e13-137">All the input control points (identified by **VS\_CONTROL\_POINT\_OUTPUT**) are visible to each hull shader invocation.</span></span> <span data-ttu-id="e1e13-138">In diesem Beispiel gibt es 32-Eingabe Steuerungs Punkte.</span><span class="sxs-lookup"><span data-stu-id="e1e13-138">In this example, there are 32 input control points.</span></span>

<span data-ttu-id="e1e13-139">Ein Hull-Shader wird einmal pro Ausgabe Steuerungspunkt (identifiziert mit [SV \_ outputcontrolpointid](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) für jeden Patch aufgerufen (identifiziert durch SV \_ primitiveid).</span><span class="sxs-lookup"><span data-stu-id="e1e13-139">A hull shader is invoked once per output control point (identified with [SV\_OutputControlPointID](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) for each patch (identified with SV\_PrimitiveID).</span></span> <span data-ttu-id="e1e13-140">Der Zweck dieses bestimmten Shaders ist das Berechnen der Ausgabe *i*, die als Bezier-Steuerungspunkt definiert wurde (in diesem Beispiel sind 16 Ausgabe Kontrollpunkte definiert, die von outputcontrolpoints definiert werden).</span><span class="sxs-lookup"><span data-stu-id="e1e13-140">The purpose of this particular shader is to calculate output *i*, which was defined to be a BEZIER control point (this example has 16 output control points defined by outputcontrolpoints).</span></span>

<span data-ttu-id="e1e13-141">Ein Hull-Shader führt eine Routine einmal pro Patch (die Patch-konstantenfunktion) aus, um patchkonstante Daten (Mosaik Faktoren als Minimalwert) zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="e1e13-141">A hull shader runs a routine once per patch (the patch constant function) to compute patch-constant data (tessellation factors as a minimum).</span></span> <span data-ttu-id="e1e13-142">Separat führt ein Hull-Shader für jeden Patch eine Patch-konstantenfunktion (mit dem Namen "subdesbezierconstantshs") aus, um patchkonstante Daten zu berechnen, z. b. Mosaik Faktoren für die Mosaik Phase.</span><span class="sxs-lookup"><span data-stu-id="e1e13-142">Separately, a hull shader runs a patch constant function (called SubDToBezierConstantsHS) on each patch to compute patch-constant data such as tessellation factors for the tessellator stage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1e13-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1e13-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1e13-144">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="e1e13-144">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="e1e13-145">Mosaik Übersicht</span><span class="sxs-lookup"><span data-stu-id="e1e13-145">Tessellation Overview</span></span>](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 