---
title: Entwerfen eines Hüllen-Shaders
description: In diesem Thema wird gezeigt, wie Sie einen Hüllen-Shader entwerfen.
ms.assetid: c11c5652-dd7d-433d-bfa2-9853618ba334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79021d6a5c03b057defdeae0d506898831ab740d11d2e105242ff53b1b39e9bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046638"
---
# <a name="how-to-design-a-hull-shader"></a>Vorgehensweise: Entwerfen eines Hüllen-Shaders

Ein Hüllen-Shader ist die erste von drei Phasen, die zusammenarbeiten, um mosaik zu [implementieren](direct3d-11-advanced-stages-tessellation.md) (die anderen beiden Phasen sind der Mosaikator und ein Domänen-Shader). In diesem Thema wird gezeigt, wie Sie einen Hüllen-Shader entwerfen.

Ein Hüllen-Shader erfordert zwei Funktionen: den Haupthüllen-Shader und eine Patchkonstantenfunktion. Der Hüllen-Shader implementiert Berechnungen für jeden Kontrollpunkt. Der Hüllen-Shader ruft auch die Patchkonstantenfunktion auf, die Berechnungen für jeden Patch implementiert.

Nachdem Sie einen Hüllen-Shader entworfen haben, lesen [Sie Vorgehensweise: Erstellen eines Hüllen-Shaders,](direct3d-11-advanced-stages-hull-shader-create.md) um zu erfahren, wie Sie einen Hüllen-Shader erstellen.

**So entwerfen Sie einen Hüllen-Shader**

1.  Definieren Sie das Eingabesteuerelement und die Ausgabekontrollpunkte des Shaders.

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

    

2.  Definieren Sie ausgabepatchkonstante Daten.

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

    

    Für eine Quad-Domäne definiert [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor) 4 Edge-Mosaikfaktoren (um die Kanten zu mosaikieren), da der Fixfunktionstessellator wissen muss, wie viel mosaikiert werden soll. Die erforderlichen Ausgaben unterscheiden sich für die Dreiecks- und Isolinedomänen.

    Der fixierte Funktionstessellator untersucht keine anderen Ausgaben des Hüllen-Shaders, z. B. andere Patchkonstantendaten oder einen der Kontrollpunkte. Der Domänen-Shader , der für jeden Punkt aufgerufen wird, den der feste Funktionstessellator generiert, wird als Eingabe für alle Ausgabekontrollpunkte des Hüllen-Shaders und alle Ausgabepatchkonstantendaten angezeigt. der Shader wertet den Patch an seiner Position aus.

3.  Definieren Sie eine Patchkonstantenfunktion. Eine Patchkonstantenfunktion wird einmal für jeden Patch ausgeführt, um alle Daten zu berechnen, die für den gesamten Patch konstant sind (im Gegensatz zu Den Steuerungspunktdaten, die im Hüllen-Shader berechnet werden).

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

    

    Zu den Eigenschaften der Patchkonstantenfunktion gehören:

    -   Eine Eingabe gibt eine Variable an, die eine Patch-ID enthält, und wird durch den **SV \_ PrimitiveID-Systemwert** identifiziert (siehe [Semantik](../direct3dhlsl/dx-graphics-hlsl-semantics.md) im Shadermodell 4).
    -   Ein Eingabeparameter sind die Eingabesteuerpunkte, die in diesem Beispiel in **VS \_ CONTROL POINT \_ \_ OUTPUT** deklariert werden. Eine Patchfunktion kann alle Eingabesteuerpunkte für jeden Patch anzeigen. In diesem Beispiel gibt es 32 Steuerungspunkte pro Patch.
    -   Die Funktion muss mindestens die Mosaikfaktoren pro Patch für die Mosaikphase berechnen, die mit [SV \_ TessFactor](/windows/desktop/direct3dhlsl/sv-tessfactor)identifiziert werden. Eine Quad-Domäne erfordert vier Mosaikfaktoren für die Kanten und zwei zusätzliche Faktoren (identifiziert durch [SV \_ InsideTessFactor](/windows/desktop/direct3dhlsl/sv-insidetessfactor)), um das Mosaik innerhalb des Patches zu ermöglichen. Der feste Funktionstessellator untersucht keine anderen Ausgaben des Hüllen-Shaders (z. B. die Patchkonstantendaten oder einen der Kontrollpunkte).
    -   Die Ausgaben werden in der Regel durch eine -Struktur definiert und in diesem Beispiel durch **HS \_ CONSTANT DATA \_ \_ OUTPUT** identifiziert. Die Struktur hängt vom Domänentyp ab und unterscheidet sich bei Dreiecks- oder Isolinedomänen.

    Ein Domänen-Shader wird dagegen für jeden Punkt aufgerufen, den der fixierte Funktionstessellator generiert und die Ausgabekontrollpunkte und die Konstantendaten des Ausgabepatches (beide aus dem Hüllen-Shader) anzeigen muss, um einen Patch an seiner Position auszuwerten.

4.  Definieren Sie einen Hüllen-Shader. Ein Hüllen-Shader identifiziert die Eigenschaften eines Patches, einschließlich einer Patchkonstantenfunktion. Ein Hüllen-Shader wird einmal für jeden Ausgabekontrollpunkt aufgerufen.

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

    

    Ein Hüllen-Shader verwendet die folgenden Attribute:

    -   Ein [](/windows/desktop/direct3dhlsl/sm5-attributes-domain) Domänenattribut.
    -   Ein [](/windows/desktop/direct3dhlsl/sm5-attributes-partitioning) Partitionierungsattribut.
    -   Ein [outputtopology-Attribut.](/windows/desktop/direct3dhlsl/sm5-attributes-outputtopology)
    -   Ein [outputcontrolpoints-Attribut.](/windows/desktop/direct3dhlsl/sm5-attributes-outputcontrolpoints)
    -   Ein [patchconstantfunc-Attribut.](/windows/desktop/direct3dhlsl/sm5-attributes-patchconstantfunc) Ein Hüllen-Shader berechnet Ausgabekontrollpunkte. In diesem Beispiel gibt es 16 Ausgabe-Bézier-Kontrollpunkte.

Alle Eingabesteuerpunkte (identifiziert durch **VS \_ CONTROL POINT \_ \_ OUTPUT)** sind für jeden Shaderaufruf sichtbar. In diesem Beispiel gibt es 32 Eingabesteuerpunkte.

Ein Hüllen-Shader wird einmal pro Ausgabekontrollpunkt (identifiziert mit [SV \_ OutputControlPointID)](/windows/desktop/direct3dhlsl/sv-outputcontrolpointid)für jeden Patch (identifiziert mit SV \_ PrimitiveID) aufgerufen. Der Zweck dieses bestimmten Shaders besteht darin, die Ausgabe *i* zu berechnen, die als BEZIER-Steuerungspunkt definiert wurde (in diesem Beispiel sind 16 Ausgabekontrollpunkte durch outputcontrolpoints definiert).

Ein Hüllen-Shader führt einmal pro Patch (die Patchkonstantenfunktion) eine Routine aus, um patchkonstante Daten (Mosaikfaktoren als Minimum) zu berechnen. Separat führt ein Hüllen-Shader eine Patchkonstantenfunktion (subDToBezierConstantsHS) für jeden Patch aus, um Patchkonstantendaten wie Mosaikfaktoren für die Mosaikphase zu berechnen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Übersicht über Mosaik](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 