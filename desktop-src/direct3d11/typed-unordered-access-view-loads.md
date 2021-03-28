---
title: Typisierte nicht geordnete zugriffsansichts Ladungen
description: Die gegebene UAV-Auslastung (unsortierter Zugriffs Ansicht) ist die Fähigkeit eines Shaders, aus einer UAV mit einem bestimmten DXGI-Format zu lesen \_ .
ms.assetid: BA72BF21-8621-461D-8677-9DFB7D5BC6AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0958b3563ab8001fd7b34ae62c9bcc37ad75c07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315453"
---
# <a name="typed-unordered-access-view-loads"></a>Typisierte nicht geordnete zugriffsansichts Ladungen

Die gegebene UAV-Auslastung (unsortierter Zugriffs Ansicht) ist die Fähigkeit eines Shaders, aus einer UAV mit einem bestimmten DXGI-Format zu lesen \_ .

-   [Übersicht](#overview)
-   [Unterstützte Formate und API-Aufrufe](#supported-formats-and-api-calls)
-   [Verwenden von typisierten UAV-Ladungen aus HLSL](#using-typed-uav-loads-from-hlsl)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Eine ungeordnete Zugriffs Ansicht (UAV) ist eine Ansicht einer unsorierten Zugriffs Ressource (die auch Puffer, Texturen und Textur Arrays enthalten kann, ohne Multisampling). Eine UAV ermöglicht Temporale ungeordnete Lese-/Schreibzugriffe aus mehreren Threads. Dies bedeutet, dass dieser Ressourcentyp gleichzeitig von mehreren Threads gelesen/geschrieben werden kann, ohne dass Speicher Konflikte entstehen. Dieser gleichzeitige Zugriff wird durch die Verwendung von [atomaren Funktionen](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-atomic-functions)gehandhabt.

D3D12 und D3D 11.3 werden in der Liste der Formate erweitert, die mit typisierten UAV-Ladevorgängen verwendet werden können.

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
-   8g8 \_ Sint
-   R16 \_ unorm
-   R16 \_ snorm
-   R8 \_ snorm
-   A8- \_ unorm
-   B5G6R5 \_ unorm
-   B5G5R5A1 \_ unorm
-   B4G4R4A4 \_ unorm

Um die Unterstützung für weitere Formate zu ermitteln, müssen Sie [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) mit der [**D3D11 \_ Feature \_ Data \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) -Struktur als ersten Parameter aufrufen. Das `TypedUAVLoadAdditionalFormats` Bit wird festgelegt, wenn die oben genannte Liste als Satz unterstützt wird. Erstellen Sie einen zweiten Rückruf von **checkfeaturesupport unter** Verwendung einer [**D3D11 \_ Feature \_ Data \_ Format \_ SUPPORT2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2) -Struktur (Überprüfen der zurückgegebenen Struktur mit dem D3D12- \_ Format \_ SUPPORT2 \_ UAV \_ typisiertes Load- \_ Member des D3D11- [**\_ Formats \_ SUPPORT2**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2) Enum), um die Unterstützung in der Liste der optional unterstützten Formate zu ermitteln, z. b.:

``` syntax
D3D11_FEATURE_DATA_D3D11_OPTIONS2 FeatureData;
ZeroMemory(&FeatureData, sizeof(FeatureData));
HRESULT hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS2, &FeatureData, sizeof(FeatureData));
if (SUCCEEDED(hr))
{
    // TypedUAVLoadAdditionalFormats contains a Boolean that tells you whether the feature is supported or not
    if (FeatureData.TypedUAVLoadAdditionalFormats)
    {
        // Can assume “all-or-nothing” subset is supported (e.g. R32G32B32A32_FLOAT)
        // Can not assume other formats are supported, so we check:
        D3D11_FEATURE_DATA_FORMAT_SUPPORT2 FormatSupport;
        ZeroMemory(&FormatSupport, sizeof(FormatSupport));
        FormatSupport.InFormat = DXGI_FORMAT_R32G32_FLOAT;
        hr = pDevice->CheckFeatureSupport(D3D11_FEATURE_FORMAT_SUPPORT2, &FormatSupport, sizeof(FormatSupport));
        if (SUCCEEDED(hr) && (FormatSupport.OutFormatSupport2 & D3D11_FORMAT_SUPPORT2_UAV_TYPED_LOAD) != 0)
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

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D 11,3-Features](direct3d-11-3-features.md)
</dt> <dt>

[Shadermodell 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> </dl>

 

 