---
title: Entpacken und Verpacken DXGI_FORMAT für die In-Place Bildbearbeitung
description: Die D3DX \_ dxgiformatconvert. INL-Datei enthält Funktionen für Inline Formatkonvertierungen, die Sie im COMPUTE-Shader oder Pixel-Shader auf Direct3D 11-Hardware verwenden können.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04f3729bbeda5b0677da9d52e595e621523ff2d1
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106368283"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a>Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung

Die D3DX \_ dxgiformatconvert. INL-Datei enthält Funktionen für Inline Formatkonvertierungen, die Sie im COMPUTE-Shader oder Pixel-Shader auf Direct3D 11-Hardware verwenden können. Sie können diese Funktionen in der Anwendung verwenden, um gleichzeitig Lese-und Schreibvorgänge für eine Textur auszuführen. Das heißt, Sie können eine direkte Bildbearbeitung ausführen. Um diese Funktionen für die Inline Formatkonvertierung zu verwenden, schließen \_ Sie die Datei D3DX dxgiformatconvert. INL in Ihre Anwendung ein.

> Der D3DX \_ dxgiformatconvert. INL-Header wird im Legacy-DirectX-SDK ausgeliefert. Es ist auch im nuget-Paket [Microsoft. dxsdk. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) enthalten.

Die unsortierter Zugriffs Ansicht (UAV) von Direct3D 11 einer Texture1D-, Texture2D-oder Texture3D-Ressource unterstützt den zufälligen Zugriff auf Lese-und Schreibvorgänge von einem Compute-Shader oder Pixel-Shader in den Arbeitsspeicher. Allerdings unterstützt Direct3D 11 gleichzeitige Lese-und Schreibvorgänge für das DXGI- \_ Format \_ R32 \_ uint. Beispielsweise unterstützt Direct3D 11 nicht gleichzeitiges Lesen von und Schreiben in andere, nützlichere Formate, wie z. b. DXGI- \_ Format \_ R8G8B8A8 \_ unorm. Sie können nur einen UAV-Vorgang für den zufälligen Zugriff auf solche anderen Formate verwenden, oder Sie können nur einen Shader-Ressourcenansicht (SRV) für den zufälligen Zugriff verwenden, der aus solchen anderen Formaten gelesen wird. Die Hardware für die Format Konvertierung ist nicht verfügbar, um gleichzeitig Lese-und Schreibvorgänge in solchen anderen Formaten auszuführen.

Sie können jedoch gleichzeitig sowohl aus solchen anderen Formaten lesen als auch schreiben, indem Sie die Textur in das DXGI- \_ Format \_ R32 \_ uint-Textur Format umwandeln, wenn Sie eine UAV erstellen, solange das ursprüngliche Format der Ressource eine Umwandlung in das DXGI- \_ Format \_ R32 \_ uint unterstützt. Die meisten 32 Bit pro Element Formate unterstützen die Umwandlung in das DXGI- \_ Format \_ R32 \_ uint Wenn Sie die Textur in das DXGI- \_ Format \_ R32 \_ uint-Textur Format umwandeln, wenn Sie eine UAV erstellen, können Sie dann gleichzeitig Lese-und Schreibvorgänge in die Textur ausführen, solange der Shader beim Schreiben beim Lesen und Verpacken das manuelle formatieren beim Schreiben durchführt.

Der Vorteil der Umwandlung der Textur in das DXGI- \_ Format von \_ R32 \_ uint ist, dass Sie später das entsprechende Format (z. b. DXGI- \_ Format \_ R16G16 \_ float) mit anderen Sichten in derselben Textur verwenden können, wie z. b. renderzielsichten (rtvs) oder Srvs. Aus diesem Grund kann die Hardware das typische automatische Format entpacken und Verpacken, eine Textur Filterung durchführen usw., wenn keine Hardware Einschränkungen vorhanden sind.

Das folgende Szenario erfordert, dass eine Anwendung die folgenden Aktionen ausführt, um eine direkte Bildbearbeitung auszuführen.

Angenommen, Sie möchten eine Textur erstellen, in der Sie einen PixelShader oder einen Compute-Shader verwenden können, um eine direkte Bearbeitung auszuführen, und Sie möchten, dass die Textur Daten in einem Format gespeichert werden, das einem der folgenden typlosen Formate untergeordnet ist:

-   DXGI- \_ Format \_ R10G10B10A2 \_ typlose
-   DXGI- \_ Format \_ R8G8B8A8 \_ typlose
-   DXGI- \_ Format \_ B8G8R8A8 \_ typlose
-   DXGI- \_ Format \_ B8G8R8X8 \_ typlose
-   DXGI- \_ Format \_ R16G16 \_ typlose

Das DXGI- \_ Format \_ R10G10B10A2 \_ unorm-Format ist beispielsweise ein Nachfolger des DXGI-Formats \_ \_ R10G10B10A2 \_ typlose Format. Daher unterstützt das DXGI- \_ Format \_ R10G10B10A2 \_ unorm das Verwendungs Muster, das in der folgenden Reihenfolge beschrieben wird. Formate, die von einem typlosen DXGI-Format (z. b. \_ \_ \_ DXGI- \_ Format \_ R32 float) abgeleitet werden, \_ werden trivial unterstützt, ohne dass eine der in der folgenden Sequenz beschriebenen Format Konvertierungs Hilfe erforderlich ist.

**So führen Sie eine direkte Bildbearbeitung aus**

1.  Erstellen Sie eine Textur mit dem entsprechenden typlosen abhängigen Format, das im vorherigen Szenario angegeben ist, sowie die erforderlichen Bindungsflags, z \_ . b. D3D11 Bind \_ \_ unorderaccess \| D3D11 \_ Bind \_ Shader \_ Resource.
2.  Erstellen Sie für eine direkte Bildbearbeitung eine UAV mit dem DXGI- \_ Format \_ R32 \_ uint. Die Direct3D 11-API lässt in der Regel keine Umwandlung zwischen unterschiedlichen Format "Familien" zu. Die API Direct3D 11 gibt jedoch eine Ausnahme mit dem DXGI- \_ Format \_ R32 \_ uint aus.
3.  Verwenden Sie im COMPUTE-Shader oder Pixel-Shader das entsprechende Inline Format Pack und die entpacken-Funktionen, die in der \_ Datei D3DX dxgiformatconvert. INL bereitgestellt werden. Nehmen wir beispielsweise an, dass das DXGI- \_ Format \_ R32 \_ uint UAV der Textur tatsächlich das DXGI \_ \_ -Format R10G10B10A2 \_ unorm-formatierte Daten enthält. Nachdem die Anwendung eine uint aus der UAV in den Shader gelesen hat, muss Sie die folgende Funktion aufrufen, um das Textur Format zu entpacken:

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    Wenn Sie dann im gleichen Shader in die UAV schreiben möchten, ruft die Anwendung die folgende Funktion auf, um Shader-Daten in einen uint zu packen, den die Anwendung in die UAV schreiben kann:

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  Die Anwendung kann dann andere Ansichten, z. b. Srvs, mit dem erforderlichen Format erstellen. Die Anwendung kann z. b. einen SRV mit dem DXGI- \_ Format \_ R10G10B10A2 \_ unorm Format erstellen, wenn die Ressource als DXGI- \_ Format \_ R10G10B10A2 \_ typlose erstellt wurde. Wenn ein Shader auf diesen SRV zugreift, kann die Hardware wie üblich eine automatische Typkonvertierung durchführen.

> [!Note]  
> Wenn der Shader nur in eine UAV schreiben oder als SRV gelesen werden muss, ist keiner dieser Konvertierungs Aufgaben erforderlich, da Sie vollständig typisierte UAVs oder Srvs verwenden können. Die in D3DX \_ dxgiformatconvert. INL bereitgestellten formatkonvertierungs Funktionen sind möglicherweise nur nützlich, wenn Sie gleichzeitige Lese-und Schreibvorgänge in eine UAV einer Textur durchführen möchten.

 

Im folgenden finden Sie eine Liste der formatkonvertierungs Funktionen, die in der \_ Datei D3DX dxgiformatconvert. INL enthalten sind. Diese Funktionen werden nach dem DXGI \_ -Format kategorisiert, das Sie entpacken und Verpacken. Jedes der unterstützten Formate wird von einem der im vorherigen Szenario aufgelisteten typlosen Formate abgeleitet und unterstützt die Umwandlung in das DXGI- \_ Format \_ R32 \_ uint als UAV.

<dl> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI- \_ Format \_ R10G10B10A2 \_ unorm
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI- \_ Format \_ R10G10B10A2 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI- \_ Format \_ R8G8B8A8 \_ unorm
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> Die \_ inexact-Type-Funktion verwendet shaderanweisungen ohne hohe Genauigkeit, um die genaue Antwort zu erhalten. Die Alternative Funktion verwendet eine im Shader gespeicherte Nachschlage Tabelle, um eine exakte sRGB->float-Konvertierung anzugeben.

 

</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI- \_ Format \_ R8G8B8A8 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI- \_ Format \_ R8G8B8A8 \_ snorm
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>DXGI- \_ Format \_ R8G8B8A8 \_ Sint
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI- \_ Format \_ B8G8R8A8 \_ unorm
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> Die \_ inexact-Type-Funktion verwendet shaderanweisungen ohne hohe Genauigkeit, um die genaue Antwort zu erhalten. Die Alternative Funktion verwendet eine im Shader gespeicherte Nachschlage Tabelle, um eine exakte sRGB->float-Konvertierung anzugeben.

 

</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI- \_ Format \_ B8G8R8X8 \_ unorm
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> Die \_ inexact-Type-Funktion verwendet shaderanweisungen ohne hohe Genauigkeit, um die genaue Antwort zu erhalten. Die Alternative Funktion verwendet eine im Shader gespeicherte Nachschlage Tabelle, um eine exakte sRGB->float-Konvertierung anzugeben.

 

</dd> <dt>

<span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI- \_ Format \_ R16G16 \_ float
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI- \_ Format \_ R16G16 \_ unorm
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI- \_ Format \_ R16G16 \_ uint
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI- \_ Format \_ R16G16 \_ snorm
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI- \_ Format \_ R16G16 \_ Sint
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

 

 




