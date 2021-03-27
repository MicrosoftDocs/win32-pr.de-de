---
title: Direct3D 11,1-Features
description: Die folgende Funktionalität wurde in Direct3D 11,1 hinzugefügt, die in Windows 8, Windows RT und Windows Server 2012 enthalten ist.
ms.assetid: 2203D2D2-ECF6-4753-90FA-12A52678DFBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dece9ed6e0a40ade28857277c344be0e9f2e7ce1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727496"
---
# <a name="direct3d-111-features"></a>Direct3D 11,1-Features

Die folgende Funktionalität wurde in Direct3D 11,1 hinzugefügt, die in Windows 8, Windows RT und Windows Server 2012 enthalten ist. Teil Unterstützung für [Direct3D 11,1](direct3d-11-features.md) ist unter Windows 7 und Windows Server 2008 R2 über das [Platt Form Update für Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7)verfügbar, das über das [Platt Form Update für Windows 7](https://support.microsoft.com/kb/2670838)verfügbar ist.

-   [Shader-Ablauf Verfolgung und Compilerverbesserungen](#shader-tracing-and-compiler-enhancements)
-   [Direct3D Geräte Freigabe](#direct3d-device-sharing)
-   [Überprüfen der Unterstützung von neuen Direct3D 11,1-Features und-Formaten](#check-support-of-new-direct3d-111-features-and-formats)
-   [Minimale Genauigkeit mit HLSL verwenden](#use-hlsl-minimum-precision)
-   [Angeben von Benutzer Clip Flächen in HLSL auf Featureebene 9 und höher](#specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Erstellen größerer konstanter Puffer, auf die ein Shader zugreifen kann](#create-larger-constant-buffers-than-a-shader-can-access)
-   [Verwenden von logischen Vorgängen in einem Renderziel](#use-logical-operations-in-a-render-target)
-   [Erzwingen der Stichproben Anzahl zum Erstellen eines Raster-Zustands](#force-the-sample-count-to-create-a-rasterizer-state)
-   [Verarbeiten von Video Ressourcen mit Shadern](#process-video-resources-with-shaders)
-   [Erweiterte Unterstützung für freigegebene Texture2D-Ressourcen](#extended-support-for-shared-texture2d-resources)
-   [Ändern von unter Berichten mit neuen Kopier Optionen](#change-subresources-with-new-copy-options)
-   [Verwerfen von Ressourcen und Ressourcen Ansichten](#discard-resources-and-resource-views)
-   [Unterstützung einer größeren Anzahl von UAVs](#support-a-larger-number-of-uavs)
-   [Binden eines unter Bereichs eines konstanten Puffers an einen Shader](#bind-a-subrange-of-a-constant-buffer-to-a-shader)
-   [Abrufen des unter Bereichs eines konstanten Puffers, der an einen Shader gebunden ist](#retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader)
-   [Alle oder Teile einer Ressourcen Ansicht löschen](#clear-all-or-part-of-a-resource-view)
-   [Zuordnen von Srvs dynamischer Puffer ohne über \_ schreiben](/windows)
-   [Verwenden von UAVs in jeder Pipeline Phase](#use-uavs-at-every-pipeline-stage)
-   [Erweiterte Unterstützung für Warp-Geräte](#extended-support-for-warp-devices)
-   [Verwenden von Direct3D in Sitzung 0-Prozessen](#use-direct3d-in-session-0-processes)
-   [Unterstützung für Schatten Puffer auf Featureebene 9](#support-for-shadow-buffer-on-feature-level-9)
-   [Zugehörige Themen](#related-topics)

## <a name="shader-tracing-and-compiler-enhancements"></a>Shader-Ablauf Verfolgung und Compilerverbesserungen

Mit Direct3D 11,1 können Sie die Shader-Ablauf Verfolgung verwenden, um sicherzustellen, dass Ihr Code wie beabsichtigt funktioniert. Falls nicht, können Sie das Problem ermitteln und beheben. Das Windows Software Development Kit (SDK) für Windows 8 enthält die HLSL-compilererweiterungen. Die Shader-Ablauf Verfolgung und der HLSL-Compiler werden in D3dcompiler \_nn.dll implementiert.

Die Shader-Ablaufverfolgungs-API und die Erweiterungen des HLSL-Compilers bestehen aus den folgenden Methoden und Funktionen.

-   [**ID3D11RefDefaultTrackingOptions:: settrackingoptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11refdefaulttrackingoptions-settrackingoptions)
-   [**ID3D11RefTrackingOptions:: settrackingoptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11reftrackingoptions-settrackingoptions)
-   [**ID3D11TracingDevice:: setshadertrackingoptions**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11TracingDevice:: setshadertrackingoptionsbytype**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11tracingdevice-setshadertrackingoptionsbytype)
-   [**ID3D11ShaderTraceFactory:: kreateshadertrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertracefactory-createshadertrace)
-   [**ID3D11ShaderTrace:: traceready**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-traceready)
-   [**ID3D11ShaderTrace:: resettrace**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-resettrace)
-   [**ID3D11ShaderTrace:: gettracestats**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-gettracestats)
-   [**ID3D11ShaderTrace::P sselectstamp**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-psselectstamp)
-   [**ID3D11ShaderTrace:: getinitialregistercontent**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getinitialregistercontents)
-   [**ID3D11ShaderTrace:: getstep**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getstep)
-   [**ID3D11ShaderTrace:: getschreittenregister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getwrittenregister)
-   [**ID3D11ShaderTrace:: getreadregister**](/windows/desktop/api/D3D11ShaderTracing/nf-d3d11shadertracing-id3d11shadertrace-getreadregister)
-   [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2)
-   [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)
-   [**D3DDisassemble11Trace**](/windows/desktop/direct3dhlsl/d3ddisassemble11trace)
-   [**D3DDisassembleRegion**](/windows/desktop/direct3dhlsl/d3ddisassembleregion)
-   [**D3DGetTraceInstructionOffsets**](/windows/desktop/direct3dhlsl/d3dgettraceinstructionoffsets)
-   [**D3DReadFileToBlob**](/windows/desktop/direct3dhlsl/d3dreadfiletoblob)
-   [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart)
-   [**D3DWriteBlobToFile**](/windows/desktop/direct3dhlsl/d3dwriteblobtofile)

Die D3dcompiler. lib-Bibliothek erfordert D3dcompiler- \_nn.dll. Diese dll ist nicht Bestandteil von Windows 8. Sie befindet sich im \\ Ordner "bin" des Windows SDK für Windows 8 zusammen mit der Befehlszeilenversion des HLSL-Compilers (Fxc.exe).

> [!Note]  
> Obwohl Sie diese Bibliothek und dll-Kombination für die Entwicklung verwenden können, können Sie keine Windows Store-Apps bereitstellen, die diese Kombination verwenden. Daher müssen Sie HLSL-Shader kompilieren, bevor Sie Ihre Windows Store-App senden. Sie können HLSL-Kompilierungs Binärdateien auf den Datenträger schreiben, oder der Compiler kann Header mit statischen Byte Arrays generieren, die die Shader-BLOB-Daten enthalten. Verwenden Sie die [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) -Schnittstelle für den Zugriff auf die BLOB-Daten. Um Ihre Windows Store-App zu entwickeln, nennen Sie [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2) oder [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile) , um die Rohdaten-HLSL-Quelle zu kompilieren, und laden Sie dann die resultierenden BLOB-Daten in Direct3D.

 

## <a name="direct3d-device-sharing"></a>Direct3D Geräte Freigabe

Direct3D 11,1 ermöglicht Direct3D 10-APIs und Direct3D 11-APIs die Verwendung eines zugrunde liegenden renderinggeräts.

Dieses Direct3D 11,1-Feature besteht aus den folgenden Methoden und der-Schnittstelle.

-   [**ID3D11Device1:: kreatedevicecontextstate**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createdevicecontextstate)
-   [**ID3D11DeviceContext1:: Swap-Gerätestatus**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-swapdevicecontextstate)
-   [**ID3DDeviceContextState**](/windows/win32/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate)

## <a name="check-support-of-new-direct3d-111-features-and-formats"></a>Überprüfen der Unterstützung von neuen Direct3D 11,1-Features und-Formaten

Mit Direct3D 11,1 können Sie nach neuen Funktionen suchen, die vom Grafiktreiber unterstützt werden, und auf neue Weise, dass ein Format auf einem Gerät unterstützt wird. Microsoft DirectX Graphics Infrastructure (DXGI) 1,2 gibt auch neue [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Werte an.

Dieses Direct3D 11,1-Feature besteht aus der folgenden API.

-   [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11 \_ Feature \_ Data \_ D3D11 \_ options**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), [**D3D11 \_ Feature \_ Data \_ Architecture \_ Info**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_architecture_info), [**D3D11 \_ Feature \_ Data \_ d3d9 \_ options**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_options), [**D3D11 \_ Feature \_ Data \_ Shader \_ Min \_ Precision \_ Support**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)und [**D3D11 \_ Feature \_ Data \_ d3d9 \_ Shadow \_ Support**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d9_shadow_support) Structures
-   [**ID3D11Device:: checkformatsupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) mit [**D3D11 \_ Format \_ Support \_ Decoder- \_ Ausgabe**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), D3D11-Format Unterstützung für [**\_ \_ \_ Video \_ Prozessor \_ Ausgabe**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**D3D11- \_ Formatunterstützung Video \_ \_ \_ Prozessor \_ Eingabe**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support), [**D3D11- \_ Format \_ Unterstützung \_ Video \_ Encoder**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support)und [**D3D11 \_ Format \_ SUPPORT2 Ausgabe der \_ \_ Fusions \_ Logik \_ op**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2)

## <a name="use-hlsl-minimum-precision"></a>Minimale Genauigkeit mit HLSL verwenden

Ab Windows 8 können Grafiktreiber minimale Genauigkeit der [HLSL-Skalardatentypen](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) implementieren, indem Sie eine beliebige Genauigkeit angeben, die größer oder gleich der angegebenen bitgenauigkeit ist. Wenn der HLSL-Shader-Code mit minimaler Genauigkeit auf Hardware verwendet wird, die die minimale Genauigkeit von HLSL implementiert, werden weniger Speicherbandbreite verwendet, und daher wird auch weniger Systemleistung verwendet.

Sie können die Unterstützung der minimalen Genauigkeit Abfragen, die der Grafiktreiber bietet, indem Sie [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) mit dem [**D3D11 \_ Feature- \_ Shader- \_ \_ \_ Unterstützungs**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) Wert für minimale Genauigkeit aufrufen. Übergeben Sie in diesem **ID3D11Device:: checkfeaturesupport** -Befehl einen Zeiger an eine [**D3D11- \_ Funktionsdaten- \_ \_ Shader- \_ \_ \_ Unterstützungs**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support) Struktur, die von **ID3D11Device:: checkfeaturesupport** mit den minimalen Genauigkeits Stufen gefüllt wird, die der Treiber für die Pixel-Shader-Stufe und für andere Shader-Stufen unterstützt. Die zurückgegebenen Informationen geben lediglich an, dass die Grafikhardware HLSL-Vorgänge mit geringerer Genauigkeit als die standardmäßige Gleit Komma Zahl mit 32 Bit ausführen kann, garantiert jedoch nicht, dass die Grafikhardware tatsächlich mit geringerer Genauigkeit ausgeführt wird.

Sie müssen nicht mehrere Shader erstellen, die die minimale Genauigkeit nicht verwenden. Erstellen Sie stattdessen Shader mit minimaler Genauigkeit, und die minimalen Genauigkeits Variablen verhalten sich bei vollständiger 32-Bit-Genauigkeit, wenn der Grafiktreiber meldet, dass keine minimale Genauigkeit unterstützt wird. Weitere Informationen zur minimalen Genauigkeit von HLSL finden [Sie unter Verwenden der minimalen Genauigkeit von HLSL](/windows/desktop/direct3dhlsl/using-hlsl-minimum-precision).

HLSL-Shader mit minimaler Genauigkeit können nicht für Betriebssysteme vor Windows 8 verwendet werden.

## <a name="specify-user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Angeben von Benutzer Clip Flächen in HLSL auf Featureebene 9 und höher

Ab Windows 8 können Sie das **clipplane** -Funktions Attribut in einer HLSL- [Funktionsdeklaration](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-syntax) anstelle von [SV \_ clipdistance](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) verwenden, damit Ihr Shader auf [Featureebene](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x und auf Featureebene 10 und höher funktioniert. Weitere Informationen finden Sie unter [User Clip Plane on Feature Level 9 Hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="create-larger-constant-buffers-than-a-shader-can-access"></a>Erstellen größerer konstanter Puffer, auf die ein Shader zugreifen kann

Mit Direct3D 11,1 können Sie Konstante Puffer erstellen, die größer sind als die maximale Konstante Puffergröße, auf die ein Shader zugreifen kann (4096 32-Bit \* 4-Component Konstanten – 64 KB). Wenn Sie später die Puffer an die Pipeline binden (z. b. über [**pssetconstantbuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetconstantbuffers) oder [**PSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)), können Sie einen Pufferbereich angeben, auf den der Shader zugreifen kann, der innerhalb des 4096-Limits passt.

Direct3D 11,1 aktualisiert die [**ID3D11Device::**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) up-Buffer-Methode für dieses Feature.

## <a name="use-logical-operations-in-a-render-target"></a>Verwenden von logischen Vorgängen in einem Renderziel

Mit Direct3D 11,1 können Sie logische Operationen anstelle eines Mischungs Ziels verwenden. Es ist jedoch nicht möglich, Logikoperationen mit der Mischung über mehrere Renderziele zu kombinieren.

Dieses Direct3D 11,1-Feature besteht aus der folgenden API.

-   [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1) mit [ **D3D11 \_ Logic \_ op**](/windows/desktop/api/D3D11_1/ne-d3d11_1-d3d11_logic_op)

## <a name="force-the-sample-count-to-create-a-rasterizer-state"></a>Erzwingen der Stichproben Anzahl zum Erstellen eines Raster-Zustands

Mit Direct3D 11,1 können Sie eine Anzahl von Erzwingungs Beispielen angeben, wenn Sie einen Status des Rasterizers erstellen.

Dieses Direct3D 11,1-Feature besteht aus der folgenden API.

-   [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1)

> [!Note]  
>
> Wenn Sie mit der Anzahl der Stichproben, die auf 1 oder höher erzwungen werden soll
>
> -   Binden Sie keine tiefen Schablonen Ansichten.
> -   Deaktivieren Sie die tiefen Tests.
> -   Stellen Sie sicher, dass der Shader keine tiefe ausgibt.
> -   Wenn Sie über renderzielsichten verfügen ([**D3D11 \_ Bind- \_ \_ Renderziel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)), und Sie die Anzahl der Stichproben auf einen Wert größer als 1 erzwingen, stellen Sie sicher, dass jedes Renderziel nur über ein einzelnes Beispiel verfügt.
> -   Betreiben Sie den Shader nicht bei der Stichproben Häufigkeit. Daher gibt [**ID3D11ShaderReflection:: issamplefrequencyshader**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11shaderreflection-issamplefrequencyshader) den Wert **false** zurück.
>
> Andernfalls ist das Renderingverhalten nicht definiert. Informationen zum Konfigurieren der tiefen Schablone finden Sie unter [Konfigurieren von Depth-Stencil Funktionen](d3d10-graphics-programming-guide-depth-stencil.md).

 

## <a name="process-video-resources-with-shaders"></a>Verarbeiten von Video Ressourcen mit Shadern

Direct3D 11,1 ermöglicht Ihnen das Erstellen von Sichten (SRV/RTV/UAV) für Video Ressourcen, sodass Direct3D-Shader diese Video Ressourcen verarbeiten können. Das Format einer zugrunde liegenden Video Ressource schränkt die Formate ein, die von der Ansicht verwendet werden können. Die [**DXGI- \_ formatenumeration**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) enthält neue Format Werte für Video Ressourcen. Diese **DXGI- \_ Format** Werte geben die gültigen Sicht Formate an, die Sie erstellen können, und wie die Direct3D 11,1-Runtime die Ansicht zuordnet. Sie können mehrere Ansichten verschiedener Teile derselben Oberfläche erstellen, und je nach Format können sich die Größen der Ansichten voneinander unterscheiden.

Direct3D 11,1 aktualisiert die folgenden Methoden für dieses Feature.

-   [**ID3D11Device:: kreateshaderresourceview**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview)
-   [**ID3D11Device:: kreaterendertargetview**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview)
-   [**ID3D11Device:: kreateunorderedaccessview**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createunorderedaccessview)

## <a name="extended-support-for-shared-texture2d-resources"></a>Erweiterte Unterstützung für freigegebene Texture2D-Ressourcen

Direct3D 11,1 garantiert, dass Sie Texture2D-Ressourcen freigeben können, die Sie mit bestimmten Ressourcentypen und Formaten erstellt haben. Verwenden Sie zum Freigeben von Texture2D-Ressourcen die [**D3D11- \_ Ressource \_ misc \_ Shared**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag), [**D3D11 \_ Resource \_ misc \_ Shared \_ keyedmutex**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)oder eine Kombination der **D3D11 \_ Resource \_ misc \_ Shared \_ keyedmutex** und [**D3D11 \_ Resource \_ misc Shared \_ \_ nthandle**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) (New for Windows 8) Flags, wenn Sie diese Ressourcen erstellen.

Direct3D 11,1 garantiert, dass Sie Texture2D-Ressourcen freigeben können, die Sie mit diesen [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Werten erstellt haben:

-   DXGI- \_ Format \_ R8G8B8A8 \_ unorm
-   DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB
-   DXGI- \_ Format \_ B8G8R8A8 \_ unorm
-   DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB
-   DXGI- \_ Format \_ B8G8R8X8 \_ unorm
-   DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB
-   DXGI- \_ Format \_ R10G10B10A2 \_ unorm
-   DXGI- \_ Format \_ R16G16B16A16 \_ float

Außerdem gewährleistet Direct3D 11,1, dass Sie Texture2D-Ressourcen freigeben können, die Sie mit einer MipMap-Ebene von 1, der Array Größe 1, den Bindungsflags von [**D3D11 \_ Bind- \_ Shader- \_ Ressource**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) und [**D3D11 \_ Bind- \_ \_ Renderziel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) ([**D3D11 \_ Usage \_ default**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)) und nur diesen [**D3D11 \_ Resource \_ misc- \_ Flagwerten**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) erstellt haben:

-   [**D3D11 \_ \_ ressourcenmisc frei \_ gegeben**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ \_ ressourcenmisc \_ Shared \_ keyedmutex**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ \_ ressourcenmisc \_ Shared \_ nthandle**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ \_ ressourcenmisc- \_ GDI- \_ kompatibel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

Mit Direct3D 11,1 können Sie eine größere Vielfalt von Texture2D-Ressourcentypen und-Formaten gemeinsam nutzen. Sie können Abfragen, ob der Grafiktreiber und die Hardware erweiterte Texture2D-Ressourcen Freigabe unterstützen, indem Sie [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) mit dem [**D3D11 \_ Feature \_ D3D11 \_ options**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature) -Wert aufrufen. Übergeben Sie in diesem **ID3D11Device:: checkfeaturesupport** -Befehl einen Zeiger an eine [**D3D11 \_ Feature \_ Data \_ D3D11 \_ options**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) -Struktur. **ID3D11Device:: checkfeaturesupport** legt das **extendedresourceshareing** -Mitglied von **D3D11 \_ Feature \_ Data D3D11- \_ \_ Optionen** auf **true** fest, wenn die Hardware und der Treiber erweiterte Texture2D-Ressourcen Freigabe unterstützen.

Wenn [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) " **true** " in " **extendedresourceshareing**" zurückgibt, können Sie Ressourcen, die Sie erstellt haben, mit den folgenden [**DXGI- \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Werten freigeben:

-   DXGI- \_ Format \_ R32G32B32A32 \_ typlose
-   DXGI- \_ Format \_ R32G32B32A32 \_ float
-   DXGI- \_ Format \_ R32G32B32A32 \_ uint
-   DXGI- \_ Format \_ R32G32B32A32 \_ Sint
-   DXGI- \_ Format \_ R16G16B16A16 \_ typlose
-   DXGI- \_ Format \_ R16G16B16A16 \_ float
-   DXGI- \_ Format \_ R16G16B16A16 \_ unorm
-   DXGI- \_ Format \_ R16G16B16A16 \_ uint
-   DXGI- \_ Format \_ R16G16B16A16 \_ snorm
-   DXGI- \_ Format \_ R16G16B16A16 \_ Sint
-   DXGI- \_ Format \_ R10G10B10A2 \_ unorm
-   DXGI- \_ Format \_ R10G10B10A2 \_ uint
-   DXGI- \_ Format \_ R8G8B8A8 \_ typlose
-   DXGI- \_ Format \_ R8G8B8A8 \_ unorm
-   DXGI- \_ Format \_ R8G8B8A8 \_ unorm \_ sRGB
-   DXGI- \_ Format \_ R8G8B8A8 \_ uint
-   DXGI- \_ Format \_ R8G8B8A8 \_ snorm
-   DXGI- \_ Format \_ R8G8B8A8 \_ Sint
-   DXGI- \_ Format \_ B8G8R8A8 \_ typlose
-   DXGI- \_ Format \_ B8G8R8A8 \_ unorm
-   DXGI- \_ Format \_ B8G8R8X8 \_ unorm
-   DXGI- \_ Format \_ B8G8R8A8 \_ unorm \_ sRGB
-   DXGI- \_ Format \_ B8G8R8X8 \_ typlose
-   DXGI- \_ Format \_ B8G8R8X8 \_ unorm \_ sRGB
-   DXGI- \_ Format \_ R32 \_ typlos
-   DXGI- \_ Format \_ R32 \_ float
-   DXGI- \_ Format \_ R32 \_ uint
-   DXGI- \_ Format \_ R32 \_ Sint
-   DXGI- \_ Format \_ R16 \_ typlose
-   DXGI- \_ Format \_ R16 \_ float
-   DXGI- \_ Format \_ R16 \_ unorm
-   DXGI- \_ Format \_ R16 \_ uint
-   DXGI- \_ Format, \_ R16 \_ snorm
-   DXGI- \_ Format, \_ R16 \_ Sint
-   DXGI- \_ Format \_ R8 \_ typlos
-   DXGI- \_ Format \_ R8 \_ unorm
-   DXGI- \_ Format \_ R8 \_ uint
-   DXGI- \_ Format \_ R8 \_ snorm
-   DXGI- \_ Format \_ R8 \_ Sint
-   DXGI- \_ Format \_ a8 \_ unorm
-   DXGI- \_ Format \_ ayuv
-   DXGI- \_ Format \_ im YUY2
-   DXGI- \_ Format \_ NV12
-   DXGI- \_ Format \_ NV11
-   DXGI- \_ Format \_ P016
-   DXGI- \_ Format \_ P010
-   DXGI- \_ Format \_ Y216
-   DXGI- \_ Format \_ Y210
-   DXGI- \_ Format \_ Y416
-   DXGI- \_ Format \_ Y410

Wenn [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) in **extendedresourceshareing** den Wert **true** zurückgibt, können Sie Ressourcen, die Sie mit diesen Features und Flags erstellt haben, freigeben:

-   [**D3D11 \_ Verwendungs \_ Standard**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)
-   [**D3D11 \_ Bind- \_ Shader- \_ Ressource**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ Bind \_ - \_ Renderziel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ \_ ressourcenmisc \_ Generieren von \_ mips**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ Binden des \_ ungeordneten \_ Zugriffs**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   MipMap-Ebenen (eine oder mehrere Ebenen) in den 2D-Textur Ressourcen (angegeben im **miplevels** -Member von [**D3D11 \_ TEXTURE2D \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)Debug)
-   Arrays von 2D-Textur Ressourcen (eine oder mehrere Texturen) (angegeben im **arraySize** -Member [**von \_ D3D11 \_ TEXTURE2D**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)Debug)
-   [**D3D11 \_ Bind- \_ Decoder**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   [**D3D11 \_ Ressourcen mit \_ \_ eingeschränktem \_ Inhalt**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ \_ ressourcenmisc schränkt die frei \_ \_ gegebene \_ Ressource ein.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ Resource \_ misc \_ schränkt den frei \_ gegebenen \_ Ressourcen \_ Treiber ein.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

> [!Note]  
> Wenn **extendedresourceshareing** den Wert **true** hat, haben Sie mehr Flexibilität, wenn Sie Bindungsflags für die Freigabe von Texture2D-Ressourcen angeben. Der Grafiktreiber und die Hardware unterstützen nicht nur mehr Bindungsflags, sondern auch mehr mögliche Kombinationen von Bindungsflags. Sie können z. b. nur [**D3D11 \_ Bind \_ - \_ Renderziel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) oder keine Bindungsflags usw. angeben.

 

Auch wenn [**ID3D11Device:: checkfeaturesupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) in **extendedresourceshareing**" **true** " zurückgibt, können Sie die Ressourcen, die Sie mit diesen Features und Flags erstellt haben, trotzdem nicht freigeben:

-   [**D3D11 \_ Bind- \_ tiefen \_ Schablone**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag)
-   2D-Textur Ressourcen im Multisampling Antialiasing (MSAA)-Modus (angegeben mit [**DXGI \_ Sample \_ DESC**](/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_sample_desc))
-   [**D3D11 \_ \_ ressourcenmisc- \_ Ressourcen \_ Klammer**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)
-   [**D3D11 \_ Verwendung \_ unveränderlich**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), [**D3D11 \_ use \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)oder [**D3D11 \_ Usage \_ Staging**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) (d. h. mappable)
-   [**D3D11 \_ \_ ressourcenmisc \_ texturecube**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="change-subresources-with-new-copy-options"></a>Ändern von unter Berichten mit neuen Kopier Optionen

Direct3D 11,1 ermöglicht die Verwendung neuer kopierflags zum Kopieren und Aktualisieren von unter Ressourcen. Wenn Sie einen unter Bericht kopieren, können Quell-und Ziel Ressourcen identisch sein, und die Quell-und Zielregionen können sich überlappen.

Dieses Direct3D 11,1-Feature besteht aus der folgenden API.

-   [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1)
-   [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)

## <a name="discard-resources-and-resource-views"></a>Verwerfen von Ressourcen und Ressourcen Ansichten

Mit Direct3D 11,1 können Sie Ressourcen und Sichten von Ressourcen aus dem Gerätekontext verwerfen. Mit dieser neuen Funktion wird die GPU informiert, dass vorhandene Inhalte in Ressourcen oder Ressourcen Sichten nicht mehr benötigt werden.

Dieses Direct3D 11,1-Feature besteht aus der folgenden API.

-   [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource)
-   [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview)
-   [**ID3D11DeviceContext1::D iscardview1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview1)

## <a name="support-a-larger-number-of-uavs"></a>Unterstützung einer größeren Anzahl von UAVs

Mit Direct3D 11,1 können Sie eine größere Anzahl von UAVs verwenden, wenn Sie Ressourcen an die [Ausgabe-Fusion-Phase](d3d10-graphics-programming-guide-output-merger-stage.md) binden und ein Array von Sichten für eine ungeordnete Ressource festlegen.

Direct3D 11,1 aktualisiert die folgenden Methoden für dieses Feature.

-   [**Verknüpfung id3d11devicecontext aus:: omabtrendertargesorandunorderedaccessviews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargetsandunorderedaccessviews)
-   [**Verknüpfung id3d11devicecontext aus:: cssetunorderedaccessviews**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-cssetunorderedaccessviews)

## <a name="bind-a-subrange-of-a-constant-buffer-to-a-shader"></a>Binden eines unter Bereichs eines konstanten Puffers an einen Shader

Mit Direct3D 11,1 können Sie einen Unterbereich eines konstanten Puffers binden, auf den ein Shader zugreifen kann. Sie können einen größeren Konstanten Puffer bereitstellen und den Unterbereich angeben, der vom Shader verwendet werden kann.

Dieses Direct3D 11,1-Feature besteht aus der folgenden API.

-   [**ID3D11DeviceContext1::CSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-cssetconstantbuffers1)
-   [**ID3D11DeviceContext1::D ssetconstantbuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gssetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hssetconstantbuffers1)
-   [**ID3D11DeviceContext1::P ssetconstantbuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSSetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vssetconstantbuffers1)

## <a name="retrieve-the-subrange-of-a-constant-buffer-that-is-bound-to-a-shader"></a>Abrufen des unter Bereichs eines konstanten Puffers, der an einen Shader gebunden ist

Mit Direct3D 11,1 können Sie die Unterbereiche eines konstanten Puffers abrufen, der an einen Shader gebunden ist.

Dieses Direct3D 11,1-Feature besteht aus der folgenden API.

-   [**ID3D11DeviceContext1::CSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-csgetconstantbuffers1)
-   [**ID3D11DeviceContext1::D sgetconstantbuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-dsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::GSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-gsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::HSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-hsgetconstantbuffers1)
-   [**ID3D11DeviceContext1::P sgetconstantbuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-psgetconstantbuffers1)
-   [**ID3D11DeviceContext1::VSGetConstantBuffers1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-vsgetconstantbuffers1)

## <a name="clear-all-or-part-of-a-resource-view"></a>Alle oder Teile einer Ressourcen Ansicht löschen

Mit Direct3D 11,1 können Sie eine Ressourcen Ansicht (RTV, UAV oder eine beliebige Videoansicht einer Texture2D-Oberfläche) löschen. Sie wenden denselben Farbwert auf alle Teile der Ansicht an.

Dieses Direct3D 11,1-Feature besteht aus der folgenden API.

-   [**ID3D11DeviceContext1:: Clearview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-clearview)

## <a name="map-srvs-of-dynamic-buffers-with-no_overwrite"></a>Zuordnen von Srvs dynamischer Puffer ohne über \_ schreiben

Mit Direct3D 11,1 können Sie Shader-Ressourcen Sichten (SRV) dynamischer Puffer mit D3D11 \_ map \_ Write \_ No überschreiben zuordnen \_ . Bei den Laufzeiten Direct3D 11 und früher wurde die Zuordnung auf Scheitelpunkt-oder Index Puffer beschränkt.

Direct3D 11,1 aktualisiert die [**Verknüpfung id3d11devicecontext aus:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) -Methode für dieses Feature.

## <a name="use-uavs-at-every-pipeline-stage"></a>Verwenden von UAVs in jeder Pipeline Phase

Mit Direct3D 11,1 können Sie die folgenden Shadermodell-5,0-Anweisungen für alle shaderphasen verwenden, die zuvor in nur Pixel-Shader und Compute-Shadern verwendet wurden.

-   [DCL- \_ UAV- \_ typisiert](/windows/desktop/direct3dhlsl/dcl-uav-typed--sm5---asm-)
-   [DCL- \_ UAV- \_ Rohdaten](/windows/desktop/direct3dhlsl/dcl-uav-raw--sm5---asm-)
-   [DCL- \_ UAV \_ strukturiert](/windows/desktop/direct3dhlsl/dcl-uav-structured--sm5---asm-)
-   [LD \_ Rohdaten](/windows/desktop/direct3dhlsl/ld-raw--sm5---asm-)
-   [LD \_ strukturiert](/windows/desktop/direct3dhlsl/ld-structured--sm5---asm-)
-   [LD \_ UAV- \_ typisiert](/windows/desktop/direct3dhlsl/ld-uav-typed--sm5---asm-)
-   [\_Rohdaten speichern](/windows/desktop/direct3dhlsl/store-raw--sm5---asm-)
-   [\_strukturierte Speicherung](/windows/desktop/direct3dhlsl/store-structured--sm5---asm-)
-   [Speicher- \_ UAV- \_ typisiert](/windows/desktop/direct3dhlsl/store-uav-typed--sm5---asm-)
-   [Synchronisieren von \_ uglobal](/windows/desktop/direct3dhlsl/sync--sm5---asm-)
-   Alle Atomics und unmittelbaren Atomics (z. b. [Atomic \_ und](/windows/desktop/direct3dhlsl/atomic-and--sm5---asm-) und [imm \_ Atomic \_ und](/windows/desktop/direct3dhlsl/imm-atomic-and--sm5---asm-))

Direct3D 11,1 aktualisiert die folgenden Methoden für dieses Feature.

-   [**Verknüpfung id3d11devicecontext aus:: kreatedomainshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader)
-   [**Verknüpfung id3d11devicecontext aus:: kreategeometryshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshader)
-   [**Verknüpfung id3d11devicecontext aus:: kreategeometryshaderwithstreamoutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput)
-   [**Verknüpfung id3d11devicecontext aus:: kreatehullshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader)
-   [**Verknüpfung id3d11devicecontext aus:: kreatevertexshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)

Diese Anweisungen waren in Direct3D 11,0 in PS \_ 5 \_ 0 und CS \_ 5 \_ 0 vorhanden. Da Direct3D 11,1 UAVs in allen shaderphasen verfügbar macht, sind diese Anweisungen in allen shaderphasen verfügbar.

Wenn Sie kompilierte Shader (vs/HS/DS/HS) übergeben, die eine dieser Anweisungen in einer CREATE-Shader-Funktion verwenden, wie z. b. " [**kreatevertexshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createvertexshader)", kann die CREATE-Shader-Funktion nicht ausgeführt werden. Die Funktion "Create-Shader" schlägt auch fehl, wenn der Shader versucht, einen UAV-Slot zu verwenden, der über die von der Hardware unterstützten UAV-Slots hinausgeht.

Die UAVs, auf die durch diese Anweisungen verwiesen wird, sind für alle Pipeline stufenfrei gegeben. Beispielsweise ist eine UAV, die an Slot 0 an der [Ausgabe-Fusion-Phase](d3d10-graphics-programming-guide-output-merger-stage.md) gebunden ist, am Slot 0 bis vs/HS/DS/GS/PS verfügbar.

Der UAV-Zugriff, den Sie aus oder über Shader-Stufen ausgeben, die innerhalb eines bestimmten Draw \* () ausgeführt werden oder die Sie aus dem Compute-Shader innerhalb einer Dispatch () ausgeben, wird \* nicht garantiert in der Reihenfolge abgeschlossen, in der Sie sie ausgestellt haben. Allerdings werden alle UAV-Zugriffe am Ende des Draw \* () oder Dispatch \* () abgeschlossen.

## <a name="extended-support-for-warp-devices"></a>Erweiterte Unterstützung für Warp-Geräte

Direct3D 11,1 erweitert die Unterstützung von [Warp](overviews-direct3d-11-devices-create-warp.md) -Geräten, die Sie erstellen, indem Sie [**D3D \_ Driver \_ Type \_ Warp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) in den *DriverType* -Parameter von [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)übergibt.

Ab Direct3D 11,1-Warp-Geräte Unterstützung:

-   Alle Direct3D [featureebenen](overviews-direct3d-11-devices-downlevel-intro.md) zwischen 9,1 und 11,1
-   [Compute-Shader](direct3d-11-advanced-stages-compute-shader.md) und Mosaik [](direct3d-11-advanced-stages-tessellation.md)
-   Freigegebene Oberflächen. Das heißt, Sie können die Oberflächen zwischen den Warp-Geräten und zwischen den Warp-Geräten in verschiedenen Prozessen vollständig freigeben.

Folgende optionale Features werden von Warp-Geräten nicht unterstützt:

-   [Doppel](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles)
-   [Codieren oder Decodieren von Videos](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)
-   [Unterstützung der Unterstützung für minimale Genauigkeit](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_shader_min_precision_support)

Wenn Sie einen virtuellen Computer (Virtual Machine, VM), Hyper-V mit deaktivierter GPU (Graphics Processing Unit) oder ohne Anzeigetreiber ausführen, erhalten Sie ein Warp-Gerät, dessen Anzeige Name "Microsoft Basic Display Adapter" lautet. Dieses Warp-Gerät kann die vollständige Windows-Darstellung ausführen, einschließlich dwm, Internet Explorer und Windows Store-Apps. Dieses Warp-Gerät unterstützt auch das Ausführen von Legacy-apps, die [DirectDraw](/windows/desktop/directdraw/directdraw) verwenden, oder das Ausführen von apps mit Direct3D 3 bis Direct3D 11,1.

## <a name="use-direct3d-in-session-0-processes"></a>Verwenden von Direct3D in Sitzung 0-Prozessen

Ab Windows 8 und Windows Server 2012 können Sie die meisten der Direct3D-APIs in Sitzung 0-Prozessen verwenden.

> [!Note]  
> Diese Ausgabe-, Fenster-, SwapChain-und Präsentations bezogenen APIs sind in Sitzung 0-Prozessen nicht verfügbar, da Sie nicht auf die Umgebung der Sitzung 0 zutreffen:
>
> -   [**Idxgifactory:: kreateswapchain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)
> -   [**Idxgifactory:: getwindowassociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-getwindowassociation)
> -   [**Idxgifactory:: makewindowassociation**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-makewindowassociation)
> -   [**Idxgiadapter:: EnumOutputs**](/windows/desktop/api/dxgi/nf-dxgi-idxgiadapter-enumoutputs)
> -   [**ID3D11Debug:: setfeaturemask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)
> -   [**ID3D11Debug:: setpresentperrenderopdelay**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay)
> -   [**ID3D11Debug:: menwapchain**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setswapchain)
> -   [**ID3D10Debug:: setfeaturemask**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask)
> -   [**ID3D10Debug:: setpresentperrenderopdelay**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setpresentperrenderopdelay)
> -   [**ID3D10Debug:: menwapchain**](/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setswapchain)
> -   [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdeviceandswapchain)
> -   [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdeviceandswapchain1)
> -   [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)
>
> Wenn Sie eine der vorangehenden APIs in einem Session 0-Prozess aufzurufen, wird der DXGI-Fehler zurückgegeben, der [**\_ \_ \_ zurzeit nicht \_ verfügbar**](/windows/desktop/direct3ddxgi/dxgi-error)ist.

 

## <a name="support-for-shadow-buffer-on-feature-level-9"></a>Unterstützung für Schatten Puffer auf Featureebene 9

Verwenden Sie eine Teilmenge der Funktionen Direct3D 10 \_ 0 und Schatten Puffer, um Schatteneffekte auf Featureebene 9 x zu implementieren [](overviews-direct3d-11-devices-downlevel-intro.md) \_ . Informationen dazu, was Sie tun müssen, um Schatteneffekte auf Featureebene 9 \_ x zu implementieren, finden Sie unter [Implementieren von Schatten Puffern für Direct3D Feature Level 9](/previous-versions/windows/apps/jj262110(v=win.10)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neuerungen in Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 