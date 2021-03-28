---
title: Direct3D 11,2-Features
description: Die folgende Funktionalität wurde in Direct3D 11,2 hinzugefügt, die in Windows 8.1, Windows RT 8,1 und Windows Server 2012 R2 enthalten ist.
ms.assetid: 2A2D9BBB-F53A-4187-A25B-F4E58C896EE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299b720bfb91297043c8e7d76beb50067eb64e17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976729"
---
# <a name="direct3d-112-features"></a>Direct3D 11,2-Features

Die folgende Funktionalität wurde in Direct3D 11,2 hinzugefügt, die in Windows 8.1, Windows RT 8,1 und Windows Server 2012 R2 enthalten ist.

-   [Gekachelte Ressourcen](#tiled-resources)
    -   [Unterstützung für gekachelte Ressourcen](#check-tiled-resources-support)
-   [Erweiterte Unterstützung für Warp-Geräte](#extended-support-for-warp-devices)
-   [Kommentieren von Grafik Befehlen](#annotate-graphics-commands)
-   [HLSL-Shader-Verknüpfung](#hlsl-shader-linking)
    -   [Funktionsverknüpfungs Diagramm (FLG)](#function-linking-graph-flg)
-   [HLSL-Posteingangs Compiler](#inbox-hlsl-compiler)
-   [Zugehörige Themen](#related-topics)

## <a name="tiled-resources"></a>Gekachelte Ressourcen

Mit Direct3D 11,2 können Sie gekachelte Ressourcen erstellen, die als große logische Ressourcen angesehen werden können, die kleine Mengen an physischem Arbeitsspeicher verwenden. Gekachelte Ressourcen sind nützlich (z. b.) mit Gelände in spielen und der App-Benutzeroberfläche.

Gekachelte Ressourcen werden erstellt, indem das Flag [**D3D11 \_ Resource \_ misc- \_ Kachel**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) angegeben wird. Verwenden Sie diese API, um mit einer gekachelten Ressource zu arbeiten:

-   [**ID3D11Device2:: getresourcetiult**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling)
-   [**ID3D11DeviceContext2:: updatetiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)
-   [**ID3D11DeviceContext2:: updatetilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings)
-   [**ID3D11DeviceContext2:: copytiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles)
-   [**ID3D11DeviceContext2:: copytilemappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings)
-   [**ID3D11DeviceContext2:: resizetilepool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)
-   [**ID3D11DeviceContext2:: tiledresourcebarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier)
-   **D3D11 \_ \_Debugfunktion Deaktivieren der nach \_ Verfolgung von \_ Kacheln nach \_ \_ \_ Verfolgung \_ und \_ Validierung** mit [ **ID3D11Debug:: setfeaturemask**](/windows/desktop/api/D3D11SDKLayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask)

Weitere Informationen zu gekachelten Ressourcen finden Sie unter [gekachelte Ressourcen](tiled-resources.md).

### <a name="check-tiled-resources-support"></a>Unterstützung für gekachelte Ressourcen

Vor der Verwendung von gekachelten Ressourcen müssen Sie herausfinden, ob das Gerät gekachelte Ressourcen unterstützt. So überprüfen Sie die Unterstützung für gekachelte Ressourcen:


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



## <a name="extended-support-for-warp-devices"></a>Erweiterte Unterstützung für Warp-Geräte

Direct3D 11,2 erweitert die Unterstützung von [Warp](overviews-direct3d-11-devices-create-warp.md) -Geräten, die Sie erstellen, indem Sie [**D3D \_ Driver \_ Type \_ Warp**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) in den *DriverType* -Parameter von [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice)übergibt. Der Warp Software-Renderer in Direct3D 11,2 bietet vollständige Unterstützung für die Direct3D- [Funktionsebene](overviews-direct3d-11-devices-downlevel-intro.md) 11 \_ 1, einschließlich der [gekachelten Ressourcen](#tiled-resources), [**"idxgidevice3:: Trim**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidevice3-trim), Shared BCN-Oberflächen, minblend und Karten Standard. Die [doppelte](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_doubles) Unterstützung in HLSL-Shadern wurde ebenfalls mit der Unterstützung für 16X-MSAA ermöglicht.

## <a name="annotate-graphics-commands"></a>Kommentieren von Grafik Befehlen

Mit Direct3D 11,2 können Sie Grafikbefehle mit der folgenden API kommentieren:

-   [**ID3D11DeviceContext2:: isannotationaktivierte**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled)
-   [**ID3D11DeviceContext2:: begineventint**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint)
-   [**ID3D11DeviceContext2:: setmarkerint**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint)
-   [**ID3D11DeviceContext2:: endevent**](/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent)

## <a name="hlsl-shader-linking"></a>HLSL-Shader-Verknüpfung

Windows 8.1 fügt eine separate Kompilierung und Verknüpfung von HLSL-Shadern hinzu, sodass grafikprogrammierer vorkompilierte HLSL-Funktionen erstellen, Sie in Bibliotheken Verpacken und zur Laufzeit mit vollständigen Shadern verknüpfen können. Dabei handelt es sich im Wesentlichen um eine Entsprechung von C/C++ separate Kompilierung, Bibliotheken und Verknüpfungen, und Programmierer können vorkompilierten HLSL-Code verfassen, wenn weitere Informationen verfügbar sind, um die Berechnung abzuschließen. Weitere Informationen zum Verwenden der Shader-Verknüpfung finden Sie unter [Verwenden von Shader-Verknüpfungen](/windows/desktop/direct3dhlsl/using-shader-linking).

Führen Sie diese Schritte aus, um einen abschließenden Shader mithilfe dynamischer Verknüpfungen zur Laufzeit zu erstellen.

**So erstellen und verwenden Sie shaderverknüpfung**

1.  Erstellen Sie ein [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker) Linker-Objekt, das einen Verknüpfungs Kontext darstellt. Ein einzelner Kontext kann nicht zum entwickeln mehrerer Shader verwendet werden. ein Verknüpfungs Kontext wird verwendet, um einen einzelnen Shader zu schaffen, und dann wird der Verknüpfungs Kontext entfernt.
2.  Verwenden Sie [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) , um Bibliotheken in Ihren Bibliotheks-blobden zu laden und festzulegen.
3.  Verwenden Sie [**D3DLoadModule**](/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule) , um einen Eintrag-Shader-BLOB zu laden und festzulegen, oder erstellen Sie einen [FLG-Shader](#function-linking-graph-flg).
4.  Verwenden Sie [**ID3D11Module**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11module)::[**CreateInstance**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11module-createinstance) , um [**ID3D11ModuleInstance**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11moduleinstance) -Objekte zu erstellen, und rufen Sie dann Funktionen für diese Objekte auf, um Ressourcen erneut an ihre endgültigen Slots zu binden.
5.  Fügen Sie die Bibliotheken zum Linker hinzu, und rufen Sie dann [**ID3D11Linker**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11linker)::[**Link**](/windows/desktop/api/D3D11Shader/nf-d3d11shader-id3d11linker-link) auf, um den endgültigen Shader-Bytecode zu erstellen, der dann wie ein vollständig vorkompilierter und verknüpfter Shader in der Laufzeit geladen und verwendet werden kann.

### <a name="function-linking-graph-flg"></a>Funktionsverknüpfungs Diagramm (FLG)

Windows 8.1 fügt auch das FLG (Function Linking Graph) hinzu. Sie können FLG zum Erstellen von Shadern verwenden, die aus einer Sequenz von vorkompilierten Funktionsaufrufen bestehen, von denen Werte an einander übergeben werden. Wenn Sie das FLG verwenden, ist es nicht erforderlich, HLSL zu schreiben und den HLSL-Compiler aufzurufen. Stattdessen wird die Shader-Strukturprogramm gesteuert mithilfe von C++-API-aufrufen angegeben. FLG-Knoten stellen Eingabe-und Ausgabe Signaturen und Aufrufe von vorkompilierten Bibliotheksfunktionen dar. Die Reihenfolge, in der die Funktionsaufruf Knoten registriert werden, definiert die Abfolge der Aufrufe. Der Eingabe Signatur Knoten muss zuerst angegeben werden, während der Ausgabe Signatur Knoten zuletzt angegeben werden muss. FLG-Kanten definieren, wie Werte von einem Knoten an einen anderen übermittelt werden. Die Datentypen der bestandenen Werte müssen identisch sein. Es gibt keine implizite Typkonvertierung. Shape-und swishingregeln folgen dem HLSL-Verhalten, und die Werte können nur in dieser Sequenz weitergeleitet werden. Informationen zur FLG-API finden Sie unter [**ID3D11FunctionLinkingGraph**](/windows/desktop/api/D3D11Shader/nn-d3d11shader-id3d11functionlinkinggraph).

## <a name="inbox-hlsl-compiler"></a>HLSL-Posteingangs Compiler

Der HLSL-Compiler ist nun in Windows 8.1 und höher Eingangsbox. Nun können die meisten APIs für die Shader-Programmierung in Windows Store-Apps verwendet werden, die für Windows 8.1 und höher erstellt werden. Viele APIs für die Shader-Programmierung konnten in Windows Store-Apps, die für Windows 8 erstellt wurden, nicht verwendet werden. die Referenzseiten für diese APIs wurden mit einer Notiz gekennzeichnet. Einige shaderapis (z. b. [**D3DCompileFromFile**](/windows/desktop/direct3dhlsl/d3dcompilefromfile)) können jedoch nur zum Entwickeln von Windows Store-Apps und nicht in Apps verwendet werden, die Sie an den Windows Store übermitteln. die Referenzseiten für diese APIs sind immer noch mit einer Notiz gekennzeichnet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Neuerungen in Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 