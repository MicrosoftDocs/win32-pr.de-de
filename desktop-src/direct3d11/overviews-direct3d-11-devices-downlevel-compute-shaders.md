---
title: Berechnen von Shadern auf hardware downlevelr Hardware
description: In diesem Thema wird erläutert, wie Compute-Shader in einer Direct3D 11-App auf Direct3D 10-Hardware verwendet werden.
ms.assetid: b864269f-c1f7-4253-888d-04d1ed3e6587
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673397d6974d2191acc1f5e30ccf8cae8b5b5f4b0ab5cae305360fef3e7186f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894470"
---
# <a name="compute-shaders-on-downlevel-hardware"></a>Berechnen von Shadern auf hardware downlevelr Hardware

Direct3D 11 bietet die [](direct3d-11-advanced-stages-compute-shader.md) Möglichkeit, Compute-Shader zu verwenden, die mit den meisten Direct3D 10.x-Hardware betrieben werden, mit einigen Einschränkungen des Betriebs. Die Compute-Shadertechnologie wird auch als DirectCompute-Technologie bezeichnet. In diesem Thema wird [](direct3d-11-advanced-stages-compute-shader.md) erläutert, wie Compute-Shader in einer Direct3D 11-App auf Direct3D 10-Hardware verwendet werden.

Die Unterstützung für Compute-Shader auf kompatibler Hardware ist nur für Geräte verfügbar, die mit Direct3D 10.x kompatibel sind. Compute-Shader können nicht auf Direct3D 9.x-Hardware verwendet werden.

Um zu überprüfen, ob Die Direct3D 10.x-Hardware Compute-Shader unterstützt, rufen Sie [**ID3D11Device::CheckFeatureSupport auf.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) Übergeben Sie im **CheckFeatureSupport-Aufruf** den Wert D3D11 FEATURE D3D10 X HARDWARE OPTIONS an den Feature-Parameter, übergeben Sie einen Zeiger auf die \_ \_ \_ \_ \_ [**D3D11 \_ FEATURE DATA \_ \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS-Struktur**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d10_x_hardware_options) an den *Parameter pFeatureSupportData,* und übergeben Sie die Größe der **D3D11 \_ FEATURE DATA \_ \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS-Struktur** an den *Parameter FeatureSupportDataSize.*  **CheckFeatureSupport** gibt **TRUE** in **den ComputeShaders \_ Plus \_ RawAndStructuredBuffers \_ Via \_ Shader \_ 4 \_ x** Member of **D3D11 \_ FEATURE DATA \_ \_ D3D10 \_ X HARDWARE \_ \_ OPTIONS** zurück, wenn die Direct3D 10.x-Hardware Computeshader unterstützt.

Im [Abschnitt Referenz zu 10Level9](d3d11-graphics-reference-10level9.md) werden die Unterschiede zwischen dem Verhalten verschiedener [**ID3D11Device-**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) und [**ID3D11DeviceContext-Methoden**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) auf verschiedenen 10Level9-Featureebenen aufgeführt.

-   [Ungeordnete Zugriffsansichten (Unordered Access Views, UAVs)](#unordered-access-views-uavs)
-   [Shaderressourcenansichten (SRVs)](#shader-resource-views-srvs)
-   [Threadgruppen](#thread-groups)
    -   [Threadgruppendimensionen](#thread-group-dimensions)
    -   [Zweidimensionale Threadindizes](#two-dimensional-thread-indices)
    -   [Freigegebener Speicher für Threadgruppen (TGSM)](#thread-group-shared-memory-tgsm)
-   [D3DCompile mit D3DCOMPILE \_ SKIP \_ OPTIMIZATION](/windows)
-   [Zugehörige Themen](#related-topics)

## <a name="unordered-access-views-uavs"></a>Ungeordnete Zugriffsansichten (Unordered Access Views, UAVs)

Ungeordnete Zugriffsansichten ([RWByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwbyteaddressbuffer)) und Structured ([RWStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-rwstructuredbuffer)) werden auf hardware downlevelr Hardware mit den folgenden Einschränkungen unterstützt:

-   Nur ein einzelner UAV kann gleichzeitig über [**ID3D11DeviceContext::CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)an eine Pipeline gebunden werden.
-   Der Basisoffset für eine unformatierte UAV muss an einer 256-Byte-Grenze ausgerichtet werden (anstelle einer 16-Byte-Ausrichtung, die für Direct3D 11-Hardware erforderlich ist).

Typierte UAVs werden auf downlevelr Hardware nicht unterstützt. Dies schließt [Texture1D-,](/windows/desktop/direct3dhlsl/sm5-object-rwtexture1d) [Texture2D-](/windows/desktop/direct3dhlsl/sm5-object-rwtexture2d)und [Texture3D-UAVs](/windows/desktop/direct3dhlsl/sm5-object-rwtexture3d) ein.

Pixel-Shader auf hardware downlevelr Hardware unterstützen keinen ungeordneten Zugriff.

## <a name="shader-resource-views-srvs"></a>Shaderressourcenansichten (SRVs)

Unformatierte und strukturierte Puffer als Shader-Ressourcenansichten werden auf hardware downlevelr Hardware für den schreibgeschützten Zugriff unterstützt, wie sie auf Direct3D 11-Hardware verwendet werden. Diese Ressourcentypen werden für Vertex-Shader, Geometrie-Shader, Pixel-Shader sowie Compute-Shader unterstützt.

## <a name="thread-groups"></a>Threadgruppen

Ein Compute-Shader kann auf vielen Threads parallel innerhalb einer Threadgruppe ausgeführt werden.

Threadgruppen werden auf hardware downlevelr hardwareunterstützter Hardware mit den folgenden Einschränkungen unterstützt:

### <a name="thread-group-dimensions"></a>Threadgruppendimensionen

Threadgruppen, die für downlevel-Hardware definiert sind, sind auf die X- und Y-Dimensionen 768 beschränkt. Dies ist kleiner als die maximal zulässigen Werte von 1024 für Direct3D 11-Hardware. Die maximale Z-Dimension von 64 bleibt unverändert.

Die Gesamtzahl der Threads in der Gruppe (X × Y × Z) ist auf 768 beschränkt. Dies ist kleiner als der Grenzwert von 1024 für Direct3D 11-Hardware.

Wenn diese Zahlen überschritten werden, kann die Shaderkompilierung nicht mehr verwendet werden.

### <a name="two-dimensional-thread-indices"></a>Two-Dimensional Threadindizes

Ein bestimmter Thread innerhalb einer Threadgruppe wird mithilfe eines 3D-Vektors indiziert, der von (x,y,z) angegeben wird.

Für Compute-Shader, die auf hardware downlevelr Hardware ausgeführt werden, unterstützen Threadgruppen nur zwei Dimensionen. Dies bedeutet, dass der Z-Wert im 3D-Vektor immer 1 sein muss.

Diese Einschränkung gilt insbesondere für Folgendes:

-   [**ID3D11DeviceContext::D ispatch:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatch)Das *ThreadGroupCountZ-Argument* muss 1 sein.
-   [**ID3D11DeviceContext::D ispatchIndirect:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dispatchindirect)Diese Funktion wird auf hardware downlevelr Hardware nicht unterstützt.
-   [numthreads](/windows/desktop/direct3dhlsl/sm5-attributes-numthreads): Der Z-Wert muss 1 sein.

### <a name="thread-group-shared-memory-tgsm"></a>Freigegebener Speicher für Threadgruppen (TGSM)

Shared Memory für Threadgruppen ist auf hardware downlevelr Hardware auf 16 KB beschränkt. Dies ist kleiner als die 32 KB, die für Direct3D 11-Hardware verfügbar sind.

Ein Compute-Shaderthread darf nur in seine eigene TGSM-Region schreiben. Dieser Schreibbereich hat eine maximale Größe von 256 Byte oder weniger, und der maximale Wert nimmt ab, wenn die Anzahl der für die Gruppe deklarierten Threads zunimmt.

In der folgenden Tabelle wird die maximale Größe eines TGSM-Region pro Thread für die Anzahl der Threads in der Gruppe definiert:



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



 

Ein Compute-Shaderthread kann das TGSM von einem beliebigen Ort aus lesen.

## <a name="d3dcompile-with-d3dcompile_skip_optimization"></a>D3DCompile mit D3DCOMPILE \_ SKIP \_ OPTIMIZATION

[**D3DCompile gibt**](/windows/desktop/direct3dhlsl/d3dcompile) **E \_ NOTIMPL** zurück, wenn Sie cs 4 0 zusammen mit der \_ Kompilierungsoption \_ [**D3DCOMPILE \_ SKIP \_ OPTIMIZATION**](/windows/desktop/direct3dhlsl/d3dcompile-constants) als Shaderziel übergeben. Das Cs \_ 5 \_ 0-Shaderziel funktioniert mit **D3DCOMPILE \_ SKIP \_ OPTIMIZATION**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11 auf Downlevelhardware](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 