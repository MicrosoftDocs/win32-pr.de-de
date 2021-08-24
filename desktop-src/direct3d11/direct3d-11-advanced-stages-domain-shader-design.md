---
title: Entwerfen eines Domänen-Shaders
description: In diesem Thema wird gezeigt, wie Sie einen Domänen-Shader entwerfen.
ms.assetid: 329d4eb9-8886-401d-8fb4-39e06886998f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46733bc9147f67cf33a127d8254f16c5813d8ebc2f0cb96c2071ae15589e34bd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566180"
---
# <a name="how-to-design-a-domain-shader"></a>Vorgehensweise: Entwerfen eines Domänen-Shaders

Ein Domänen-Shader ist die dritte von drei Phasen, die zusammenarbeiten, um Mosaik zu [implementieren.](direct3d-11-advanced-stages-tessellation.md) Der Domänen-Shader generiert die Oberflächengeometrie aus den transformierten Kontrollpunkten aus einem Hüllen-Shader und den UV-Koordinaten. In diesem Thema wird gezeigt, wie Sie einen Domänen-Shader entwerfen.

Ein Domänen-Shader wird einmal für jeden Punkt aufgerufen, der vom festen Funktionstessellator generiert wird. Die Eingaben sind die UV \[ \] W-Koordinaten des Punkts auf dem Patch sowie alle Ausgabedaten des Hüllen-Shaders, einschließlich Kontrollpunkten und Patchkonstanten. Die Ausgabe ist ein Scheitelpunkt, der auf beliebige Weise definiert ist. Wenn die Ausgabe an den Pixelshader gesendet wird, muss die Ausgabe eine Position enthalten (angegeben mit einer \_ SV-Positionssemantik).

**So entwerfen Sie einen Domänen-Shader**

1.  Definieren Sie das Domänenattribut.

    ```
    [domain("quad")]
    ```

    

    Die Domäne ist für einen Quad-Patch definiert.

2.  Deklarieren Sie den Speicherort auf der Hülle mit dem Systemwert des [Domänenstandorts.](/windows/desktop/direct3dhlsl/sv-domainlocation)

    -   Verwenden Sie für einen Quad-Patch float2.
    -   Verwenden Sie für einen Tri-Patch float3 (für baryzentrische Koordinaten).
    -   Verwenden Sie für eine Isolinie float2.

    Daher sieht der Domänenspeicherort für einen Quad-Patch wie folgt aus:

    ```
    float2 UV : SV_DomainLocation
    ```

    

3.  Definieren Sie die anderen Eingaben.

    Die anderen Eingaben stammen vom Hüllen-Shader und sind benutzerdefiniert. Dazu gehören die Eingabesteuerpunkte für den Patch, von denen zwischen 1 und 32 Punkte vorhanden sein können, und Eingabepatchkonstantendaten.

    Die Kontrollpunkte sind benutzerdefiniert, in der Regel mit einer Struktur wie dieser (definiert in [Vorgehensweise: Entwerfen eines Hüllen-Shaders):](direct3d-11-advanced-stages-hull-shader-design.md)

    ```
    const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch
    ```

    

    Die Patchkonstantendaten sind ebenfalls benutzerdefiniert und können wie folgt aussehen (definiert in [Vorgehensweise: Entwerfen eines Hüllen-Shaders):](direct3d-11-advanced-stages-hull-shader-design.md)

    ```
    HS_CONSTANT_DATA_OUTPUT input
    ```

    

4.  Fügen Sie benutzerdefinierten Code hinzu, um die Ausgaben zu berechnen. dies bildet den Text des Domänen-Shaders.

    Diese Struktur enthält benutzerdefinierte Domänen-Shaderausgaben.

    ```
    struct DS_OUTPUT
    {
        float3 vNormal    : NORMAL;
        float2 vUV        : TEXCOORD;
        float3 vTangent   : TANGENT;
        float3 vBiTangent : BITANGENT;
        
        float4 vPosition  : SV_POSITION;
    };
    ```

    

    Die Funktion nimmt jedes Eingabe-UV (aus dem Mosaik) und wertet den Bézierpatch an dieser Position aus.

    ```
    [domain("quad")]
    DS_OUTPUT BezierEvalDS( HS_CONSTANT_DATA_OUTPUT input, 
                            float2 UV : SV_DomainLocation,
                            const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch )
    {
        DS_OUTPUT Output;

        // Insert code to compute the output here.

        return Output;    
    }
    ```

    

    Die Funktion wird einmal für jeden Punkt aufgerufen, der vom festen Funktionstessellator generiert wird. Da in diesem Beispiel ein Quad-Patch verwendet wird, ist der Speicherort der Eingabedomäne ([SV \_ DomainLocation](/windows/desktop/direct3dhlsl/sv-domainlocation)) float2 (UV). Ein Tri-Patch würde eine float3-Eingabeposition (UVW-barycentric-Koordinaten) und eine Isolinie eine Float2-Eingabedomänenposition aufweisen.

    Die anderen Eingaben für die Funktion stammen direkt vom Hüllen-Shader. In diesem Beispiel sind es 16 Steuerpunkte, die jeweils ein **BEZIER \_ CONTROL \_ POINT** sind, sowie Patchkonstantendaten (**HS \_ CONSTANT DATA \_ \_ OUTPUT**). Die Ausgabe ist ein Scheitelpunkt, der alle gewünschten Daten enthält– **DS \_ OUTPUT** in diesem Beispiel.

Nachdem Sie einen Domänen-Shader entworfen haben, finden Sie weitere Informationen unter [Vorgehensweise: Erstellen eines Domänen-Shaders.](direct3d-11-advanced-stages-domain-shader-create.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Übersicht über Mosaik](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 