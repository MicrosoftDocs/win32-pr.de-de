---
title: Übersicht über Compute-Shader
description: Ein Compute-Shader ist eine programmierbare Shaderstufe, die Microsoft Direct3D 11 über die Grafikprogrammierung hinaus erweitert. Die Compute-Shadertechnologie wird auch als DirectCompute-Technologie bezeichnet.
ms.assetid: 02c1f98e-fdd6-49b0-b8b2-efbd472ab599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6167915a670b6dfb4fffae957ee0121e8e52f639463b0d1132be9dac3552fe9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119566340"
---
# <a name="compute-shader-overview"></a>Übersicht über Compute-Shader

Ein Compute-Shader ist eine programmierbare Shaderstufe, die Microsoft Direct3D 11 über die Grafikprogrammierung hinaus erweitert. Die Compute-Shadertechnologie wird auch als DirectCompute-Technologie bezeichnet.

Wie bei anderen programmierbaren Shadern (z. B. Vertex- und Geometrie-Shader) wird ein Compute-Shader mit [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) entworfen und implementiert, aber genau an diesem Ort endet die Ähnlichkeit. Ein Compute-Shader bietet high-speed General Purpose Computing und nutzt die große Anzahl paralleler Prozessoren auf der Grafikprozessor (GRAPHICS Processing Unit, GPU). Der Compute-Shader bietet Funktionen zur Speicherfreigabe und Threadsynchronisierung, um effektivere parallele Programmiermethoden zu ermöglichen. Sie rufen die [**ID3D11DeviceContext::D ispatch-**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) oder [**ID3D11DeviceContext::D ispatchIndirect-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect) auf, um Befehle in einem Compute-Shader auszuführen. Ein Compute-Shader kann auf vielen Threads parallel ausgeführt werden.

## <a name="using-compute-shader-on-direct3d-10x-hardware"></a>Verwenden von Compute-Shader auf Direct3D 10.x-Hardware

Ein Compute-Shader auf Microsoft Direct3D 10 wird auch als DirectCompute 4.x bezeichnet.

Wenn Sie die Direct3D 11-API und aktualisierte Treiber [verwenden,](overviews-direct3d-11-devices-downlevel-intro.md) kann direct3D-Hardware auf Featureebene 10 und 10.1 optional eine eingeschränkte Form von DirectCompute unterstützen, die die Profile cs \_ 4 0 und cs \_ \_ 4 \_ 1 verwendet. [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models) Wenn Sie DirectCompute auf dieser Hardware verwenden, beachten Sie die folgenden Einschränkungen:

-   Die maximale Anzahl von Threads ist auf D3D11 \_ CS \_ 4 \_ X THREAD GROUP MAX THREADS PER \_ GROUP \_ \_ \_ \_ \_ (768) pro Gruppe beschränkt.
-   Die X- und Y-Dimension von **numthreads** ist auf D3D11 \_ CS \_ 4 \_ X THREAD GROUP MAX X \_ \_ \_ \_ (768) und D3D11 \_ CS \_ 4 X THREAD GROUP \_ MAX \_ \_ \_ \_ Y (768) beschränkt.
-   Die Z-Dimension **von numthreads** ist auf 1 beschränkt.
-   Die Z-Dimension von dispatch ist auf D3D11 \_ CS \_ 4 \_ X DISPATCH MAX THREAD GROUPS IN Z \_ DIMENSION \_ \_ \_ \_ \_ \_ (1) beschränkt.
-   Nur eine Ansicht mit ungeordneten Zugriffen kann an den Shader gebunden werden (D3D11 \_ CS \_ 4 \_ X \_ UAV REGISTER COUNT ist \_ \_ 1).
-   Nur [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s und [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s sind als Unordered Access-Ansichten verfügbar.
-   Ein Thread kann zum Schreiben nur auf seine eigene Region im gruppenfreigaben Speicher zugreifen, obwohl er von einem beliebigen Speicherort aus lesen kann.
-   [SV \_ GroupIndex](/previous-versions/windows/desktop/legacy/ff471569(v=vs.85)) oder [SV \_ GroupThreadID](/windows/desktop/direct3dhlsl/sv-groupthreadid) muss beim Zugriff auf den gruppenfreigaben **Speicher zum** Schreiben verwendet werden.
-   **Der gruppenfreigaben** Speicher ist auf 16 KB pro Gruppe beschränkt.
-   Ein einzelner Thread ist auf einen 256-Byte-Bereich von **gruppenfreigabem** Speicher zum Schreiben beschränkt.
-   Es sind keine atomaren Anweisungen verfügbar.
-   Es sind keine Werte mit doppelter Genauigkeit verfügbar.

## <a name="using-compute-shader-on-direct3d-11x-hardware"></a>Verwenden von Compute-Shader auf Direct3D 11.x-Hardware

Ein Compute-Shader auf Direct3D 11 wird auch als DirectCompute 5.0 bezeichnet.

Wenn Sie DirectCompute mit cs \_ 5 \_ 0-Profilen [verwenden,](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models)beachten Sie Folgendes:

-   Die maximale Anzahl von Threads ist auf D3D11 \_ CS THREAD GROUP MAX THREADS PER GROUP \_ \_ \_ \_ \_ \_ (1024) pro Gruppe beschränkt.
-   Die X- und Y-Dimension von **numthreads** ist auf D3D11 \_ CS THREAD GROUP MAX X \_ \_ \_ \_ (1024) und D3D11 \_ CS THREAD GROUP MAX \_ \_ \_ \_ Y (1024) beschränkt.
-   Die Z-Dimension **von numthreads** ist auf D3D11 \_ CS THREAD GROUP MAX Z \_ \_ \_ \_ (64) beschränkt.
-   Die maximale Dimension des Dispatchs ist auf D3D11 \_ CS DISPATCH MAX THREAD GROUPS PER DIMENSION \_ \_ \_ \_ \_ \_ (65535) beschränkt.
-   Die maximale Anzahl von Ansichten mit ungeordneten Zugriffen, die an einen Shader gebunden werden können, ist D3D11 \_ PS \_ CS \_ UAV REGISTER COUNT \_ \_ (8).
-   Unterstützt [RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s, [RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s und typierte Unordered Access-Ansichten[(RWTexture1D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d) [RWTexture2D,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d) [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)und so weiter).
-   Atomar-Anweisungen sind verfügbar.
-   Unterstützung mit doppelter Genauigkeit ist möglicherweise verfügbar. Informationen zum Bestimmen, ob doppelte Genauigkeit verfügbar ist, finden Sie unter [**D3D11 \_ FEATURE \_ DOUBLES**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                              | Beschreibung                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Neue Ressourcentypen](direct3d-11-advanced-stages-cs-resources.md)<br/>      | In Direct3D 11 wurden mehrere neue Ressourcentypen hinzugefügt.<br/>                                                                                                                                                                                                 |
| [Zugreifen auf Ressourcen](direct3d-11-advanced-stages-cs-access.md)<br/>        | Es gibt mehrere Möglichkeiten, auf Ressourcen [zu zugreifen.](overviews-direct3d-11-resources-types.md)<br/>                                                                                                                                                                   |
| [Atomic-Funktionen](direct3d-11-advanced-stages-cs-atomic-functions.md)<br/> | Verwenden Sie eine interlocked intrinsic-Funktion, um auf einen neuen Ressourcentyp oder freigegebenen Arbeitsspeicher zu zugreifen. Interlocked-Funktionen funktionieren garantiert atomar. Das heißt, dass sie garantiert in der programmierten Reihenfolge auftreten. In diesem Abschnitt werden die atomic-Funktionen aufgeführt.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafikpipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[How To: Create a Compute Shader](direct3d-11-advanced-stages-compute-create.md)
</dt> </dl>

 

