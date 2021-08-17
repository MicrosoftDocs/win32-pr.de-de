---
title: Direct3D 11.2-Features
description: Die folgenden Funktionen wurden in Direct3D 11.2 hinzugefügt, das in Windows 8.1, Windows RT 8.1 und Windows Server 2012 R2 enthalten ist.
ms.assetid: 2A2D9BBB-F53A-4187-A25B-F4E58C896EE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cd253cf618b3915c4f303691cab86a11cc9268061d536892c0ff5ccf4fffe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124545"
---
# <a name="direct3d-112-features"></a>Direct3D 11.2-Features

Die folgenden Funktionen wurden in Direct3D 11.2 hinzugefügt, das in Windows 8.1, Windows RT 8.1 und Windows Server 2012 R2 enthalten ist.

-   [Gekachelte Ressourcen](#tiled-resources)
    -   [Überprüfen der Unterstützung von gekachelten Ressourcen](#check-tiled-resources-support)
-   [Erweiterte Unterstützung für WARP-Geräte](#extended-support-for-warp-devices)
-   [Kommentieren von Grafikbefehlen](#annotate-graphics-commands)
-   [HLSL-Shaderverknüpfung](#hlsl-shader-linking)
    -   [Funktionsverknüpfungsdiagramm (FLG)](#function-linking-graph-flg)
-   [HLSL-Posteingangscompiler](#inbox-hlsl-compiler)
-   [Zugehörige Themen](#related-topics)

## <a name="tiled-resources"></a>Gekachelte Ressourcen

Mit Direct3D 11.2 können Sie gekachelte Ressourcen erstellen, die als große logische Ressourcen mit geringer Menge an physischem Speicher bezeichnet werden können. Gekachelte Ressourcen sind (z.B.) mit Gelände in Spielen und App-Benutzeroberfläche nützlich.

Gekachelte Ressourcen werden erstellt, indem das [**FLAG D3D11 \_ RESOURCE \_ MISC \_ TILED angegeben**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) wird. Verwenden Sie diese API, um mit einer gekachelten Ressource zu arbeiten:

-   [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)
-   [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)
-   [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)
-   [**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings)
-   [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)
-   **D3D11 \_ DEBUG \_ FEATURE \_ DISABLE \_ TILED RESOURCE MAPPING TRACKING \_ AND VALIDATION \_ \_ \_ \_ flag** with [ **ID3D11Debug::SetFeatureMask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)

Weitere Informationen zu gekachelten Ressourcen finden Sie unter [Gekachelte Ressourcen.](tiled-resources.md)

### <a name="check-tiled-resources-support"></a>Überprüfen der Unterstützung von gekachelten Ressourcen

Bevor Sie gekachelte Ressourcen verwenden, müssen Sie herausfinden, ob das Gerät gekachelte Ressourcen unterstützt. So überprüfen Sie die Unterstützung für gekachelte Ressourcen:


```C++
HRESULT hr = D3D11CreateDevice(
    nullptr,                    // Specify nullptr to use the default adapter.
    D3D_DRIVER_TYPE_HARDWARE,   // Create a device using the hardware graphics driver.
    0,                          // Should be 0 unless the driver is D3D_DRIVER_TYPE_SOFTWARE.
    creationFlags,              // Set debug and Direct2D compatibility flags.
    featureLevels,              // List of feature levels this app can support.
    ARRAYSIZE(featureLevels),   // Size of the list above.
    D3D11_SDK_VERSION,          // Always set this to D3D11_SDK_VERSION for Windows Store apps.
    &device,                    // Returns the Direct3D device created.
    &m_d3dFeatureLevel,         // Returns feature level of device created.
    &context                    // Returns the device immediate context.
    );

if (SUCCEEDED(hr))
{
    D3D11_FEATURE_DATA_D3D11_OPTIONS1 featureData;
    DX::ThrowIfFailed(
        device->CheckFeatureSupport(D3D11_FEATURE_D3D11_OPTIONS1, &featureData, sizeof(featureData))
        );

    m_tiledResourcesTier = featureData.TiledResourcesTier;
}
```



## <a name="extended-support-for-warp-devices"></a>Erweiterte Unterstützung für WARP-Geräte

Direct3D 11.2 erweitert die Unterstützung für [WARP-Geräte,](overviews-direct3d-11-devices-create-warp.md) die Sie erstellen, indem Sie [**D3D \_ DRIVER TYPE \_ \_ WARP**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) im *DriverType-Parameter* von [**D3D11CreateDevice übergeben.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) Der WARP-Softwarerenderer in Direct3D 11.2 [](overviews-direct3d-11-devices-downlevel-intro.md) fügt vollständige Unterstützung für Direct3D-Featureebene 11 1 hinzu, einschließlich gekachelter \_ Ressourcen, [**IDXGIDevice3::Trim,**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim)freigegebener BCn-Oberflächen, Minblend und [](#tiled-resources)Karten-Standard. [Die](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) doppelte Unterstützung in HLSL-Shadern wurde ebenfalls zusammen mit der Unterstützung für die 16-fache MSAA aktiviert.

## <a name="annotate-graphics-commands"></a>Kommentieren von Grafikbefehlen

Mit Direct3D 11.2 können Sie Grafikbefehle mit dieser API kommentieren:

-   [**ID3D11DeviceContext2::IsAnnotationEnabled**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled)
-   [**ID3D11DeviceContext2::BeginEventInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint)
-   [**ID3D11DeviceContext2::SetMarkerInt**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint)
-   [**ID3D11DeviceContext2::EndEvent**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent)

## <a name="hlsl-shader-linking"></a>HLSL-Shaderverknüpfung

Windows 8.1 fügt separate Kompilierung und Verknüpfung von HLSL-Shadern hinzu, wodurch Grafikprogrammierer vorkompilierte HLSL-Funktionen erstellen, in Bibliotheken packen und zur Laufzeit in vollständige Shader verknüpfen können. Dies entspricht im Wesentlichen der separaten C/C++-Kompilierung, Bibliotheken und Verknüpfung und ermöglicht Programmierern, vorkompilierten HLSL-Code zu erstellen, wenn weitere Informationen verfügbar sind, um die Berechnung fertig zu stellen. Weitere Informationen zur Verwendung der Shaderverknüpfung finden Sie unter [Verwenden der Shaderverknüpfung.](/windows/desktop/direct3dhlsl/using-shader-linking)

Führen Sie diese Schritte aus, um einen endgültigen Shader mit dynamischer Verknüpfung zur Laufzeit zu erstellen.

**So erstellen und verwenden Sie Shaderverknüpfungen**

1.  Erstellen Sie ein [**ID3D11Linker-Linkerobjekt,**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) das einen Verknüpfungskontext darstellt. Ein einzelner Kontext kann nicht verwendet werden, um mehrere Shader zu erzeugen. Ein Verknüpfungskontext wird verwendet, um einen einzelnen Shader zu erzeugen, und dann wird der Verknüpfungskontext verworfen.
2.  Verwenden [**Sie D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) zum Laden und Festlegen von Bibliotheken aus ihren Bibliothekblobs.
3.  Verwenden [**Sie D3DLoadModule zum**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) Laden und Festlegen eines Eintrags-Shaderblobs, oder erstellen Sie einen [FLG-Shader.](#function-linking-graph-flg)
4.  Verwenden [**Sie ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)::[**CreateInstance,**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) um [**ID3D11ModuleInstance-Objekte**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) zu erstellen, und rufen Sie dann Funktionen für diese Objekte auf, um Ressourcen erneut an ihre endgültigen Slots zu gebunden.
5.  Fügen Sie dem Linker die Bibliotheken hinzu, und rufen Sie dann [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)::[**Link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) auf, um endgültigen Shader-Bytecode zu erstellen, der dann geladen und in der Laufzeit wie ein vollständig vorkompiliertes und verknüpftes Shader verwendet werden kann.

### <a name="function-linking-graph-flg"></a>Funktionsverknüpfungsdiagramm (FLG)

Windows 8.1 fügt auch das Function Linking Graph (FLG) hinzu. Sie können FLG verwenden, um Shader zu erstellen, die aus einer Sequenz von vorkompilierten Funktionsaufrufen bestehen, die Werte aneinander übergeben. Wenn Sie das FLG verwenden, müssen Sie HLSL nicht schreiben und den HLSL-Compiler aufrufen. Stattdessen wird die Shaderstruktur programmgesteuert mithilfe von C++-API-Aufrufen angegeben. FLG-Knoten stellen Eingabe- und Ausgabesignaturen und Aufrufe vorkompilierten Bibliotheksfunktionen dar. Die Reihenfolge der Registrierung der Funktionsaufrufknoten definiert die Sequenz der Aufrufe. Der Eingabesignaturknoten muss zuerst angegeben werden, während der Ausgabesignaturknoten zuletzt angegeben werden muss. FLG-Kanten definieren, wie Werte von einem Knoten an einen anderen übergeben werden. Die Datentypen der übergebenen Werte müssen identisch sein. es gibt keine implizite Typkonvertierung. Form- und Swizzlingregeln folgen dem HLSL-Verhalten, und Werte können nur in dieser Sequenz weitergeleitet werden. Informationen zur FLG-API finden Sie unter [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph).

## <a name="inbox-hlsl-compiler"></a>HLSL-Posteingangscompiler

Der HLSL-Compiler ist jetzt inbox on Windows 8.1 und höher. Jetzt können die meisten APIs für die Shaderprogrammierung in Windows Store-Apps verwendet werden, die für Windows 8.1 und höher erstellt wurden. Viele APIs für die Shaderprogrammierung konnten nicht in Windows Store-Apps verwendet werden, die für Windows 8. Die Referenzseiten für diese APIs wurden mit einem Hinweis markiert. Einige Shader-APIs (z. B. [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)) können jedoch weiterhin nur zum Entwickeln von Windows Store-Apps und nicht in Apps verwendet werden, die Sie an die Windows Store. Die Referenzseiten für diese APIs sind weiterhin mit einem Hinweis gekennzeichnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neues in Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 