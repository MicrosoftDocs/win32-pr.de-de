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
# <a name="how-to-design-a-hull-shader"></a>Gewusst wie: Entwerfen eines Hull-Shaders

Ein Hull-Shader ist die erste von drei Phasen, die zusammenarbeiten, um Mosaik [zu implementieren (](direct3d-11-advanced-stages-tessellation.md) die beiden anderen Phasen sind der Mosaik-und Domänen-Shader). In diesem Thema wird gezeigt, wie ein Hull-Shader entworfen wird.

Ein Hull-Shader erfordert zwei Funktionen: den Haupt-Hull-Shader und eine Patch-konstantenfunktion. Der Hull-Shader implementiert Berechnungen für jeden Steuerungspunkt. der Hull-Shader ruft auch die Patch-Konstante Funktion auf, die Berechnungen für die einzelnen Patches implementiert.

Nachdem Sie einen Hull-Shader entworfen haben, finden Sie weitere Informationen unter Gewusst [wie: Erstellen](direct3d-11-advanced-stages-hull-shader-create.md) eines Hull-Shaders, um zu erfahren, wie ein Hull-Shader erstellt wird.

**So entwerfen Sie einen Hull-Shader**

1.  Definieren des Hull-Shader-Eingabe Steuer Elements und von Ausgabe Steuerungs Punkten.

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

    

2.  Definiert die Daten der Ausgabe Patch-Konstante.

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

    

    Bei einer vierfach Domäne definiert der [SV- \_ tmosaik-Faktor](/windows/desktop/direct3dhlsl/sv-tessfactor) vier Edge-Mosaik Faktoren (um die Ränder zu Mosaik), da der Mosaik-Mosaik Faktor wissen muss, wie viel im Mosaik Prozess festgelegt werden muss. Die erforderlichen Ausgaben unterscheiden sich für die Dreiecks-und isolin-Domänen.

    Der Mosaik-Mosaik Ausdruck untersucht keine anderen Hull-shaderausgaben, wie z. b. andere patchkonstantendaten oder einen der Steuerungs Punkte. Der Domänen-Shader, der für jeden Punkt aufgerufen wird, der vom tmosaik-Debugger generiert wird--wird als Eingabe alle Ausgabe Steuerungs Punkte des Hull-Shader und alle Ausgabe Patch-konstantendaten angezeigt. der Shader wertet den Patch an seinem Speicherort aus.

3.  Definieren Sie eine Patch-Konstante Funktion. Eine Patch-konstantenfunktion wird einmal für jeden Patch ausgeführt, um alle Daten zu berechnen, die für den gesamten Patch konstant sind (im Gegensatz zu den Daten im Rumpf-Shader).

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

    

    Zu den Eigenschaften der Patch-konstantenfunktion gehören:

    -   Eine Eingabe gibt eine Variable an, die eine Patch-ID enthält, und wird durch den System Wert **SV \_ primitiveid** identifiziert (siehe [Semantik](../direct3dhlsl/dx-graphics-hlsl-semantics.md) in Shader Model 4).
    -   Ein Eingabeparameter ist die Eingabe Steuerungs Punkte, die in diesem Beispiel in der **vs- \_ Steuerungs \_ Punkt \_ Ausgabe** deklariert werden. Eine patchfunktion kann alle Eingabe Steuerungs Punkte für jeden Patch sehen. in diesem Beispiel gibt es 32-Kontrollpunkte pro Patch.
    -   Die-Funktion muss mindestens pro Patch-Mosaik Faktoren für die Mosaik Stufe berechnen, die mit [SV \_ Tess Factor](/windows/desktop/direct3dhlsl/sv-tessfactor)identifiziert werden. Für eine Quad-Domäne sind vier Mosaik Faktoren für die Ränder und zwei zusätzliche Faktoren (identifiziert durch [SV \_ insidetess Factor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)) erforderlich, um das Mosaik Ende des Patches zu gestalten. Der Mosaik-Mosaik Ausdruck untersucht keine anderen Hull-shaderausgaben (z. b. die Patch-konstantendaten oder eines der Steuerpunkte).
    -   Die Ausgaben werden normalerweise durch eine-Struktur definiert und in diesem Beispiel durch die **\_ \_ Daten \_ Ausgabe der HS-Konstante** identifiziert. die Struktur hängt vom Domänentyp ab und unterscheidet sich von den Domänen Typen.

    Ein Domänen-Shader auf der anderen Seite wird für jeden Punkt aufgerufen, den der tmosaik-Debugger generiert hat, und er muss die Ausgabe Steuerungs Punkte und die Ausgabe-Patch-konstantendaten (beides aus dem Hull-Shader) anzeigen, um einen Patch an seinem Speicherort auszuwerten.

4.  Definieren Sie einen Hull-Shader. Ein Hull-Shader identifiziert die Eigenschaften eines Patches, einschließlich einer Patch-konstantenfunktion. Ein Hull-Shader wird für jeden Ausgabe Steuerungspunkt einmal aufgerufen.

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

    

    Ein Hull-Shader verwendet die folgenden Attribute:

    -   Ein [Domänen](/windows/desktop/direct3dhlsl/sm5-attributes-domain) Attribut.
    -   Ein [Partitionierungs](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) Attribut.
    -   Ein [outputtopology](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology) -Attribut.
    -   Ein [outputcontrolpoints](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints) -Attribut.
    -   Ein [patchconstantfunc](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) -Attribut. Ein Hull-Shader berechnet Ausgabe Steuerungs Punkte, es gibt in diesem Beispiel 16 Ausgabe Bezier-Steuerungs Punkte.

Alle Eingabe Steuerungs Punkte (die durch die **vs- \_ Steuerungs \_ Punkt \_ Ausgabe** identifiziert werden) sind für jeden Hull-Shader-Aufruf sichtbar. In diesem Beispiel gibt es 32-Eingabe Steuerungs Punkte.

Ein Hull-Shader wird einmal pro Ausgabe Steuerungspunkt (identifiziert mit [SV \_ outputcontrolpointid](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)) für jeden Patch aufgerufen (identifiziert durch SV \_ primitiveid). Der Zweck dieses bestimmten Shaders ist das Berechnen der Ausgabe *i*, die als Bezier-Steuerungspunkt definiert wurde (in diesem Beispiel sind 16 Ausgabe Kontrollpunkte definiert, die von outputcontrolpoints definiert werden).

Ein Hull-Shader führt eine Routine einmal pro Patch (die Patch-konstantenfunktion) aus, um patchkonstante Daten (Mosaik Faktoren als Minimalwert) zu berechnen. Separat führt ein Hull-Shader für jeden Patch eine Patch-konstantenfunktion (mit dem Namen "subdesbezierconstantshs") aus, um patchkonstante Daten zu berechnen, z. b. Mosaik Faktoren für die Mosaik Phase.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Mosaik Übersicht](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 