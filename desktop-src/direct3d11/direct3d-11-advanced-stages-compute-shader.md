---
title: Übersicht über Compute-Shader
description: Ein Compute-Shader ist eine programmierbare Shader-Phase, die Microsoft Direct3D 11 über die Grafik Programmierung hinaus erweitert. Die COMPUTE-Shader-Technologie wird auch als DirectCompute-Technologie bezeichnet.
ms.assetid: 02c1f98e-fdd6-49b0-b8b2-efbd472ab599
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c890e63b468a993e0d08f678d2276d6ce2adad
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734753"
---
# <a name="compute-shader-overview"></a>Übersicht über Compute-Shader

Ein Compute-Shader ist eine programmierbare Shader-Phase, die Microsoft Direct3D 11 über die Grafik Programmierung hinaus erweitert. Die COMPUTE-Shader-Technologie wird auch als DirectCompute-Technologie bezeichnet.

Wie andere programmierbare Shader (z. b. Scheitelpunkt-und Geometry-Shader) wird ein Compute-Shader entworfen und mit [HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl) implementiert, aber das ist nur der Ort, an dem die Ähnlichkeit endet. Ein Compute-Shader bietet eine hohe Geschwindigkeit für das allgemeine Computing und nutzt die große Anzahl paralleler Prozessoren auf der GPU (Graphics Processing Unit). Der COMPUTE-Shader bietet Funktionen für die Speicherfreigabe und die Thread Synchronisierung, um effektivere parallele Programmiermethoden zu ermöglichen. Zum Ausführen von Befehlen in einem Compute-Shader wird die [**Verknüpfung id3d11devicecontext aus::D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch) -oder [**Verknüpfung id3d11devicecontext aus::D ispatchindirekte**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect) -Methode aufgerufen. Ein Compute-Shader kann in vielen Threads parallel ausgeführt werden.

## <a name="using-compute-shader-on-direct3d-10x-hardware"></a>Verwenden von Compute-Shader auf Direct3D 10. x-Hardware

Ein Compute-Shader auf Microsoft Direct3D 10 wird auch als DirectCompute 4. x bezeichnet.

Wenn Sie die Direct3D 11-API und aktualisierte Treiber verwenden, kann die Hardware von [Featureebene](overviews-direct3d-11-devices-downlevel-intro.md) 10 und 10,1 Direct3D optional eine eingeschränkte Form von DirectCompute unterstützen, die die \_ profile CS 4 \_ 0 und CS \_ 4 1 verwendet \_ . [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models) Beachten Sie bei der Verwendung von DirectCompute auf dieser Hardware die folgenden Einschränkungen:

-   Die maximale Anzahl von Threads ist auf D3D11 \_ CS \_ 4 \_ X \_ Thread \_ Gruppe \_ Max \_ Threads \_ pro \_ Gruppe (768) pro Gruppe beschränkt.
-   Die X-und Y-Dimension von **numThreads** ist auf D3D11 \_ CS \_ 4 \_ x \_ Thread \_ Gruppe \_ Max \_ x (768) und D3D11 \_ CS \_ 4 \_ x \_ Thread \_ Gruppe \_ Max \_ Y (768) beschränkt.
-   Die Z-Dimension von **numThreads** ist auf 1 begrenzt.
-   Die z-Dimension von Dispatch ist auf D3D11 \_ CS \_ 4 \_ X \_ Dispatch \_ Max \_ Thread \_ Groups \_ in \_ Z- \_ Dimension (1) beschränkt.
-   Nur eine ungeordnete Zugriffs Ansicht kann an den Shader gebunden werden (D3D11 \_ CS \_ 4 \_ X \_ UAV \_ Register \_ count ist 1).
-   Nur [rwstructuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s und [rwbyteaddressbuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s sind als ungeordnete Zugriffs Sichten verfügbar.
-   Ein Thread kann nur auf seine eigene Region im groupshared-Speicher zum Schreiben zugreifen, er kann jedoch von einem beliebigen Speicherort aus lesen.
-   [SV \_ GroupIndex](/previous-versions/windows/desktop/legacy/ff471569(v=vs.85)) oder [SV \_ dispatchthreadid](/windows/desktop/direct3dhlsl/sv-dispatchthreadid) muss beim Zugriff auf den **groupshared** -Speicher zum Schreiben verwendet werden.
-   **Groupshared** -Speicher ist auf 16 KB pro Gruppe beschränkt.
-   Ein einzelner Thread ist auf einen 256-Byte-Bereich des **groupshared** -Speichers zum Schreiben beschränkt.
-   Es sind keine atomarischen Anweisungen verfügbar.
-   Es sind keine Werte mit doppelter Genauigkeit verfügbar.

## <a name="using-compute-shader-on-direct3d-11x-hardware"></a>Verwenden von Compute-Shader auf Direct3D 11. x-Hardware

Ein Compute-Shader auf Direct3D 11 wird auch als DirectCompute 5,0 bezeichnet.

Beachten Sie beim Verwenden von DirectCompute mit CS \_ 5 \_ 0- [Profilen](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-models)die folgenden Punkte:

-   Die maximale Anzahl von Threads ist auf die maximale Anzahl von Threads der D3D11 \_ CS- \_ Thread \_ Gruppe \_ \_ \_ pro \_ Gruppe (1024) pro Gruppe beschränkt.
-   Die X-und Y-Dimension von **numThreads** ist auf die D3D11 \_ CS \_ \_ -Thread Gruppe \_ Max \_ X (1024) und die D3D11 \_ CS- \_ Thread \_ Gruppe \_ Max \_ Y (1024) beschränkt.
-   Die Z-Dimension von **numThreads** ist auf die D3D11 \_ CS- \_ Thread \_ Gruppe \_ Max \_ Z (64) beschränkt.
-   Die maximale Dimension der Verteilung ist auf D3D11 \_ CS \_ Dispatch \_ Max \_ Thread \_ Groups \_ per \_ Dimension (65535) beschränkt.
-   Die maximale Anzahl nicht geordneter Zugriffs Sichten, die an einen Shader gebunden werden können, ist D3D11 \_ PS \_ CS \_ UAV \_ Register \_ count (8).
-   Unter [stützt rwstructuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)s [, rwbyteaddressbuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)s und typisierte nicht geordnete Zugriffs Sichten ([RWTexture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d), [RWTexture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d), [RWTexture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d)usw.).
-   Es sind atomarische Anweisungen verfügbar.
-   Unterstützung für doppelte Genauigkeit ist möglicherweise verfügbar. Informationen dazu, wie Sie feststellen können, ob doppelte Genauigkeit verfügbar ist, finden Sie unter [**D3D11 \_ Feature \_ Doubles**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Neue Ressourcentypen](direct3d-11-advanced-stages-cs-resources.md)<br/>      | In Direct3D 11 wurden mehrere neue Ressourcentypen hinzugefügt.<br/>                                                                                                                                                                                                 |
| [Zugreifen auf Ressourcen](direct3d-11-advanced-stages-cs-access.md)<br/>        | Es gibt mehrere Möglichkeiten, auf [Ressourcen](overviews-direct3d-11-resources-types.md)zuzugreifen.<br/>                                                                                                                                                                   |
| [Atomarische Funktionen](direct3d-11-advanced-stages-cs-atomic-functions.md)<br/> | Um auf einen neuen Ressourcentyp oder freigegebenen Speicher zuzugreifen, verwenden Sie eine intrinsische Interlocked-Funktion. Interlocked-Funktionen werden gewährleistet, dass Sie atomisch ausgeführt werden. Das heißt, dass Sie garantiert in der programmierten Reihenfolge auftreten. In diesem Abschnitt werden die atomaren Funktionen aufgelistet.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafik Pipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Vorgehensweise: Erstellen eines Compute-Shaders](direct3d-11-advanced-stages-compute-create.md)
</dt> </dl>

 

