---
title: Compute-Shader auf downlevelhardware
description: In diesem Thema wird die Verwendung von Compute-Shadern in einer Direct3D 11-App auf Direct3D 10-Hardware erläutert.
ms.assetid: b864269f-c1f7-4253-888d-04d1ed3e6587
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e77214e917d4d74b0e1eebcc3de245d136157976
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104039816"
---
# <a name="compute-shaders-on-downlevel-hardware"></a>Compute-Shader auf downlevelhardware

Direct3D 11 bietet die Möglichkeit, [Compute-Shader](direct3d-11-advanced-stages-compute-shader.md) zu verwenden, die mit den meisten Direct3D 10. x-Hardware betrieben werden, wobei einige Einschränkungen für den Betrieb bestehen. Die COMPUTE-Shader-Technologie wird auch als DirectCompute-Technologie bezeichnet. In diesem Thema wird die Verwendung von [Compute-Shadern](direct3d-11-advanced-stages-compute-shader.md) in einer Direct3D 11-App auf Direct3D 10-Hardware erläutert.

Die Unterstützung für Compute-Shader auf downlevelhardware gilt nur für Geräte, die mit Direct3D 10. x kompatibel sind. Compute-Shader können nicht auf Direct3D 9. x-Hardware verwendet werden.

Um zu überprüfen, ob Direct3D 10. x-Hardware Compute-Shader unterstützt, wenden Sie [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport)an. Übergeben Sie **im checkfeaturesupport** -Befehl den D3D11 \_ Feature \_ d3d10 \_ X \_ Hardware \_ options-Wert an *den Feature* -Parameter, übergeben Sie einen Zeiger an die [**D3D11 \_ Feature \_ Data \_ d3d10 \_ x \_ Hardware \_ options**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) -Struktur an den *pfeaturesupportdata* -Parameter, und übergeben Sie die Größe der **D3D11 \_ Feature \_ Data \_ d3d10 \_ x \_ Hardware \_ options** -Struktur an den *featuresupportdatasize* -Parameter. **Checkfeaturesupport** gibt **true** in den **Berechnungen compueshaders \_ Plus \_ rawandstructuredbuffers \_ über \_ Shader \_ 4 \_ x** **D3D11 \_ Feature \_ Data \_ d3d10 \_ x \_ Hardware \_ Optionen** zurück, wenn die Hardware Direct3D 10. x Compute-Shader unterstützt.

Der [Verweis Bereich 10level9](d3d11-graphics-reference-10level9.md) listet die Unterschiede zwischen der Art und Weise, wie sich verschiedene [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -und [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Methoden auf verschiedenen 10 Level9-featureebenen

-   [Ungeordnete Zugriffs Sichten (UAVs)](#unordered-access-views-uavs)
-   [Shader-Ressourcen Sichten (Srvs)](#shader-resource-views-srvs)
-   [Thread Gruppen](#thread-groups)
    -   [Thread Gruppen Dimensionen](#thread-group-dimensions)
    -   [Zweidimensionale Thread Indizes](#two-dimensional-thread-indices)
    -   [Thread Gruppe Shared Memory (TGSM)](#thread-group-shared-memory-tgsm)
-   [D3DCompile mit D3DCompile \_ Skip- \_ Optimierung](/windows)
-   [Zugehörige Themen](#related-topics)

## <a name="unordered-access-views-uavs"></a>Ungeordnete Zugriffs Sichten (UAVs)

Rohdaten ([roteaddressbuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) und strukturierte ([rwstructuredbuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) ungeordnete Zugriffs Sichten werden auf downlevelhardware unterstützt, wobei die folgenden Einschränkungen gelten:

-   Nur eine einzige UAV kann jeweils über [**Verknüpfung id3d11devicecontext aus:: cssetunorderedaccessviews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)an eine Pipeline gebunden werden.
-   Der Basis Offset für eine unformatierte UAV muss an einer 256-Byte-Begrenzung ausgerichtet sein (anstelle von 16-Byte-Ausrichtung, die für Direct3D 11-Hardware erforderlich ist).

Typisierte UAVs werden auf downlevelhardware nicht unterstützt. Dies umfasst [Texture1D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d)-, [Texture2D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)-und [Texture3D](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d) -UAVs.

Pixel-Shader auf downlevelhardware unterstützen den ungeordneten Zugriff nicht.

## <a name="shader-resource-views-srvs"></a>Shader-Ressourcen Sichten (Srvs)

Rohdaten und strukturierte Puffer als shaderressourcensichten werden auf downlevelhardware für den schreibgeschützten Zugriff unterstützt, da Sie sich auf Direct3D 11-Hardware befinden. Diese Ressourcentypen werden für Vertex-Shader, Geometry-Shader, Pixel-Shader und Compute-Shader unterstützt.

## <a name="thread-groups"></a>Thread Gruppen

Ein Compute-Shader kann in vielen Threads parallel innerhalb einer Thread Gruppe ausgeführt werden.

Thread Gruppen werden auf downlevelhardware unterstützt, wobei die folgenden Einschränkungen gelten:

### <a name="thread-group-dimensions"></a>Thread Gruppen Dimensionen

Thread Gruppen, die für downlevelhardware definiert sind, sind auf die X-und Y-Abmessungen von 768 beschränkt. Dieser Wert ist geringer als die maximale Anzahl von 1024 für Direct3D 11-Hardware. Die maximale Z-Dimension von 64 ist unverändert.

Die Gesamtanzahl der Threads in der Gruppe (X × X × Z) ist auf 768 beschränkt. Dies ist kleiner als das Limit von 1024 für Direct3D 11-Hardware.

Wenn diese Zahlen überschritten werden, schlägt die Shader-Kompilierung fehl.

### <a name="two-dimensional-thread-indices"></a>Thread Indizes Two-Dimensional

Ein bestimmter Thread innerhalb einer Thread Gruppe wird mithilfe eines 3D-Vektors indiziert, der von (x, y, z) angegeben wird.

Für Compute-Shader, die auf downlevelhardware betrieben werden, unterstützen Thread Gruppen nur zwei Dimensionen. Dies bedeutet, dass der Z-Wert im 3D-Vektor immer 1 sein muss.

Diese Einschränkung gilt speziell für Folgendes:

-   [**Verknüpfung id3d11devicecontext aus::D ispatch**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch)– das *threadgroupzähl-* Argument muss 1 sein.
-   [**Verknüpfung id3d11devicecontext aus::D ispatchindirekte**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect)– diese Funktion wird auf downlevelhardware nicht unterstützt.
-   [numThreads](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads)– der Z-Wert muss 1 sein.

### <a name="thread-group-shared-memory-tgsm"></a>Thread Gruppe Shared Memory (TGSM)

Der gemeinsam genutzte Speicher der Thread Gruppe ist auf eine downlevelhardware auf 16 KB beschränkt. Dieser Wert ist kleiner als 32 KB, der für Direct3D 11-Hardware verfügbar ist.

Ein Compute-Shader-Thread kann nur in eine eigene TGSM-Region schreiben. Dieser schreibgeschützte Bereich hat eine maximale Größe von 256 Bytes oder weniger, wobei die maximale Anzahl der Threads, die für die Gruppe deklariert sind, zunimmt.

In der folgenden Tabelle wird die maximale Größe eines TGSM-Bereichs pro Thread für die Anzahl der Threads in der Gruppe definiert:



| Anzahl der Threads in der Gruppe | Maximale TGSM-Größe pro Thread |
|----------------------------|------------------------------|
| 0-64                       | 256                          |
| 65-68                      | 240                          |
| 69-72                      | 224                          |
| 73-76                      | 208                          |
| 77-84                      | 192                          |
| 85-92                      | 176                          |
| 93-100                     | 160                          |
| 101-112                    | 144                          |
| 113-128                    | 128                          |
| 129-144                    | 112                          |
| 145-168                    | 96                           |
| 169-204                    | 80                           |
| 205-256                    | 64                           |
| 257-340                    | 48                           |
| 341-512                    | 32                           |
| 513-768                    | 16                           |



 

Ein Compute-Shader-Thread kann die TGSM von einem beliebigen Speicherort lesen.

## <a name="d3dcompile-with-d3dcompile_skip_optimization"></a>D3DCompile mit D3DCompile \_ Skip- \_ Optimierung

[**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) gibt **E \_ notimpl** zurück, wenn Sie CS \_ 4 \_ 0 als Shader-Ziel zusammen mit der Kompilierungs Option [**D3DCompile \_ Skip \_ Optimization**](/windows/desktop/direct3dhlsl/d3dcompile-constants) übergeben. Das CS \_ 5 \_ 0-Shader-Ziel funktioniert mit der **D3DCOMPILE \_ Skip- \_ Optimierung**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11 auf downlevelhardware](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 