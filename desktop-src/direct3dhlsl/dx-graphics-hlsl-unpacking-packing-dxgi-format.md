---
title: Entpacken und Packen von DXGI_FORMAT für In-Place Bildbearbeitung
description: Die Datei D3DX \_ DXGIFormatConvert.inl enthält Inlineformatkonvertierungsfunktionen, die Sie im Compute-Shader oder Pixel-Shader auf Direct3D 11-Hardware verwenden können.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 906c26151f0499a89c03c42bef4705bc7e58ddd59c8c55cb8d361c22a86a7cd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118090447"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a>Entpacken und Packen von DXGI \_ FORMAT für In-Place Bildbearbeitung

Die Datei D3DX \_ DXGIFormatConvert.inl enthält Inlineformatkonvertierungsfunktionen, die Sie im Compute-Shader oder Pixel-Shader auf Direct3D 11-Hardware verwenden können. Sie können diese Funktionen in Ihrer Anwendung verwenden, um gleichzeitig aus einer Textur zu lesen und in eine Textur zu schreiben. Das heißt, Sie können eine direkte Bildbearbeitung durchführen. Um diese Inlineformatkonvertierungsfunktionen zu verwenden, schließen Sie die Datei D3DX \_ DXGIFormatConvert.inl in Ihre Anwendung ein.

> Der D3DX \_ DXGIFormatConvert.inl-Header ist im Legacy-DirectX SDK enthalten. Es ist auch im [Paket Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet enthalten.

Die ungeordnete Zugriffsansicht (Unordered Access View, UAV) von Direct3D 11 einer Texture1D-, Texture2D- oder Texture3D-Ressource unterstützt zufällige Lese- und Schreibvorgänge in den Arbeitsspeicher von einem Compute-Shader oder Pixel-Shader. Direct3D 11 unterstützt jedoch gleichzeitig sowohl das Lesen aus als auch das Schreiben in das DXGI \_ FORMAT \_ R32 \_ UINT-Texturformat. Direct3D 11 unterstützt beispielsweise nicht gleichzeitig sowohl das Lesen aus als auch das Schreiben in andere nützliche Formate, z. B. DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM. Sie können nur einen UAV für den zufälligen Schreibzugriff auf solche anderen Formate verwenden, oder Sie können nur einen Shader Ressourcenansicht (SRV) verwenden, um zufälligen Zugriff auf Lesezugriff aus solchen anderen Formaten zu erhalten. Formatkonvertierungshardware ist nicht für das gleichzeitige Lesen aus und Schreiben in solche anderen Formate verfügbar.

Sie können jedoch immer noch gleichzeitig aus solchen anderen Formaten lesen und in diese schreiben, indem Sie die Textur beim Erstellen eines UAV in das DXGI \_ FORMAT \_ R32 \_ UINT-Texturformat umwandeln, sofern das ursprüngliche Format der Ressource die Umwandlung in DXGI \_ FORMAT \_ R32 \_ UINT unterstützt. Die meisten Formate mit 32 Bit pro Element unterstützen die Umwandlung in DXGI \_ FORMAT \_ R32 \_ UINT. Indem Sie die Textur beim Erstellen eines UAV in das \_ DXGI FORMAT \_ R32 \_ UINT-Texturformat umwandeln, können Sie gleichzeitig Lese- und Schreibvorgänge in die Textur ausführen, solange der Shader das manuelle Entpacken des Formats beim Lesen und Packen beim Schreiben ausführt.

Der Vorteil der Umwandlung der Textur in das \_ DXGI FORMAT \_ R32 \_ UINT-Texturformat besteht darin, dass Sie später das entsprechende Format (z. B. DXGI \_ FORMAT \_ R16G16 \_ FLOAT) mit anderen Ansichten auf derselben Textur verwenden können, z. B. RenderZielansichten (RTVs) oder SRVs. Daher kann die Hardware das typische automatische Format entpacken und packen, texturfiltern usw. dort, wo es keine Hardwareeinschränkungen gibt.

Das folgende Szenario erfordert, dass eine Anwendung die folgende Sequenz von Aktionen ausführt, um die direkte Bildbearbeitung durchzuführen.

Angenommen, Sie möchten eine Textur erstellen, für die Sie einen Pixelshader oder Compute-Shader verwenden können, um eine direkte Bearbeitung durchzuführen, und sie möchten, dass die Texturdaten in einem Format gespeichert werden, das ein Nachfolger eines der folgenden TYPELESS-Formate ist:

-   \_DXGI-FORMAT \_ R10G10B10A2 \_ TYPLOS
-   \_DXGI-FORMAT \_ R8G8B8A8 \_ TYPLOS
-   \_DXGI-FORMAT \_ B8G8R8A8 \_ TYPLESS
-   \_DXGI-FORMAT \_ B8G8R8X8 \_ TYPLESS
-   \_DXGI-FORMAT \_ R16G16 \_ TYPLOS

Beispielsweise ist das \_ UNORM-Format DXGI FORMAT \_ R10G10B10A2 \_ ein Nachfolger des DXGI FORMAT \_ \_ R10G10B10A2 \_ TYPELESS-Formats. Daher unterstützt DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM das in der folgenden Sequenz beschriebene Verwendungsmuster. Formate, die von DXGI \_ FORMAT \_ R32 TYPELESS abgeleitet \_ sind, z. B. DXGI \_ FORMAT \_ R32 \_ FLOAT, werden trivial unterstützt, ohne dass eine der in der folgenden Sequenz beschriebenen Formatkonvertierungshilfeen erforderlich ist.

**So führen Sie die direkte Bildbearbeitung aus**

1.  Erstellen Sie eine Textur mit dem entsprechenden TYPELESS-abhängigen Format, das im vorherigen Szenario angegeben wurde, zusammen mit den erforderlichen Bindungsflags, z. B. D3D11 \_ BIND \_ UNORDERED \_ ACCESS \| D3D11 \_ BIND \_ SHADER \_ RESOURCE.
2.  Erstellen Sie für die direkte Bildbearbeitung ein UAV mit dem DXGI \_ FORMAT \_ R32 \_ UINT-Format. Die Direct3D 11-API lässt in der Regel keine Umwandlung zwischen verschiedenen Formaten "Familien" zu. Die Direct3D 11-API macht jedoch eine Ausnahme mit dem DXGI \_ FORMAT \_ R32 \_ UINT-Format.
3.  Verwenden Sie im Compute-Shader oder Pixel-Shader die entsprechenden Inlineformatpaket- und Entpackfunktionen, die in der Datei D3DX \_ DXGIFormatConvert.inl bereitgestellt werden. Angenommen, das DXGI \_ FORMAT \_ R32 \_ UINT UAV der Textur enthält tatsächlich DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM-formatierte Daten. Nachdem die Anwendung einen Uint aus dem UAV in den Shader gelesen hat, muss sie die folgende Funktion aufrufen, um das Texturformat zu entpacken:

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    Um dann in den UAV im gleichen Shader zu schreiben, ruft die Anwendung die folgende Funktion auf, um Shaderdaten in einen UINT zu packen, den die Anwendung in den UAV schreiben kann:

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  Die Anwendung kann dann andere Ansichten, z. B. SRVs, mit dem erforderlichen Format erstellen. Beispielsweise kann die Anwendung einen SRV mit dem \_ UNORM-Format DXGI FORMAT \_ R10G10B10A2 \_ erstellen, wenn die Ressource als DXGI \_ FORMAT \_ R10G10B10A2 TYPELESS erstellt \_ wurde. Wenn ein Shader auf diesen SRV zugreift, kann die Hardware wie gewohnt eine automatische Typkonvertierung durchführen.

> [!Note]  
> Wenn der Shader nur in einen UAV schreiben oder als SRV lesen darf, ist keine dieser Konvertierungsarbeiten erforderlich, da Sie vollständig typisierte UAVs oder SRVs verwenden können. Die in D3DX DXGIFormatConvert.inl bereitgestellten Formatkonvertierungsfunktionen \_ sind möglicherweise nur nützlich, wenn Sie gleichzeitiges Lesen aus und Schreiben in eine UAV einer Textur durchführen möchten.

 

Im Folgenden ist die Liste der Formatkonvertierungsfunktionen aufgeführt, die in der Datei D3DX \_ DXGIFormatConvert.inl enthalten sind. Diese Funktionen werden nach dem DXGI FORMAT kategorisiert, \_ das sie entpacken und packen. Jedes der unterstützten Formate stammt von einem der im vorherigen Szenario aufgeführten TYPELESS-Formate und unterstützt die Umwandlung in DXGI \_ FORMAT \_ R32 \_ UINT als UAV.

<dl> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI \_ FORMAT \_ R10G10B10A2 \_ UINT
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>\_DXGI-FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> Die \_ Funktion "inexact-type" verwendet Shaderanweisungen, die nicht über eine ausreichende Genauigkeit verfügen, um die genaue Antwort zu geben. Die alternative Funktion verwendet eine im Shader gespeicherte Nachschlagetabelle, um eine genaue SRGB->Float-Konvertierung zu ermöglichen.

 

</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI \_ FORMAT \_ R8G8B8A8 \_ UINT
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>\_DXGI-FORMAT \_ R8G8B8A8 \_ SINT
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>\_DXGI-FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> Die \_ Funktion "inexact-type" verwendet Shaderanweisungen, die nicht über eine ausreichende Genauigkeit verfügen, um die genaue Antwort zu geben. Die alternative Funktion verwendet eine im Shader gespeicherte Nachschlagetabelle, um eine genaue SRGB->Float-Konvertierung zu ermöglichen.

 

</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>\_DXGI-FORMAT \_ B8G8R8X8 \_ UNORM
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>\_DXGI-FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> Die \_ Funktion "inexact-type" verwendet Shaderanweisungen, die nicht über eine ausreichende Genauigkeit verfügen, um die genaue Antwort zu geben. Die alternative Funktion verwendet eine im Shader gespeicherte Nachschlagetabelle, um eine genaue SRGB->Float-Konvertierung zu ermöglichen.

 

</dd> <dt>

<span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI \_ FORMAT \_ R16G16 \_ FLOAT
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>\_DXGI-FORMAT \_ R16G16 \_ UNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI \_ FORMAT \_ R16G16 \_ UINT
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>\_DXGI-FORMAT \_ R16G16 \_ SNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>\_DXGI-FORMAT \_ R16G16 \_ SINT
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a>Verwandte Themen

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieranleitung für HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




