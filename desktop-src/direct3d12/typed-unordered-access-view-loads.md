---
title: Typisierte UAV-Ladevorgänge (unsortierter Zugriffs Ansicht)
description: Die gegebene UAV-Auslastung (unsortierter Zugriffs Ansicht) ist die Fähigkeit eines Shaders, aus einer UAV mit einem bestimmten DXGI-Format zu lesen \_ .
ms.assetid: 6106D15E-EAF6-4583-B4F2-7CC7EE30DE15
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4adfd7511590a43b7f87507c5a1e0a2a87c925b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548674"
---
# <a name="typed-unordered-access-view-uav-loads"></a>Typisierte UAV-Ladevorgänge (unsortierter Zugriffs Ansicht)

Die gegebene UAV-Auslastung (unsortierter Zugriffs Ansicht) ist die Fähigkeit eines Shaders, aus einer UAV mit einem bestimmten [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)zu lesen.

-   [Übersicht](#overview)
-   [Unterstützte Formate und API-Aufrufe](#supported-formats-and-api-calls)
-   [Verwenden von typisierten UAV-Ladungen aus HLSL](#using-typed-uav-loads-from-hlsl)
-   [Verwenden von unorm-und snorm-typisierten UAV-Ladungen aus HLSL](#using-unorm-and-snorm-typed-uav-loads-from-hlsl)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Überblick

Eine ungeordnete Zugriffs Ansicht (UAV) ist eine Ansicht einer unsorierten Zugriffs Ressource (die auch Puffer, Texturen und Textur Arrays enthalten kann, ohne Multisampling). Eine UAV ermöglicht Temporale ungeordnete Lese-/Schreibzugriffe aus mehreren Threads. Dies bedeutet, dass dieser Ressourcentyp gleichzeitig von mehreren Threads gelesen/geschrieben werden kann, ohne dass Speicher Konflikte entstehen. Dieser gleichzeitige Zugriff wird durch die Verwendung von [atomaren Funktionen](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)gehandhabt.

D3D12 (und D3D 11.3) erweitert die Liste der Formate, die mit typisierten UAV-Ladevorgängen verwendet werden können.

## <a name="supported-formats-and-api-calls"></a>Unterstützte Formate und API-Aufrufe

Bisher unterstützten die folgenden drei Formate typisierte UAV-Ladungen und waren für die D3D 11.0-Hardware erforderlich. Sie werden für alle D3D 11.3-und D3D12-Hardware unterstützt.

-   R32 \_ float
-   R32 \_ uint
-   R32 \_ Sint

Die folgenden Formate werden als Satz auf D3D12-oder D3D 11.3-Hardware unterstützt. Wenn eine solche unterstützt wird, werden alle unterstützt.

-   R32G32B32A32 \_ float
-   R32G32B32A32 \_ uint
-   R32G32B32A32 \_ Sint
-   R16G16B16A16 \_ float
-   R16G16B16A16 \_ uint
-   R16G16B16A16 \_ Sint
-   R8G8B8A8 \_ unorm
-   R8G8B8A8 \_ uint
-   R8G8B8A8 \_ Sint
-   R16 \_ float
-   R16 \_ uint
-   R16 \_ Sint
-   R8- \_ unorm
-   R8 \_ uint
-   R8 \_ Sint

Die folgenden Formate werden optional und einzeln auf D3D12-und D3D 11.3-Hardware unterstützt. Daher muss eine einzelne Abfrage für jedes Format durchgeführt werden, um die Unterstützung zu testen.

-   R16G16B16A16 \_ unorm
-   R16G16B16A16 \_ snorm
-   R32G32 \_ float
-   R32G32 \_ uint
-   R32G32 \_ Sint
-   R10G10B10A2 \_ unorm
-   R10G10B10A2 \_ uint
-   R11G11B10 \_ float
-   R8G8B8A8 \_ snorm
-   R16G16 \_ float
-   R16G16 \_ unorm
-   R16G16 \_ uint
-   R16G16 \_ snorm
-   R16G16 \_ Sint
-   R8G8 \_ unorm
-   R8G8 \_ uint
-   R8G8 \_ snorm
-   R8G8 \_ Sint
-   R16 \_ unorm
-   R16 \_ snorm
-   R8 \_ snorm
-   A8- \_ unorm
-   B5G6R5 \_ unorm
-   B5G5R5A1 \_ unorm
-   B4G4R4A4 \_ unorm

Um die Unterstützung für weitere Formate zu ermitteln, müssen Sie [**checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) mit der [**D3D12 \_ Feature \_ Data \_ D3D12 \_ options**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) -Struktur als ersten Parameter aufrufen (siehe Funktions [Abfrage](capability-querying.md)). Das Feld *typeduavloadadditionalformats* wird festgelegt, wenn die oben genannte Liste als Satz unterstützt wird. Erstellen Sie einen zweiten aufrufungstyp **, indem Sie** eine [**D3D12 \_ Feature \_ Data \_ Format- \_ Unterstützungs**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_support) Struktur verwenden (Überprüfen der zurückgegebenen Struktur mit dem D3D12- \_ Format \_ SUPPORT2 \_ UAV \_ typisiertes \_ Load-Member des [**D3D12- \_ Formats \_ SUPPORT2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_format_support2) Enum), um die Unterstützung in der Liste der optional unterstützten, oben aufgeführten Formate zu ermitteln, z. b.:

``` syntax
D3D12_FEATURE_DATA_D3D12_OPTIONS FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Cannot assume other formats are supported, so we check:
        D3D12_FEATURE_DATA_FORMAT_SUPPORT FormatSupport = {DXGI_FORMAT_R32G32_FLOAT, D3D12_FORMAT_SUPPORT1_NONE, D3D12_FORMAT_SUPPORT2_NONE};
        hr = pDevice->CheckFeatureSupport(D3D12_FEATURE_FORMAT_SUPPORT, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.Support2 & D3D12_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
        {
            // DXGI_FORMAT_R32G32_FLOAT supports UAV Typed Load!
        }
    }
}
```

## <a name="using-typed-uav-loads-from-hlsl"></a>Verwenden von typisierten UAV-Ladungen aus HLSL

Bei typisierten UAVs ist das HLSL-Flag D3D \_ Shader \_ erfordert ein \_ typisiertes \_ UAV- \_ Laden \_ zusätzlicher \_ Formate.

Dies ist beispielsweise ein Shader-Code, der eine typisierte UAV-Auslastung verarbeitet:

``` syntax
RWTexture2D<float4> uav1;
uint2 coord;
float4 main() : SV_Target
{
  return uav1.Load(coord);
}
```

## <a name="using-unorm-and-snorm-typed-uav-loads-from-hlsl"></a>Verwenden von unorm-und snorm-typisierten UAV-Ladungen aus HLSL

Wenn Sie typisierte UAV-Ladungen zum Lesen aus einer unorm-oder snorm-Ressource verwenden, müssen Sie den Elementtyp des HLSL-Objekts ordnungsgemäß als oder deklarieren `unorm` `snorm` . Sie wird als nicht definiertes Verhalten angegeben, um den in HLSL deklarierten Elementtyp mit dem zugrunde liegenden Ressourcen Datentyp nicht abzugleichen. Wenn Sie z. b. typisierte UAV-Ladevorgänge für eine Puffer Ressource mit R8 \_ unorm-Daten verwenden, müssen Sie den Elementtyp wie folgt deklarieren `unorm float` :

``` syntax
RWBuffer<unorm float> uav;
```

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Darstellung](rendering.md)
</dt> <dt>

[Ressourcen Bindung](resource-binding.md)
</dt> <dt>

[Ressourcen Bindung in HLSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Shadermodell 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Angeben von Stamm Signaturen in HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 