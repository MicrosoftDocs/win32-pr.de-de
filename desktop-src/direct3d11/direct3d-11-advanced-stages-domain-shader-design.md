---
title: Entwerfen eines Domänen-Shaders
description: In diesem Thema wird gezeigt, wie ein Domänen-Shader entworfen wird.
ms.assetid: 329d4eb9-8886-401d-8fb4-39e06886998f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a01d6b006c5ffe3afa355abe5e662cb96aa1391
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101938"
---
# <a name="how-to-design-a-domain-shader"></a>Vorgehensweise: Entwerfen eines Domänen-Shader

Ein Domänen-Shader ist der dritte von drei Phasen, die zusammenarbeiten, um Mosaik Vorgänge [zu implementieren.](direct3d-11-advanced-stages-tessellation.md) Der Domänen-Shader generiert die Oberflächengeometrie aus den transformierten Steuerungs Punkten von einem Hull-Shader und den UV-Koordinaten. In diesem Thema wird gezeigt, wie ein Domänen-Shader entworfen wird.

Ein Domänen-Shader wird einmal für jeden Punkt aufgerufen, der vom Mosaik der Fixed-Funktion generiert wird. Die Eingaben sind die UV \[ - \] Koordinaten des Punkts auf dem Patch sowie alle Ausgabedaten aus dem Hull-Shader einschließlich der Steuerungs Punkte und patchkonstanten. Die Ausgabe ist ein Scheitelpunkt, der in der gewünschten Weise definiert ist. Wenn die Ausgabe an den Pixelshader gesendet wird, muss die Ausgabe eine Position (mit einer SV- \_ Positions Semantik) enthalten.

**So entwerfen Sie einen Domänen-Shader**

1.  Definieren des Domänen Attributs.

    ```
    [domain("quad")]
    ```

    

    Die Domäne ist für einen Quad-Patch definiert.

2.  Deklarieren Sie den Speicherort auf der Hülle mit dem [Domänen Speicherort](/windows/desktop/direct3dhlsl/sv-domainlocation) System Wert.

    -   Verwenden Sie für einen Quad-Patch eine float2.
    -   Verwenden Sie für einen Tri-Patch eine float3 (für baryzentrierte Koordinaten).
    -   Verwenden Sie für eine Isoline eine float2.

    Daher sieht der Domänen Speicherort für einen Quad-Patch wie folgt aus:

    ```
    float2 UV : SV_DomainLocation
    ```

    

3.  Definieren Sie die anderen Eingaben.

    Die anderen Eingaben stammen aus dem Hull-Shader und sind Benutzer definiert. Dies schließt die Eingabe Steuerungs Punkte für Patch ein, von denen zwischen 1 und 32 Punkte bestehen können, und Daten der Eingabe patchkonstante.

    Die Kontrollpunkte sind Benutzer definiert, normalerweise mit einer Struktur wie dieser (in Gewusst [wie: Entwerfen eines Hull-Shaders](direct3d-11-advanced-stages-hull-shader-design.md)definiert):

    ```
    const OutputPatch<BEZIER_CONTROL_POINT, 16> bezpatch
    ```

    

    Die Patch-konstantendaten sind ebenfalls Benutzer definiert und könnten wie folgt aussehen (in Gewusst [wie: Entwerfen eines Hull-Shaders](direct3d-11-advanced-stages-hull-shader-design.md)definiert):

    ```
    HS_CONSTANT_DATA_OUTPUT input
    ```

    

4.  Fügen Sie benutzerdefinierten Code hinzu, um die Ausgaben zu berechnen. Dadurch wird der Hauptteil des Domänen-Shaders angezeigt.

    Diese Struktur enthält benutzerdefinierte Domänen-Shader-Ausgaben.

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

    

    Die Funktion nimmt jede Eingabe-UV (aus dem Mosaik Prozess) an und wertet den Bezier-Patch an dieser Position aus.

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

    

    Die-Funktion wird einmal für jeden Punkt aufgerufen, der vom Mosaik der Fixed-Funktion generiert wird. Da in diesem Beispiel ein Quad-Patch verwendet wird, ist der Speicherort der Eingabe Domäne ([SV \_ domainlocation](/windows/desktop/direct3dhlsl/sv-domainlocation)) ein float2 (UV), ein Tri-Patch hätte einen float3-Eingabe Speicherort (UVW-baryzentrische Koordinaten), und eine Isoline würde einen float2-Eingabe Domänen Speicherort aufweisen.

    Die anderen Eingaben für die Funktion stammen direkt aus dem Hull-Shader. In diesem Beispiel handelt es sich um 16 Kontrollpunkte, von denen jeder ein **Bezier- \_ Steuerungs \_ Punkt** ist, sowie um patchkonstantendaten (**HS- \_ Konstante \_ Daten \_ Ausgabe**). Bei der Ausgabe handelt es sich um einen Scheitelpunkt, der alle in diesem Beispiel für die Daten gewünschten **DS- \_ Ausgaben**

Nachdem Sie einen Domänen-Shader entworfen haben, finden Sie unter Gewusst [wie: Erstellen eines Domänen-Shaders](direct3d-11-advanced-stages-domain-shader-create.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Mosaik Übersicht](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 