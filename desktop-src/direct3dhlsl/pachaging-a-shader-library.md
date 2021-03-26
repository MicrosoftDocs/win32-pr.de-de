---
title: Verpacken einer shaderbibliothek
description: Hier erfahren Sie, wie Sie den Shader-Code kompilieren, den kompilierten Code in eine shaderbibliothek laden und Ressourcen von Quell Slots an Ziel Slots binden.
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90124ca9753a390b924d5ba702e1986e32eee9e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993558"
---
# <a name="packaging-a-shader-library"></a>Verpacken einer shaderbibliothek

Hier erfahren Sie, wie Sie den Shader-Code kompilieren, den kompilierten Code in eine shaderbibliothek laden und Ressourcen von Quell Slots an Ziel Slots binden.

**Ziel:** Zum Verpacken einer shaderbibliothek, die für die Shader-Verknüpfung verwendet werden soll.

## <a name="prerequisites"></a>Voraussetzungen

Es wird davon ausgegangen, dass Sie mit C+ vertraut sind. Sie müssen außerdem mit den grundlegenden Konzepten der Grafikprogrammierung vertraut sein.

**Zeit bis zum Abschluss:** 30 Minuten.

## <a name="instructions"></a>Instructions

### <a name="1-compiling-your-shader-code"></a>1. Kompilieren des Shader-Codes

Kompilieren Sie den Shader-Code mit einer der Kompilierungs Funktionen. Dieser Code Ausschnitt verwendet beispielsweise [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).

```cpp
    string source;
 
    ComPtr<ID3DBlob> codeBlob;
    ComPtr<ID3DBlob> errorBlob;
    HRESULT hr = D3DCompile(
        source.c_str(),
        source.size(),
        "ShaderModule",
        NULL,
        NULL,
        NULL,
        ("lib" + m_shaderModelSuffix).c_str(),
        D3DCOMPILE_OPTIMIZATION_LEVEL3,
        0,
        &codeBlob,
        &errorBlob
        );
```

Die Quell Zeichenfolge enthält den nicht kompilierten ASCII-HLSL-Code.

### <a name="2-load-the-compiled-code-into-a-shader-library"></a>2. Laden Sie den kompilierten Code in eine Shader-Bibliothek.

Aufrufen der [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) -Funktion, um den kompilierten Code ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) in ein Modul ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) zu laden, das eine Shader-Bibliothek darstellt.


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a>3. binden Sie Ressourcen von Quell Slots an Ziel Slots.

Rufen Sie die [**ID3D11Module:: kreateinstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) -Methode auf, um eine Instanz ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) der Bibliothek zu erstellen, damit Sie dann Ressourcen Bindungen für die Instanz definieren können.

Wenden Sie die Bind-Methoden von [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) an, um die benötigten Ressourcen aus den Quell Slots an Ziel Slots zu binden. Die Ressourcen können Texturen, Puffer, Samplern, Konstante Puffer oder UAVs sein. In der Regel verwenden Sie die gleichen Slots wie die Quell Bibliothek.


```C++
    // Create an instance of the library and define resource bindings for it.
    // In this sample we use the same slots as the source library however this is not required.
    ComPtr<ID3D11ModuleInstance> shaderLibraryInstance;
    DX::ThrowIfFailed(shaderLibrary->CreateInstance("", &shaderLibraryInstance));
    // HRESULTs for Bind methods are intentionally ignored as compiler optimizations may eliminate the source
    // bindings. In these cases, the Bind operation will fail, but the final shader will function normally.
    shaderLibraryInstance->BindResource(0, 0, 1);
    shaderLibraryInstance->BindSampler(0, 0, 1);
    shaderLibraryInstance->BindConstantBuffer(0, 0, 0);
    shaderLibraryInstance->BindConstantBuffer(1, 1, 0);
    shaderLibraryInstance->BindConstantBuffer(2, 2, 0);
```



Dieser HLSL-Code zeigt, dass die Quell Bibliothek die gleichen Slots (T0, S0, B0, B1 und B2) wie die Slots verwendet, die in den vorhergehenden Bind-Methoden von [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)verwendet werden.

``` syntax
// This is the default code in the fixed header section.
Texture2D<float3> Texture : register(t0);
SamplerState Anisotropic : register(s0);
cbuffer CameraData : register(b0)
{
    float4x4 Model;
    float4x4 View;
    float4x4 Projection;
};
cbuffer TimeVariantSignals : register(b1)
{
    float SineWave;
    float SquareWave;
    float TriangleWave;
    float SawtoothWave;
};

// This code is not displayed, but is used as part of the linking process.
cbuffer HiddenBuffer : register(b2)
{
    float3 LightDirection;
};
```

## <a name="summary-and-next-steps"></a>Zusammenfassung und nächste Schritte

Wir haben Shader-Code kompiliert, den kompilierten Code in eine shaderbibliothek geladen und Ressourcen von Quell Slots an Ziel Slots gebunden.

Im nächsten Schritt erstellen wir funktionsverknüpfungs Diagramme (FLGS) für Shader, verknüpfen Sie mit kompiliertem Code und erzeugen Shader-blobdateien, die von der Direct3D-Laufzeit verwendet werden können.

[Erstellen eines funktionsverknüpfungs Diagramms und Verknüpfen dieses Diagramms mit kompiliertem Code](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Shader-Verknüpfung](using-shader-linking.md)
</dt> </dl>

 

 