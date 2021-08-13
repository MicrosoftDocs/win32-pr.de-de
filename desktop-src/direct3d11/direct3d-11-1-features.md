---
title: Direct3D 11.1-Features
description: Die folgende Funktionalität wurde in Direct3D 11.1 hinzugefügt, die in Windows 8, Windows RT und Windows Server 2012 enthalten ist.
ms.assetid: 2203D2D2-ECF6-4753-90FA-12A52678DFBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee5f4721a9f7ef7727539387603e839f36690ed5d4b6762121ceddefa0672ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535965"
---
# <a name="direct3d-111-features"></a>Direct3D 11.1-Features

Die folgende Funktionalität wurde in Direct3D 11.1 hinzugefügt, die in Windows 8, Windows RT und Windows Server 2012 enthalten ist. Teilunterstützung für [Direct3D 11.1](direct3d-11-features.md) ist auf Windows 7 und Windows Server 2008 R2 über das [Plattformupdate für Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)verfügbar, das über das [Plattformupdate für Windows 7](https://support.microsoft.com/kb/2670838)verfügbar ist.

-   [Shader-Ablaufverfolgung und Compilerverbesserungen](#shader-tracing-and-compiler-enhancements)
-   [Direct3D-Gerätefreigabe](#direct3d-device-sharing)
-   [Überprüfen der Unterstützung neuer Direct3D 11.1-Features und -Formate](#check-support-of-new-direct3d-111-features-and-formats)
-   [Verwenden der mindesten HLSL-Genauigkeit](#use-hlsl-minimum-precision)
-   [Angeben von Benutzerclipebenen in HLSL auf Featureebene 9 und höher](#specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Erstellen größerer Konstantenpuffer, auf die ein Shader zugreifen kann](#create-larger-constant-buffers-than-a-shader-can-access)
-   [Verwenden logischer Vorgänge in einem Renderziel](#use-logical-operations-in-a-render-target)
-   [Erzwingen der Stichprobenanzahl zum Erstellen eines Rasterisierungszustands](#force-the-sample-count-to-create-a-rasterizer-state)
-   [Verarbeiten von Videoressourcen mit Shadern](#process-video-resources-with-shaders)
-   [Erweiterte Unterstützung für freigegebene Texture2D-Ressourcen](#extended-support-for-shared-texture2d-resources)
-   [Ändern von Unterressourcen mit neuen Kopieroptionen](#change-subresources-with-new-copy-options)
-   [Verwerfen von Ressourcen und Ressourcenansichten](#discard-resources-and-resource-views)
-   [Unterstützung einer größeren Anzahl von UAVs](#support-a-larger-number-of-uavs)
-   [Binden eines Unterbereichs eines konstanten Puffers an einen Shader](#bind-a-subrange-of-a-constant-buffer-to-a-shader)
-   [Abrufen des Unterbereichs eines konstanten Puffers, der an einen Shader gebunden ist](#retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader)
-   [Löschen einer Ressourcenansicht ganz oder teilweise](#clear-all-or-part-of-a-resource-view)
-   [Zuordnen von SRVs dynamischer Puffer ohne \_ OVERWRITE](/windows)
-   [Verwenden von UAVs in jeder Pipelinephase](#use-uavs-at-every-pipeline-stage)
-   [Erweiterte Unterstützung für WARP-Geräte](#extended-support-for-warp-devices)
-   [Verwenden von Direct3D in Sitzung 0-Prozessen](#use-direct3d-in-session-0-processes)
-   [Unterstützung für Schattenpuffer auf Featureebene 9](#support-for-shadow-buffer-on-feature-level-9)
-   [Zugehörige Themen](#related-topics)

## <a name="shader-tracing-and-compiler-enhancements"></a>Shader-Ablaufverfolgung und Compilerverbesserungen

Mit Direct3D 11.1 können Sie die Shader-Ablaufverfolgung verwenden, um sicherzustellen, dass Ihr Code wie vorgesehen ausgeführt wird. Andernfalls können Sie das Problem ermitteln und beheben. Das Windows Software Development Kit (SDK) für Windows 8 enthält HLSL-Compilererweiterungen. Die Shaderablaufverfolgung und der HLSL-Compiler werden in D3dcompiler \_nn.dll implementiert.

Die Shader-Ablaufverfolgungs-API und die Verbesserungen am HLSL-Compiler bestehen aus den folgenden Methoden und Funktionen.

-   [**ID3D11RefDefaultTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions)
-   [**ID3D11RefTrackingOptions::SetTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11reftrackingoptions-settrackingoptions)
-   [**ID3D11TracingDevice::SetShaderTrackingOptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11TracingDevice::SetShaderTrackingOptionsByType**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11ShaderTraceFactory::CreateShaderTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace)
-   [**ID3D11ShaderTrace::TraceReady**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-traceready)
-   [**ID3D11ShaderTrace::ResetTrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-resettrace)
-   [**ID3D11ShaderTrace::GetTraceStats**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-gettracestats)
-   [**ID3D11ShaderTrace::P SSelectStamp**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-psselectstamp)
-   [**ID3D11ShaderTrace::GetInitialRegisterContents**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents)
-   [**ID3D11ShaderTrace::GetStep**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getstep)
-   [**ID3D11ShaderTrace::GetWrittenRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getwrittenregister)
-   [**ID3D11ShaderTrace::GetReadRegister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getreadregister)
-   [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2)
-   [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)
-   [**D3DDisassemble11Trace**](/windows/desktop/direct3dhlsl/d3ddisassemble11trace)
-   [**D3DDisassembleRegion**](/windows/desktop/direct3dhlsl/d3ddisassembleregion)
-   [**D3DGetTraceInstructionOffsets**](/windows/desktop/direct3dhlsl/d3dgettraceinstructionoffsets)
-   [**D3DReadFileToBlob**](/windows/desktop/direct3dhlsl/d3dreadfiletoblob)
-   [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart)
-   [**D3DWriteBlobToFile**](/windows/desktop/direct3dhlsl/d3dwriteblobtofile)

Die Bibliothek D3dcompiler.lib erfordert D3dcompiler \_nn.dll. Diese DLL ist nicht Teil Windows 8. er befindet sich im \\ Ordner bin des Windows SDK für Windows 8 zusammen mit der Fxc.exe Befehlszeilenversion des HLSL-Compilers.

> [!Note]  
> Obwohl Sie diese Bibliotheks- und DLL-Kombination für die Entwicklung verwenden können, können Sie nicht Windows Store Apps bereitstellen, die diese Kombination verwenden. Daher müssen Sie stattdessen HLSL-Shader kompilieren, bevor Sie Ihre Windows Store-App versenden. Sie können Binärdateien für die HLSL-Kompilierung auf den Datenträger schreiben, oder der Compiler kann Header mit statischen Bytearrays generieren, die die Shaderblobdaten enthalten. Sie verwenden die [**ID3DBlob-Schnittstelle,**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) um auf die Blobdaten zuzugreifen. Rufen Sie zum Entwickeln Ihrer Windows Store-App [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2) oder [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) auf, um die HLSL-Rohdatenquelle zu kompilieren, und übertragen Sie die resultierenden Blobdaten dann an Direct3D.

 

## <a name="direct3d-device-sharing"></a>Direct3D-Gerätefreigabe

Direct3D 11.1 ermöglicht direct3D 10-APIs und Direct3D 11-APIs die Verwendung eines zugrunde liegenden Renderinggeräts.

Dieses Direct3D 11.1-Feature besteht aus den folgenden Methoden und schnittstellen.

-   [**ID3D11Device1::CreateDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate)
-   [**ID3D11DeviceContext1::SwapDeviceContextState**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate)
-   [**ID3DDeviceContextState**](/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate)

## <a name="check-support-of-new-direct3d-111-features-and-formats"></a>Überprüfen der Unterstützung neuer Direct3D 11.1-Features und -Formate

Mit Direct3D 11.1 können Sie nach neuen Features suchen, die der Grafiktreiber möglicherweise unterstützt, sowie nach neuen Möglichkeiten, wie ein Format auf einem Gerät unterstützt wird. Microsoft DirectX Graphic Infrastructure (DXGI) 1.2 gibt auch neue [**DXGI \_ FORMAT-Werte**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) an.

Dieses Direct3D 11.1-Feature besteht aus der folgenden API.

-   [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), [**D3D11 \_ FEATURE DATA ARCHITECTURE \_ \_ \_ INFO**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info), [**D3D11 \_ FEATURE DATA \_ \_ D3D9 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options), [**D3D11 \_ FEATURE DATA \_ \_ SHADER MIN PRECISION \_ \_ \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)und [**D3D11 \_ FEATURE DATA \_ \_ D3D9 \_ SHADOW \_ SUPPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support) structures
-   [**ID3D11Device::CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) with [**D3D11 \_ FORMAT SUPPORT DECODER \_ \_ \_ OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**D3D11 \_ FORMAT SUPPORT VIDEO PROCESSOR \_ \_ \_ \_ OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**D3D11 \_ FORMAT SUPPORT VIDEO PROCESSOR \_ \_ \_ \_ INPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**D3D11 \_ FORMAT SUPPORT VIDEO \_ \_ \_ ENCODER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)und [**D3D11 \_ FORMAT \_ SUPPORT2 OUTPUT MERGER LOGIC \_ \_ \_ \_ OP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)

## <a name="use-hlsl-minimum-precision"></a>Verwenden der mindesten HLSL-Genauigkeit

Ab Windows 8 können Grafiktreiber [HLSL-Skalardatentypen](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) mit minimaler Genauigkeit implementieren, indem sie eine beliebige Genauigkeit verwenden, die größer oder gleich der angegebenen Bitgenauigkeit ist. Wenn Ihr HLSL-Shadercode mit minimaler Genauigkeit auf Hardware verwendet wird, die hlsl-Mindestgenauigkeit implementiert, verbrauchen Sie weniger Arbeitsspeicherbandbreite und somit auch weniger Systemleistung.

Sie können die minimale Genauigkeitsunterstützung des Grafiktreibers abfragen, indem Sie [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) mit dem [**D3D11 \_ FEATURE \_ SHADER \_ MIN PRECISION \_ \_ SUPPORT-Wert**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) aufrufen. Übergeben Sie in diesem **ID3D11Device::CheckFeatureSupport-Aufruf** einen Zeiger auf eine [**D3D11 \_ FEATURE DATA \_ \_ SHADER MIN PRECISION \_ \_ \_ SUPPORT-Struktur,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support) die **ID3D11Device::CheckFeatureSupport** mit den minimalen Genauigkeitsstufen auffüllt, die der Treiber für die Pixelshader-Stufe und für andere Shaderstufen unterstützt. Die zurückgegebenen Informationen geben nur an, dass die Grafikhardware HLSL-Vorgänge mit einer niedrigeren Genauigkeit als die standardmäßige 32-Bit-Gleitkommagenauigkeit ausführen kann, garantiert jedoch nicht, dass die Grafikhardware tatsächlich mit einer niedrigeren Genauigkeit ausgeführt wird.

Sie müssen nicht mehrere Shader erstellen, die eine minimale Genauigkeit verwenden. Erstellen Sie stattdessen Shader mit minimaler Genauigkeit, und die Minimalgenauigkeitsvariablen verhalten sich mit vollständiger 32-Bit-Genauigkeit, wenn der Grafiktreiber meldet, dass keine minimale Genauigkeit unterstützt wird. Weitere Informationen zur minimalen HLSL-Genauigkeit finden Sie unter [Verwenden der minimalen HLSL-Genauigkeit.](/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision)

HLSL-Shader mit minimaler Genauigkeit funktionieren auf Betriebssystemen vor Windows 8 nicht.

## <a name="specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Angeben von Benutzerclipebenen in HLSL auf Featureebene 9 und höher

Ab Windows 8 können Sie das **Clipplanes-Funktionsattribut** in einer HLSL-Funktionsdeklaration anstelle von [SV \_ ClipDistance](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) verwenden, damit Ihr Shader sowohl auf [Featureebene](overviews-direct3d-11-devices-downlevel-intro.md) 9 x als auch auf [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-syntax) \_ Featureebene 10 und höher funktioniert. Weitere Informationen finden Sie unter [User clip planes on feature level 9 hardware (Benutzer clip planes on feature level 9 hardware ( Benutzer clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)).

## <a name="create-larger-constant-buffers-than-a-shader-can-access"></a>Erstellen größerer Konstantenpuffer, auf die ein Shader zugreifen kann

Mit Direct3D 11.1 können Sie konstante Puffer erstellen, die größer sind als die maximale konstante Puffergröße, auf die ein Shader zugreifen kann (4096 32-Bit-Konstanten \* mit vier Komponenten – 64 KB). Wenn Sie die Puffer später an die Pipeline binden, z. B. über [**PSSetConstantBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers) oder [**PSSetConstantBuffers1,**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)können Sie einen Pufferbereich angeben, auf den der Shader zugreifen kann, der innerhalb des Grenzwerts von 4096 liegt.

Direct3D 11.1 aktualisiert die [**ID3D11Device::CreateBuffer-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) für dieses Feature.

## <a name="use-logical-operations-in-a-render-target"></a>Verwenden logischer Vorgänge in einem Renderziel

Mit Direct3D 11.1 können Sie logische Vorgänge verwenden, anstatt in einem Renderziel zu mischen. Sie können Logikvorgänge jedoch nicht mit einer Mischung aus mehreren Renderzielen kombinieren.

Dieses Direct3D 11.1-Feature besteht aus der folgenden API.

-   [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1) mit [ **D3D11 \_ LOGIC \_ OP**](/windows/desktop/api/D3D11_1/ne-d3d11_1-d3d11_logic_op)

## <a name="force-the-sample-count-to-create-a-rasterizer-state"></a>Erzwingen der Stichprobenanzahl zum Erstellen eines Rasterisierungszustands

Mit Direct3D 11.1 können Sie beim Erstellen eines Rasterisierungszustands eine Anzahl von Stichproben erzwingen angeben.

Dieses Direct3D 11.1-Feature besteht aus der folgenden API.

-   [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)

> [!Note]  
>
> Wenn Sie mit der Anzahl der Stichproben rendern möchten, die auf 1 oder höher erzwungen wird, müssen Sie die folgenden Richtlinien befolgen:
>
> -   Binden Sie keine Tiefenschablonenansichten.
> -   Deaktivieren Sie Tiefentests.
> -   Stellen Sie sicher, dass der Shader keine Ausgabetiefe auft.
> -   Wenn Sie Renderzielansichten gebunden haben ([**D3D11 \_ BIND \_ RENDER \_ TARGET**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)), und Sie die Anzahl der Stichproben auf größer als 1 erzwungen haben, stellen Sie sicher, dass jedes Renderziel nur ein einzelnes Beispiel hat.
> -   Betreiben Sie den Shader nicht mit der Stichprobenhäufigkeit. Daher gibt [**ID3D11ShaderReflection::IsSampleFrequencyShader**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader) **FALSE zurück.**
>
> Andernfalls ist das Renderingverhalten nicht definiert. Informationen zum Konfigurieren der Tiefen-Schablone finden Sie unter [Configuring Depth-Stencil Functionality](d3d10-graphics-programming-guide-depth-stencil.md)(Konfigurieren Depth-Stencil Funktionalität).

 

## <a name="process-video-resources-with-shaders"></a>Verarbeiten von Videoressourcen mit Shadern

Mit Direct3D 11.1 können Sie Ansichten (SRV/RTV/UAV) für Videoressourcen erstellen, damit Direct3D-Shader diese Videoressourcen verarbeiten können. Das Format einer zugrunde liegenden Videoressource schränkt die Formate ein, die die Ansicht verwenden kann. Die [**DXGI \_ FORMAT-Enumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enthält neue Videoressourcenformatwerte. Diese **DXGI \_ FORMAT-Werte** geben die gültigen Ansichtsformate an, die Sie erstellen können, und geben an, wie die Direct3D 11.1-Laufzeit die Ansicht zu ordnet. Sie können mehrere Ansichten verschiedener Teile derselben Oberfläche erstellen, und je nach Format können sich die Größen der Ansichten voneinander unterscheiden.

Direct3D 11.1 aktualisiert die folgenden Methoden für dieses Feature.

-   [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)
-   [**ID3D11Device::CreateRenderTargetView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview)
-   [**ID3D11Device::CreateUnorderedAccessView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview)

## <a name="extended-support-for-shared-texture2d-resources"></a>Erweiterte Unterstützung für freigegebene Texture2D-Ressourcen

Direct3D 11.1 garantiert, dass Sie texture2D-Ressourcen, die Sie erstellt haben, für bestimmte Ressourcentypen und Formate freigeben können. Verwenden Sie zum Freigeben von Texture2D-Ressourcen die [**Flags D3D11 \_ RESOURCE \_ MISC \_ SHARED,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) [**D3D11 \_ RESOURCE \_ MISC SHARED \_ \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)oder eine Kombination der FLAGs **D3D11 \_ RESOURCE \_ MISC SHARED \_ \_ KEYEDMUTEX** und [**D3D11 \_ RESOURCE \_ MISC SHARED \_ \_ NTHANDLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) (neu für Windows 8), wenn Sie diese Ressourcen erstellen.

Direct3D 11.1 garantiert, dass Sie texture2D-Ressourcen, die Sie erstellt haben, mit den [**folgenden DXGI \_ FORMAT-Werten teilen**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) können:

-   DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM
-   DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM
-   DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT

Darüber hinaus garantiert Direct3D 11.1, dass Sie Texture2D-Ressourcen, die Sie erstellt haben, mit einer Mipmap-Ebene von 1, arraygröße von 1, Bindungsflags von [**D3D11 \_ BIND \_ SHADER \_ RESOURCE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) und [**D3D11 \_ BIND RENDER \_ \_ TARGET**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) kombiniert, verwendungs default ([**D3D11 \_ USAGE \_ DEFAULT)**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)und nur diese [**D3D11 \_ RESOURCE \_ MISC \_ FLAG-Werte**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) freigeben können:

-   [**D3D11 \_ RESOURCE \_ MISC \_ SHARED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ RESOURCE \_ MISC \_ SHARED \_ KEYEDMUTEX**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ RESOURCE \_ MISC \_ SHARED \_ NTHANDLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ RESOURCE \_ MISC \_ GDI \_ COMPATIBLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

Mit Direct3D 11.1 können Sie eine größere Vielfalt von Texture2D-Ressourcentypen und -Formaten freigeben. Sie können abfragen, ob der Grafiktreiber und die Hardware die erweiterte Texture2D-Ressourcenfreigabe unterstützen, indem Sie [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) mit dem [**Wert D3D11 \_ FEATURE \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) aufrufen. Übergeben Sie in diesem **ID3D11Device::CheckFeatureSupport-Aufruf** einen Zeiger auf eine [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS-Struktur.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) **ID3D11Device::CheckFeatureSupport** legt das **ExtendedResourceSharing-Mitglied** von **D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS** auf **TRUE** fest, wenn die Hardware und der Treiber die erweiterte Texture2D-Ressourcenfreigabe unterstützen.

Wenn [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) **true** in **ExtendedResourceSharing** zurückgibt, können Sie ressourcen, die Sie erstellt haben, mit den folgenden [**DXGI \_ FORMAT-Werten**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) freigeben:

-   \_DXGI-FORMAT \_ R32G32B32A32 \_ TYPLOS
-   DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT
-   DXGI \_ FORMAT \_ R32G32B32A32 \_ UINT
-   DXGI \_ FORMAT \_ R32G32B32A32 \_ SINT
-   \_DXGI-FORMAT \_ R16G16B16A16 \_ TYPLOS
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ UINT
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM
-   DXGI \_ FORMAT \_ R16G16B16A16 \_ SINT
-   DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM
-   DXGI \_ FORMAT \_ R10G10B10A2 \_ UINT
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ TYPELESS
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ UINT
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM
-   DXGI \_ FORMAT \_ R8G8B8A8 \_ SINT
-   DXGI \_ FORMAT \_ B8G8R8A8 \_ TYPLOS
-   DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM
-   DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM
-   DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ B8G8R8X8 \_ TYPLOS
-   DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM \_ SRGB
-   DXGI \_ FORMAT \_ R32 \_ TYPELESS
-   DXGI \_ FORMAT \_ R32 \_ FLOAT
-   DXGI \_ FORMAT \_ R32 \_ UINT
-   DXGI \_ FORMAT \_ R32 \_ SINT
-   DXGI \_ FORMAT \_ R16 \_ TYPELESS
-   DXGI \_ FORMAT \_ R16 \_ FLOAT
-   DXGI \_ FORMAT \_ R16 \_ UNORM
-   DXGI \_ FORMAT \_ R16 \_ UINT
-   DXGI \_ FORMAT \_ R16 \_ SNORM
-   DXGI \_ FORMAT \_ R16 \_ SINT
-   DXGI \_ FORMAT \_ R8 \_ TYPELESS
-   DXGI \_ FORMAT \_ R8 \_ UNORM
-   DXGI \_ FORMAT \_ R8 \_ UINT
-   DXGI \_ FORMAT \_ R8 \_ SNORM
-   DXGI \_ FORMAT \_ R8 \_ SINT
-   DXGI \_ FORMAT \_ A8 \_ UNORM
-   DXGI \_ FORMAT \_ AYUV
-   \_DXGI-FORMAT \_ YUY2
-   DXGI \_ FORMAT \_ NV12
-   DXGI \_ FORMAT \_ NV11
-   DXGI \_ FORMAT \_ P016
-   DXGI \_ FORMAT \_ P010
-   \_DXGI-FORMAT \_ Y216
-   \_DXGI-FORMAT \_ Y210
-   \_DXGI-FORMAT \_ Y416
-   \_DXGI-FORMAT \_ Y410

Wenn [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) **true** in **ExtendedResourceSharing** zurückgibt, können Sie Ressourcen, die Sie erstellt haben, mit diesen Features und Flags freigeben:

-   [**D3D11 \_ – \_ NUTZUNGSEINSTELLUNG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)
-   [**D3D11 BIND \_ \_ \_ SHADER-RESSOURCE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ BIND \_ RENDER \_ TARGET**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ RESOURCE \_ MISC \_ GENERATE \_ MIPS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11: \_ \_ UNGEORDNETEN ZUGRIFF \_ BINDEN**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   Mipmap-Ebenen (mindestens eine Ebene) in den 2D-Texturressourcen (angegeben im **MipLevels-Member** von [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   Arrays von 2D-Texturressourcen (eine oder mehrere Texturen) (angegeben im **ArraySize-Member** von [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc))
-   [**\_D3D11-BINDUNGSDECODER \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ RESOURCE \_ MISC \_ RESTRICTED \_ CONTENT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ RESOURCE \_ MISC \_ RESTRICT \_ SHARED \_ RESOURCE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ RESOURCE \_ MISC \_ RESTRICT \_ SHARED \_ RESOURCE \_ DRIVER**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

> [!Note]  
> Wenn **ExtendedResourceSharing** **auf TRUE** festgelegt ist, haben Sie mehr Flexibilität, wenn Sie Bindungsflags für die Freigabe von Texture2D-Ressourcen angeben. Der Grafiktreiber und die Hardware unterstützen nicht nur mehr Bindungsflags, sondern auch weitere mögliche Kombinationen von Bindungsflags. Beispielsweise können Sie nur [**D3D11 \_ BIND RENDER \_ \_ TARGET**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) oder keine Bindungsflags angeben usw.

 

Auch wenn [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) **true** in **ExtendedResourceSharing** zurückgibt, können Sie die erstellten Ressourcen nicht mit diesen Features und Flags teilen:

-   [**D3D11 \_ BIND \_ DEPTH \_ STENCIL**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   2D-Texturressourcen im MSAA-Modus (Multisample Antialiasing) (angegeben mit [**DXGI \_ SAMPLE \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc))
-   [**D3D11-RESSOURCE– \_ \_ \_ MISC-RESSOURCEN-KLAMMER \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ USAGE \_ IMMUTABLE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), [**D3D11 \_ USAGE \_ DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)oder [**D3D11 USAGE STAGING (D3D11 USAGE STAGING) (D3D11 USAGE STAGING (D3D11 USAGE STAGING) (D3D11 USAGE STAGING (D3D11 USAGE \_ \_ STAGING) (D3D11 USAGE STAGING ( D3D11 USAGE DYNAMIC) (D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)
-   [**D3D11-RESSOURCE \_ \_ MISC \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="change-subresources-with-new-copy-options"></a>Ändern von Unterressourcen mit neuen Kopieroptionen

Mit Direct3D 11.1 können Sie neue Kopierflags zum Kopieren und Aktualisieren von Unterressourcen verwenden. Wenn Sie eine Unterressource kopieren, können die Quell- und Zielressourcen identisch sein, und die Quell- und Zielregionen können sich überschneiden.

Dieses Direct3D 11.1-Feature besteht aus der folgenden API.

-   [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)
-   [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)

## <a name="discard-resources-and-resource-views"></a>Verwerfen von Ressourcen und Ressourcenansichten

Mit Direct3D 11.1 können Sie Ressourcen und Ansichten von Ressourcen aus dem Gerätekontext verwerfen. Diese neue Funktion informiert die GPU darüber, dass vorhandene Inhalte in Ressourcen oder Ressourcenansichten nicht mehr benötigt werden.

Dieses Direct3D 11.1-Feature besteht aus der folgenden API.

-   [**ID3D11DeviceContext1::D iscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource)
-   [**ID3D11DeviceContext1::D iscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview)
-   [**ID3D11DeviceContext1::D iscardView1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview1)

## <a name="support-a-larger-number-of-uavs"></a>Unterstützung einer größeren Anzahl von UAVs

Mit Direct3D 11.1 können Sie eine größere Anzahl von UAVs verwenden, wenn Sie Ressourcen an die [Ausgabezusammenführungsphase](d3d10-graphics-programming-guide-output-merger-stage.md) binden und ein Array von Ansichten für eine ungeordnete Ressource festlegen.

Direct3D 11.1 aktualisiert die folgenden Methoden für dieses Feature.

-   [**ID3D11DeviceContext::OMSetRenderTargetsAndUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews)
-   [**ID3D11DeviceContext::CSSetUnorderedAccessViews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)

## <a name="bind-a-subrange-of-a-constant-buffer-to-a-shader"></a>Binden eines Unterbereichs eines konstanten Puffers an einen Shader

Mit Direct3D 11.1 können Sie einen Unterbereich eines konstanten Puffers binden, auf den ein Shader zugreifen kann. Sie können einen größeren konstanten Puffer angeben und den Unterbereich angeben, den der Shader verwenden kann.

Dieses Direct3D 11.1-Feature besteht aus der folgenden API.

-   [**ID3D11DeviceContext1::CSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1)

## <a name="retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader"></a>Abrufen des Unterbereichs eines konstanten Puffers, der an einen Shader gebunden ist

Mit Direct3D 11.1 können Sie den Unterbereich eines konstanten Puffers abrufen, der an einen Shader gebunden ist.

Dieses Direct3D 11.1-Feature besteht aus der folgenden API.

-   [**ID3D11DeviceContext1::CSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1)
-   [**ID3D11DeviceContext1::D SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::P SGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1)

## <a name="clear-all-or-part-of-a-resource-view"></a>Löschen einer Ressourcenansicht ganz oder teilweise

Mit Direct3D 11.1 können Sie eine Ressourcenansicht (RTV, UAV oder eine beliebige Videoansicht einer Texture2D-Oberfläche) löschen. Sie wenden den gleichen Farbwert auf alle Teile der Ansicht an.

Dieses Direct3D 11.1-Feature besteht aus der folgenden API.

-   [**ID3D11DeviceContext1::ClearView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)

## <a name="map-srvs-of-dynamic-buffers-with-no_overwrite"></a>Zuordnen von SRVs dynamischer Puffer ohne \_ OVERWRITE

Mit Direct3D 11.1 können Sie Shaderressourcenansichten (SRV) dynamischer Puffer mit D3D11 \_ MAP \_ WRITE NO \_ \_ OVERWRITE zuordnen. Die Direct3D 11- und früheren Runtimes beschränkten die Zuordnung zu Scheitelpunkt- oder Indexpuffern.

Direct3D 11.1 aktualisiert die [**ID3D11DeviceContext::Map-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) für dieses Feature.

## <a name="use-uavs-at-every-pipeline-stage"></a>Verwenden von UAVs in jeder Pipelinephase

Mit Direct3D 11.1 können Sie die folgenden Shadermodell 5.0-Anweisungen in allen Shaderstufen verwenden, die zuvor nur in Pixel-Shadern und Compute-Shadern verwendet wurden.

-   [dcl \_ uav \_ typed](/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-)
-   [dcl \_ uav \_ raw](/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-)
-   [dcl \_ uav \_ structured](/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-)
-   [ld \_ raw](/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-)
-   [ld \_ structured](/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-)
-   [ld \_ uav \_ typed](/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-)
-   [Rohdaten speichern \_](/windows/desktop/direct3dhlsl/store-raw--sm5---asm-)
-   [store \_ structured](/windows/desktop/direct3dhlsl/store-structured--sm5---asm-)
-   [store \_ uav \_ typed](/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-)
-   [\_sync uglobal](/windows/desktop/direct3dhlsl/sync--sm5---asm-)
-   Alle atomaren und unmittelbar atomaren (z. B. [atomic \_ und](/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-) und [imm \_ atomic \_ und](/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-))

Direct3D 11.1 aktualisiert die folgenden Methoden für dieses Feature.

-   [**ID3D11DeviceContext::CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**ID3D11DeviceContext::CreateGeometryShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**ID3D11DeviceContext::CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**ID3D11DeviceContext::CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**ID3D11DeviceContext::CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Diese Anweisungen waren in Direct3D 11.0 in ps \_ 5 \_ 0 und cs \_ 5 \_ 0 vorhanden. Da UaVs mit Direct3D 11.1 in allen Shaderstufen verfügbar sind, sind diese Anweisungen in allen Shaderstufen verfügbar.

Wenn Sie kompilierte Shader (VS/HS/DS/HS), die eine dieser Anweisungen verwenden, an eine Create-Shader-Funktion wie [**CreateVertexShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)übergeben, auf Geräten, die UAVs nicht in jeder Phase unterstützen (einschließlich vorhandener Treiber, die nicht mit diesem Feature implementiert werden), schlägt die Create-Shader-Funktion fehl. Die Create-Shader-Funktion schlägt auch fehl, wenn der Shader versucht, einen UAV-Slot zu verwenden, der über die von der Hardware unterstützten UAV-Slots hinausgeht.

Die UAVs, auf die in diesen Anweisungen verwiesen wird, werden für alle Pipelinephasen freigegeben. Beispielsweise ist ein UAV, der in der [Ausgabezusammenführungsphase](d3d10-graphics-programming-guide-output-merger-stage.md) an Slot 0 gebunden ist, in Slot 0 an VS/HS/DS/GS/PS verfügbar.

UAV-Zugriffe, die Sie innerhalb oder über Shaderstufen hinweg ausstellen, die innerhalb eines \* bestimmten Draw-Befehls () ausgeführt werden, oder die Sie über den Compute-Shader in einem Dispatch () ausstellen, \* werden nicht garantiert in der Reihenfolge abgeschlossen, in der Sie sie ausgestellt haben. Alle UAV-Zugriffe werden jedoch am Ende von Draw \* () oder Dispatch \* () abgeschlossen.

## <a name="extended-support-for-warp-devices"></a>Erweiterte Unterstützung für WARP-Geräte

Direct3D 11.1 erweitert die Unterstützung für [WARP-Geräte,](overviews-direct3d-11-devices-create-warp.md) die Sie erstellen, indem Sie [**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) im *DriverType-Parameter* von [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)übergeben.

Ab Direct3D 11.1 unterstützen WARP-Geräte:

-   Alle [Direct3D-Featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) von 9.1 bis 11.1
-   [Compute-Shader](direct3d-11-advanced-stages-compute-shader.md) und [Mosaik](direct3d-11-advanced-stages-tessellation.md)
-   Freigegebene Oberflächen. Das heißt, Sie können Oberflächen vollständig zwischen WARP-Geräten sowie zwischen WARP-Geräten in verschiedenen Prozessen freigeben.

WARP-Geräte unterstützen diese optionalen Features nicht:

-   [Doppelzimmer](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)
-   [Videocodierung oder -decodierung](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)
-   [Unterstützung von Shadern mit minimaler Genauigkeit](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)

Wenn Sie einen virtuellen Computer (VM), Hyper-V, mit deaktivierter Grafikverarbeitungseinheit (GPU) oder ohne Anzeigetreiber ausführen, erhalten Sie ein WARP-Gerät mit dem Anzeigenamen "Microsoft Basic Display Adapter". Dieses WARP-Gerät kann die gesamte Windows ausführen, einschließlich DWM-, Internet Explorer- und Windows Store-Apps. Dieses WARP-Gerät unterstützt auch die Ausführung von Legacy-Apps, die [DirectDraw](/windows/desktop/directdraw/directdraw) verwenden, oder von Apps, die Direct3D 3 bis Direct3D 11.1 verwenden.

## <a name="use-direct3d-in-session-0-processes"></a>Verwenden von Direct3D in Sitzung 0-Prozessen

Ab Windows 8 und Windows Server 2012 können Sie die meisten Direct3D-APIs in Sitzung 0-Prozessen verwenden.

> [!Note]  
> Diese Ausgabe-, Fenster-, Swapkette- und präsentationsbezogenen APIs sind in Sitzung 0-Prozessen nicht verfügbar, da sie nicht für die Sitzung 0-Umgebung gelten:
>
> -   [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)
> -   [**IDXGIFactory::GetWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-getwindowassociation)
> -   [**IDXGIFactory::MakeWindowAssociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation)
> -   [**IDXGIAdapter::EnumOutputs**](/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs)
> -   [**ID3D11Debug::SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)
> -   [**ID3D11Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay)
> -   [**ID3D11Debug::SetSwapChain**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setswapchain)
> -   [**ID3D10Debug::SetFeatureMask**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask)
> -   [**ID3D10Debug::SetPresentPerRenderOpDelay**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setpresentperrenderopdelay)
> -   [**ID3D10Debug::SetSwapChain**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setswapchain)
> -   [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdeviceandswapchain)
> -   [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)
> -   [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)
>
> Wenn Sie eine der oben genannten APIs in einem Sitzung 0-Prozess aufrufen, wird [**DXGI \_ ERROR NOT CURRENTLY AVAILABLE \_ \_ \_ zurückgegeben.**](/windows/desktop/direct3ddxgi/dxgi-error)

 

## <a name="support-for-shadow-buffer-on-feature-level-9"></a>Unterstützung für Schattenpuffer auf Featureebene 9

Verwenden Sie eine Teilmenge der Direct3D 10 0+-Schattenpufferfeatures, um Schatteneffekte auf Featureebene \_ 9 x zu [](overviews-direct3d-11-devices-downlevel-intro.md) \_ implementieren. Informationen dazu, was Sie tun müssen, um Schatteneffekte auf Featureebene 9 x zu implementieren, finden Sie unter Implementieren von Schattenpuffern für \_ [Direct3D-Funktionsebene 9.](/previous-versions/windows/apps/jj262110(v=win.10))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neues in Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 