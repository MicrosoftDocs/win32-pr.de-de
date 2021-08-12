---
title: Oberflächenfreigabe zwischen Windows-APIs
description: Dieses Thema bietet eine technische Übersicht über die Interoperabilität mithilfe der Oberflächenfreigabe zwischen Windows-Grafik-APIs, einschließlich Direct3D 11, Direct2D, DirectWrite, Direct3D 10 und Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15a5d3e1b52691aeaee2373600dc247da679f0e452a6737741418e54df9490a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290221"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a>Oberflächenfreigabe zwischen Windows-APIs

Dieses Thema bietet eine technische Übersicht über die Interoperabilität mithilfe der Oberflächenfreigabe zwischen Windows-Grafik-APIs, einschließlich Direct3D 11, Direct2D, DirectWrite, Direct3D 10 und Direct3D 9Ex. Wenn Sie bereits über Kenntnisse dieser APIs verfügen, können Sie in diesem Artikel mehrere APIs verwenden, um in einer Anwendung, die für die Betriebssysteme Windows 7 oder Windows Vista entwickelt wurde, auf derselben Oberfläche zu rendern. Dieses Thema enthält auch Best Practices-Richtlinien und Zeiger auf zusätzliche Ressourcen.

> [!Note]  
> Für Direct2D- und DirectWrite-Interoperabilität in der DirectX 11.1-Runtime können Sie [Direct2D-Geräte](/windows/desktop/Direct2D/devices-and-device-contexts) und Gerätekontexte verwenden, um direkt auf Direct3D 11-Geräten zu rendern.

 

Dieses Thema enthält folgende Abschnitte:

-   [Introduction (Einführung)](#introduction)
-   [Übersicht über die API-Interoperabilität](#api-interoperability-overview)
-   [Interoperabilitätsszenarien](#interoperability-scenarios)
    -   [Direct3D 10.1-Gerätefreigabe mit Direct2D](#direct3d-101-device-sharing-with-direct2d)
    -   [DXGI 1.1 Synchronisierte freigegebene Oberflächen](#dxgi-11-synchronized-shared-surfaces)
    -   [Interoperabilität zwischen Direct3D 9Ex- und DXGI-basierten APIs](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [Zusammenfassung](#conclusion)

## <a name="introduction"></a>Einführung

In diesem Dokument bezieht Windows-API-Interoperabilität auf die Gemeinsame Nutzung derselben Renderingoberfläche durch verschiedene APIs. Diese Art von Interoperabilität ermöglicht es Anwendungen, überzeugende Displays zu erstellen, indem sie mehrere Windows-Grafik-APIs nutzen und die Migration zu neuen Technologien erleichtern, indem die Kompatibilität mit vorhandenen APIs aufrechterhalten wird.

In Windows 7 (und Windows Vista SP2 mit Windows 7 Interop Pack, Vista 7IP) sind die Grafikrendering-APIs Direct3D 11, Direct2D, Direct3D 10.1, Direct3D 10.0, Direct3D 9Ex, Direct3D 9c und frühere Direct3D-APIs sowie GDI und GDI+. Windows Imaging Component (WIC) und DirectWrite sind verwandte Technologien für die Bildverarbeitung, und Direct2D führt Textrendering durch. Die DirectX-Videobeschleunigungs-API (DXVA), die auf Direct3D 9c und Direct3D 9Ex basiert, wird für die Videoverarbeitung verwendet.

Da Windows Grafik-APIs in Richtung Direct3D-basiert weiterentwickelt werden, investiert Microsoft mehr Aufwand in die Sicherstellung der APIs-übergreifenden Interoperabilität. Neu entwickelte Direct3D-APIs und APIs auf höherer Ebene, die auf Direct3D-APIs basieren, bieten bei Bedarf auch Unterstützung für die Überbrückung der Kompatibilität mit älteren APIs. Zur Veranschaulichung können Direct2D-Anwendungen Direct3D 10.1 verwenden, indem sie ein Direct3D 10.1-Gerät freigeben. Außerdem können Direct3D 11-, Direct2D- und Direct3D 10.1-APIs von DirectX Graphic Infrastructure (DXGI) 1.1 profitieren, was synchronisierte freigegebene Oberflächen ermöglicht, die die Interoperabilität zwischen diesen APIs vollständig unterstützen. DXGI 1.1-basierte APIs interoperieren mit GDI und mit GDI+ durch Zuordnung, indem sie den GDI-Gerätekontext von einer DXGI 1.1-Oberfläche abrufen. Weitere Informationen finden Sie in der DXGI- und GDI-Interoperabilitätsdokumentation auf MSDN.

Die nicht synchronisierte Oberflächenfreigabe wird von der Direct3D 9Ex-Runtime unterstützt. DXVA-basierte Videoanwendungen können das Direct3D 9Ex- und DXGI-Interoperabilitätshilfe für die Direct3D 9Ex-basierte DXVA-Interoperabilität mit Direct3D 11 für Compute-Shader verwenden oder mit Direct2D für 2D-Steuerelemente oder Textrendering zusammenarbeiten. WIC und DirectWrite auch mit GDI, Direct2D und anderen Direct3D-APIs zusammenarbeiten.

Direct3D 10.0, Direct3D 9c und ältere Direct3D-Runtimes unterstützen keine freigegebenen Oberflächen. Systemspeicherkopien werden weiterhin für die Interoperabilität mit GDI- oder DXGI-basierten APIs verwendet.

Beachten Sie, dass sich die Interoperabilitätsszenarien in diesem Dokument auf mehrere Grafik-APIs beziehen, die auf eine freigegebene Renderingoberfläche und nicht auf dasselbe Anwendungsfenster gerendert werden. Die Synchronisierung für separate APIs für verschiedene Oberflächen, die dann im selben Fenster zusammengesetzt werden, liegt außerhalb des Bereichs dieses Whitepapers.

## <a name="api-interoperability-overview"></a>Übersicht über die API-Interoperabilität

Die Oberflächenfreigabe-Interoperabilität Windows Grafik-APIs kann in Bezug auf API-zu-API-Szenarien und die entsprechende Interoperabilitätsfunktionalität beschrieben werden. Ab Windows 7 und ab Windows Vista SP2 mit 7IP enthalten neue APIs und zugehörige Runtimes Direct2D und zugehörige Technologien: Direct3D 11 und DXGI 1.1. Die GDI-Leistung wurde auch in Windows 7 verbessert. Direct3D 10.1 wurde in Windows Vista SP1 eingeführt. Das folgende Diagramm zeigt die Interoperabilitätsunterstützung zwischen APIs.

![Diagramm der Interoperabilitätsunterstützung zwischen Windows-Grafik-APIs](images/surface-sharing-interoperability.png)

In diesem Diagramm zeigen Pfeile Interoperabilitätsszenarien, in denen die verbundenen APIs auf dieselbe Oberfläche zugriffen können. Blaue Pfeile weisen auf Interoperabilitätsmechanismen hin, die in Windows Vista eingeführt wurden. Grüne Pfeile weisen auf die Interoperabilitätsunterstützung für neue APIs oder Verbesserungen hin, die ältere APIs bei der Zusammenarbeit mit neueren APIs unterstützen. Beispielsweise stellen grüne Pfeile die Gerätefreigabe, die Unterstützung synchronisierter freigegebener Oberflächen, das Direct3D 9Ex/DXGI-Synchronisierungshilfe und das Abrufen eines GDI-Gerätekontexts von einer kompatiblen Oberfläche dar.

## <a name="interoperability-scenarios"></a>Interoperabilitätsszenarien

Ab Windows 7 und Windows Vista 7IP unterstützen gängige Angebote von Windows-Grafik-APIs mehrere APIs, die auf derselben DXGI 1.1-Oberfläche gerendert werden.

**Direct3D 11, Direct3D 10.1, Direct2D – Interoperabilität untereinander**

Direct3D 11-, Direct3D 10.1- und Direct2D-APIs (und die zugehörigen APIs wie DirectWrite und WIC) können über die Direct3D 10.1-Gerätefreigabe oder synchronisierte freigegebene Oberflächen miteinander zusammenarbeiten.

### <a name="direct3d-101-device-sharing-with-direct2d"></a>Direct3D 10.1-Gerätefreigabe mit Direct2D

Die Gerätefreigabe zwischen Direct2D und Direct3D 10.1 ermöglicht es einer Anwendung, beide APIs zu verwenden, um nahtlos und effizient auf derselben DXGI 1.1-Oberfläche mit dem gleichen zugrunde liegenden Direct3D-Geräteobjekt zu rendern. Direct2D bietet die Möglichkeit zum Aufrufen von Direct2D-APIs mithilfe eines vorhandenen Direct3D 10.1-Geräts. Dabei wird die Tatsache genutzt, dass Direct2D auf Direct3D 10.1- und DXGI 1.1-Runtimes basiert. Die folgenden Codeausschnitte veranschaulichen, wie Direct2D das Direct3D 10.1-Geräterenderingziel von einer DXGI 1.1-Oberfläche erhält, die dem Gerät zugeordnet ist. Das Direct3D 10.1-Geräterenderingziel kann Direct2D-Zeichnungsaufrufe zwischen BeginDraw- und EndDraw-APIs ausführen.


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



**Anmerkungen**

-   Das zugeordnete Direct3D 10.1-Gerät muss das BGRA-Format unterstützen. Dieses Gerät wurde durch Aufrufen von D3D10CreateDevice1 mit dem Parameter D3D10 \_ CREATE \_ DEVICE \_ BGRA SUPPORT \_ erstellt. Das BGRA-Format wird ab Direct3D 10 Featureebene 9.1 unterstützt.
-   Die Anwendung sollte nicht mehrere ID2D1RenderTargets erstellen, die demselben Direct3D10.1-Gerät zuordnen.
-   Um eine optimale Leistung zu erzielen, sollten Sie jederzeit mindestens eine Ressource verwenden, z. B. Texturen oder Oberflächen, die dem Gerät zugeordnet sind.

Die Gerätefreigabe eignet sich für die Prozess-Singlethread-Verwendung eines Renderinggeräts, das von Direct3D 10.1- und Direct2D-Rendering-APIs gemeinsam genutzt wird. Synchronisierte freigegebene Oberflächen ermöglichen die Verwendung mehrerer Renderinggeräte, die von Direct3D 10.1-, Direct2D- und Direct3D 11-APIs verwendet werden.

Eine weitere Methode der Direct3D 10.1- und Direct2D-Interoperabilität ist die Verwendung von ID3D1RenderTarget::CreateSharedBitmap, die ein ID2D1Bitmap-Objekt aus IDXGISurface erstellt. Sie können eine Direct3D10.1-Szene in die Bitmap schreiben und mit Direct2D rendern. Weitere Informationen finden Sie unter [ID2D1RenderTarget::CreateSharedBitmap-Methode.](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)

### <a name="direct2d-software-rasterization"></a>Direct2D-Softwarerasterung

Die Gerätefreigabe mit Direct3D 10.1 wird bei Verwendung des Direct2D-Softwarerenderers nicht unterstützt, z. B. durch Angabe von D2D1 RENDER TARGET USAGE FORCE SOFTWARE RENDERING in D2D1 RENDER TARGET USAGE beim Erstellen eines \_ \_ \_ \_ \_ \_ \_ \_ \_ Direct2D-Renderziels.

Direct2D kann den Softwareraster WARP10 verwenden, um das Gerät mit Direct3D 10 oder Direct3D 11 zu teilen, aber die Leistung sinkt erheblich.

### <a name="dxgi-11-synchronized-shared-surfaces"></a>DXGI 1.1 Synchronisierte freigegebene Oberflächen

Direct3D 11-, Direct3D 10.1- und Direct2D-APIs verwenden dxgi 1.1, das die Funktionalität bietet, das Lesen von und Schreiben von zwei oder mehr Direct3D-Geräten von derselben Videospeicheroberfläche (DXGISurface1) zu synchronisieren. Die Renderinggeräte, die synchronisierte freigegebene Oberflächen verwenden, können Direct3D 10.1- oder Direct3D 11-Geräte sein, die jeweils im selben Prozess oder prozessübergreifend ausgeführt werden.

Anwendungen können synchronisierte freigegebene Oberflächen verwenden, um zwischen allen DXGI 1.1-basierten Geräten wie Direct3D 11 und Direct3D 10.1 oder zwischen Direct3D 11 und Direct2D zu zusammenarbeiten, indem sie das Direct3D 10.1-Gerät aus dem Direct2D-Renderzielobjekt abrufen.

Stellen Sie für die Verwendung von DXGI 1.1 in Direct3D 10.1 und höher sicher, dass das Direct3D-Gerät mithilfe eines DXGI 1.1-Adapterobjekts erstellt wird, das aus dem DXGI 1.1-Factoryobjekt aufzählt wird. Rufen Sie CreateDXGIFactory1 auf, um das IDXGIFactory1-Objekt zu erstellen, und EnumAdapters1, um das IDXGIAdapter1-Objekt zu aufzählen. Das IDXGIAdapter1-Objekt muss als Teil des D3D10CreateDevice- oder D3D10CreateDeviceAndSwapChain-Aufrufs übergeben werden. Weitere Informationen zu DXGI 1.1-APIs finden Sie im [Programmierhandbuch für DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).

### <a name="apis"></a>APIs

**D3D10 \_ RESOURCE \_ MISC \_ SHARED \_ KEYEDMUTEX**  
Legen Sie beim Erstellen der synchronisierten freigegebenen Ressource D3D10 \_ RESOURCE \_ MISC \_ SHARED \_ KEYEDMUTEX in D3D10 \_ RESOURCE \_ MISC FLAG \_ fest.  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



**D3D10 \_ RESOURCE \_ MISC \_ SHARED \_ KEYEDMUTEX**  
Ermöglicht die Synchronisierung der erstellten Ressource mithilfe der IDXGIKeyedMutex::AcquireSync- und ReleaseSync-APIs. Die folgenden Direct3D 10.1-APIs für die Ressourcenerstellung, die alle den PARAMETER D3D10 RESOURCE MISC FLAG verwenden, wurden erweitert, um das neue \_ \_ Flag zu \_ unterstützen.  

-   ID3D10Device1::CreateTexture1D
-   ID3D10Device1::CreateTexture2D
-   ID3D10Device1::CreateTexture3D
-   ID3D10Device1::CreateBuffer

  
Wenn eine der aufgelisteten Funktionen mit dem D3D10 RESOURCE MISC SHARED KEYEDMUTEX-Flag aufgerufen wird, kann die zurückgegebene Schnittstelle nach einer \_ \_ \_ IDXGIKeyedMutex-Schnittstelle abgefragt werden, die AcquireSync- und ReleaseSync-APIs implementiert, um den Zugriff auf die Oberfläche zu \_ synchronisieren. Das Gerät, das die Oberfläche erstellt, und jedes andere Gerät, das die Oberfläche öffnet (mit OpenSharedResource), muss IDXGIKeyedMutex::AcquireSync vor rendering-Befehlen auf der Oberfläche und IDXGIKeyedMutex::ReleaseSync aufrufen, wenn das Rendering fertig ist.  
WARP- und REF-Geräte unterstützen keine freigegebenen Ressourcen. Wenn Sie versuchen, eine Ressource mit diesem Flag auf einem WARP- oder REF-Gerät zu erstellen, gibt die create-Methode einen E \_ OUTOFMEMORY-Fehlercode zurück.  
**IDXGIKEYEDMUTEX-SCHNITTSTELLE**  
Eine neue Schnittstelle in DXGI 1.1, IDXGIKeyedMutex, stellt einen schlüsselierten Mutex dar, der exklusiven Zugriff auf eine freigegebene Ressource ermöglicht, die von mehreren Geräten verwendet wird. Eine Referenzdokumentation zu dieser Schnittstelle und den beiden Methoden AcquireSync und ReleaseSync finden Sie unter [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a>Beispiel: Synchronisierte Oberflächenfreigabe zwischen zwei Direct3D 10.1-Geräten

Das folgende Beispiel veranschaulicht die Gemeinsame Nutzung einer Oberfläche zwischen zwei Direct3D 10.1-Geräten. Die synchronisierte freigegebene Oberfläche wird von einem Direct3D10.1-Gerät erstellt.


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



Dasselbe Direct3D10.1-Gerät kann die synchronisierte freigegebene Oberfläche für das Rendering abrufen, indem AcquireSync aufruft und dann die Oberfläche für das Rendering des anderen Geräts durch Aufrufen von ReleaseSync freigegeben wird. Wenn die synchronisierte freigegebene Oberfläche nicht für ein anderes Direct3D-Gerät freigegeben wird, kann der Ersteller die synchronisierte freigegebene Oberfläche (zum Starten und Beenden des Renderings) abrufen und freigeben, indem er denselben Schlüsselwert erhält und frei gibt.


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



Das zweite Direct3D10.1-Gerät kann die synchronisierte freigegebene Oberfläche für das Rendering abrufen, indem AcquireSync aufruft und dann die Oberfläche für das Rendering des ersten Geräts durch Aufrufen von ReleaseSync freigegeben wird. Beachten Sie, dass Gerät 2 die synchronisierte freigegebene Oberfläche mit dem gleichen Schlüsselwert wie im ReleaseSync-Aufruf von Gerät 1 erhalten kann.


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



Zusätzliche Geräte, die dieselbe Oberfläche verwenden, können die Oberfläche mit zusätzlichen Schlüsseln abrufen und freigeben, wie in den folgenden Aufrufen gezeigt.


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



Beachten Sie, dass eine reale Anwendung möglicherweise immer auf einer Zwischenoberfläche gerendert wird, die dann auf die freigegebene Oberfläche kopiert wird, um zu verhindern, dass ein Gerät auf ein anderes Gerät wartet, das die Oberfläche teilt.

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a>Verwenden synchronisierter freigegebener Oberflächen mit Direct2D und Direct3D 11

Auf ähnliche Weise kann für die Freigabe zwischen Direct3D 11- und Direct3D 10.1-APIs eine synchronisierte freigegebene Oberfläche entweder über ein API-Gerät erstellt und mit den anderen API-Geräten gemeinsam genutzt werden.

Anwendungen, die Direct2D verwenden, können ein Direct3D 10.1-Gerät gemeinsam nutzen und eine synchronisierte freigegebene Oberfläche verwenden, um mit Direct3D 11 oder anderen Direct3D 10.1-Geräten zu zusammenarbeiten, unabhängig davon, ob sie demselben Prozess oder verschiedenen Prozessen angehören. Bei Singlethreadanwendungen mit nur einem Prozess ist die Gerätefreigabe jedoch die leistungsfähigste und effizienteste Interoperabilitätsmethode zwischen Direct2D und Direct3D 10 oder Direct3D 11.

### <a name="software-rasterizer"></a>Softwarerasterizer

Synchronisierte freigegebene Oberflächen werden nicht unterstützt, wenn Anwendungen die Direct3D- oder Direct2D-Softwarerasterizer verwenden, einschließlich des Referenzrasterizers und WARP, anstatt die Grafikhardwarebeschleunigung zu verwenden.

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a>Interoperabilität zwischen Direct3D 9Ex- und DXGI-basierten APIs

Direct3D 9Ex-APIs enthielten das Konzept der Oberflächenfreigabe, damit andere APIs von der freigegebenen Oberfläche lesen können. Um Lese- und Schreibvorgänge für eine freigegebene Direct3D 9Ex-Oberfläche freizugeben, müssen Sie der Anwendung selbst eine manuelle Synchronisierung hinzufügen.

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a>Direct3D 9Ex Shared Surfaces Plus Manual Synchronization Helper

Die grundlegendste Aufgabe in der Interoperabilität von Direct3D 9Ex und Direct3D 10 oder 11 besteht darin, eine einzelne Oberfläche vom ersten Gerät (Gerät A) an das zweite Gerät (Gerät B) zu übergeben, sodass das Rendering von Gerät A garantiert abgeschlossen ist, wenn Gerät B ein Handle auf der Oberfläche erhält. Daher kann Gerät B diese Oberfläche ohne Bedenken verwenden. Dies ähnelt dem klassischen Producer-Consumer-Problem, und diese Diskussion modelliert das Problem auf diese Weise. Das erste Gerät, das die Oberfläche verwendet und dann auf diesen zurückstellt, ist der Producer (Gerät A), und das Gerät, das anfänglich wartet, ist der Consumer (Gerät B). Jede reale Anwendung ist komplexer als diese und verkettet mehrere Producer-Consumer-Bausteine, um die gewünschte Funktionalität zu erstellen.

Die Producer-Consumer-Bausteine werden mithilfe einer Warteschlange von Oberflächen in das Hilf hilft implementiert. Oberflächen werden vom Producer in die Schube gestellt und vom Consumer aus der Quehiert. Das Hilfprogramm stellt drei COM-Schnittstellen vor: ISurfaceQueue, ISurfaceProducer und ISurfaceConsumer.

### <a name="high-level-overview-of-helper"></a>High-Level Übersicht über das Hilf hilft

Das ISurfaceQueue-Objekt ist der Baustein für die Verwendung der freigegebenen Oberflächen. Es wird mit einem initialisierten Direct3D-Gerät und einer Beschreibung erstellt, um eine feste Anzahl freigegebener Oberflächen zu erstellen. Das Warteschlangenobjekt verwaltet die Erstellung von Ressourcen und das Öffnen von Code. Die Anzahl und der Typ der Oberflächen sind fest. Sobald die Oberflächen erstellt wurden, kann die Anwendung sie weder hinzufügen noch entfernen.

Jede Instanz des ISurfaceQueue-Objekts stellt eine Art Ein-Wege-Straße bereit, die zum Senden von Oberflächen vom erzeugenden Gerät an das gerät verwendet werden kann. Mehrere dieser eindirektionischen Straßen können verwendet werden, um szenarienübergreifende Oberflächenfreigaben zwischen Geräten bestimmter Anwendungen zu ermöglichen.

**Erstellungs-/Objektlebensdauer**  
Es gibt zwei Möglichkeiten, das Warteschlangenobjekt zu erstellen: über CreateSurfaceQueue oder über die Clone-Methode von ISurfaceQueue. Da es sich bei den Schnittstellen um COM-Objekte handelt, wird die STANDARDMÄßIGE VERWALTUNG DER COM-Lebensdauer angewendet.  
**Producer/Consumer-Modell**  
Enqueue (): Der Producer ruft diese Funktion auf, um anzugeben, dass sie mit der Oberfläche erfolgt, die jetzt für ein anderes Gerät verfügbar sein kann. Nach der Rückkehr von dieser Funktion verfügt das Producergerät nicht mehr über Rechte an der Oberfläche, und es ist unsicher, es weiterhin zu verwenden.  
Dequeue (): Das nutzende Gerät ruft diese Funktion auf, um eine freigegebene Oberfläche zu erhalten. Die API stellt sicher, dass alle aus der Quehnung genommenen Oberflächen einsatzbereit sind.  
**Metadaten**  
Die API unterstützt das Zuordnen von Metadaten zu den freigegebenen Oberflächen.  
Enqueue() hat die Möglichkeit, zusätzliche Metadaten anzugeben, die an das nutzende Gerät übergeben werden. Die Metadaten müssen kleiner als ein maximaler Wert sein, der zum Erstellungszeitpunkt bekannt ist.  
Dequeue() kann optional einen Puffer und einen Zeiger auf die Größe des Puffers übergeben. Die Warteschlange füllt den Puffer mit den Metadaten des entsprechenden Enqueue-Aufrufs aus.  
**Klonen?**  
Jedes ISurfaceQueue-Objekt löst eine einseitige Synchronisierung. Wir gehen davon aus, dass die überwiegende Mehrheit der Anwendungen, die diese API verwenden, ein geschlossenes System verwenden wird. Das einfachste geschlossene System mit zwei Geräten, die Oberflächen hin und her senden, erfordert zwei Warteschlangen. Das ISurfaceQueue-Objekt verfügt über eine Clone()-Methode, die es ermöglicht, mehrere Warteschlangen zu erstellen, die alle Teil derselben größeren Pipeline sind.  
Clone erstellt ein neues ISurfaceQueue-Objekt aus einem vorhandenen Objekt und teilt alle geöffneten Ressourcen zwischen ihnen. Das resultierende Objekt verfügt über genau die gleichen Oberflächen wie die Quellwarteschlange. Geklonte Warteschlangen können unterschiedliche Metadatengrößen aufweisen.  
**Surface**  
ISurfaceQueue übernimmt die Verantwortung für das Erstellen und Verwalten seiner Oberflächen. Es ist nicht gültig, beliebige Oberflächen in die Enqueue einzudingen. Darüber hinaus sollte eine Oberfläche nur über einen aktiven "Besitzer" verfügen. Sie sollte sich entweder in einer bestimmten Warteschlange befinden oder von einem bestimmten Gerät verwendet werden. Es ist nicht zulässig, ihn in mehreren Warteschlangen zu speichern oder geräte die Oberfläche nach dem Einreihen in die Warteschlange weiter zu verwenden.  
</dl>

### <a name="api-details"></a>API-Details

### <a name="isurfacequeue"></a>IsurfaceQueue

Die Warteschlange ist für das Erstellen und Verwalten der freigegebenen Ressourcen verantwortlich. Sie bietet auch die Funktionalität zum Verketten mehrerer Warteschlangen mit clone. Die Warteschlange verfügt über Methoden, die das erzeugende Gerät und ein nutzendes Gerät öffnen. Es kann jeweils nur jeweils einer geöffnet werden.

Die Warteschlange macht die folgenden APIs verfügbar:



| API                            | Beschreibung                                                                                 |
|-----------------------------|----------------------------------------------------------------------------------|
| CreateSurfaceQueue          | Erstellt ein ISurfaceQueue-Objekt (die "Root"-Warteschlange).                              |
| ISurfaceQueue::OpenConsumer | Gibt eine Schnittstelle für das gerät zurück, das die Veröffentlichung aus der Quehnung des geräts verwendet.                        |
| ISurfaceQueue::OpenProducer | Gibt eine Schnittstelle für das erzeugende Gerät zurück, das in die Queue einrückt.                        |
| ISurfaceQueue::Clone        | Erstellt ein ISurfaceQueue-Objekt, das Oberflächen mit dem Stammwarteschlangenobjekt teilt. |



 

**CreateSurfaceQueue**  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



**Mitglieder**  

**Width**, **Height**  Die Abmessungen der freigegebenen Oberflächen. Alle freigegebenen Oberflächen müssen die gleichen Dimensionen aufweisen.  
**Formatieren** Das Format der freigegebenen Oberflächen. Alle freigegebenen Oberflächen müssen das gleiche Format aufweisen. Die gültigen Formate hängen von den verwendeten Geräten ab, da verschiedene Gerätepaare unterschiedliche Formattypen gemeinsam verwenden können.  
**NumSurfaces**  Die Anzahl der Oberflächen, die Teil der Warteschlange sind. Dies ist eine feste Zahl.  
 **MetaDataSize**  Die maximale Größe des Metadatenpuffers.  
**Flags**  Flags zum Steuern des Verhaltens der Warteschlange. Siehe Hinweise.  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parameter**

 *pDesc* \[ in \]  Die Beschreibung der zu erstellenden freigegebenen Surface-Warteschlange.  

 *pDevice* \[ in \]  Das Gerät, das zum Erstellen der freigegebenen Oberflächen verwendet werden soll. Dies ist ein expliziter Parameter aufgrund eines Features in Windows Vista. Für Oberflächen, die von Direct3D 9 und Direct3D 10 gemeinsam genutzt werden, müssen die Oberflächen mit Direct3D 9 erstellt werden.  

 *ppQueue* \[ out \]  Enthält bei rückgabe einen Zeiger auf das ISurfaceQueue-Objekt.  


**Rückgabewerte**

Wenn *pDevice* nicht in der Lage ist, Ressourcen gemeinsam zu nutzen, gibt diese Funktion DXGI \_ ERROR INVALID CALL \_ \_ zurück. Diese Funktion erstellt die Ressourcen. Wenn ein Fehler auftritt, wird ein Fehler zurückgegeben. Wenn dies erfolgreich ist, wird S \_ OK zurückgegeben.

**Anmerkungen**

Beim Erstellen des Warteschlangenobjekts werden auch alle Oberflächen erstellt. Alle Oberflächen werden als 2D-Renderziele angenommen und mit den festgelegten RESSOURCENflags D3D10 \_ BIND RENDER TARGET und \_ \_ D3D10 \_ BIND \_ SHADER RESOURCE \_ (oder den entsprechenden Flags für die verschiedenen Runtimes) erstellt.

Der Entwickler kann ein Flag angeben, das angibt, ob mehrere Threads auf die Warteschlange zugreifen. Wenn keine Flags festgelegt sind **(Flags** == 0), wird die Warteschlange von mehreren Threads verwendet. Der Entwickler kann Singlethreadzugriff angeben, wodurch der Synchronisierungscode deaktiviert und eine Leistungsverbesserung für diese Fälle ermöglicht wird. Jede geklonte Warteschlange verfügt über ein eigenes Flag, sodass verschiedene Warteschlangen im System über unterschiedliche Synchronisierungssteuerelemente verfügen können.

 **Öffnen eines Producers**  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



**Parameter**  

*pDevice* \[ In\]  

Das Producergerät, das Oberflächen in die Oberflächenwarteschlange einreiht. 

*ppProducer* \[ out \] Gibt ein -Objekt an die Producerschnittstelle zurück.  


**Rückgabewerte**

Wenn das Gerät keine Oberflächen freigeben kann, gibt DXGI \_ ERROR \_ INVALID CALL \_ zurück.

**Öffnen eines Consumers**  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



**Parameter**  
 *pDevice* \[ In\]  
 Das Consumergerät, das Oberflächen aus der Oberflächenwarteschlange aus der Warteschlange entfernt. 
 *ppConsumer* \[ out \]  Gibt ein Objekt an die Consumerschnittstelle zurück.  


**Rückgabewerte**

Wenn das Gerät keine Oberflächen freigeben kann, gibt DXGI \_ ERROR \_ INVALID CALL \_ zurück.

**Anmerkungen**

Diese Funktion öffnet alle Oberflächen in der Warteschlange für das Eingabegerät und speichert sie zwischen. Nachfolgende Aufrufe von Dequeue werden einfach in den Cache übertragen und müssen die Oberflächen nicht jedes Mal erneut öffnen.



### <a name="cloning-an-idxgixsurfacequeue"></a>Klonen einer IDXGIXSurfaceQueue




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



**Die** **Elemente MetaDataSize** **und Flags** haben das gleiche Verhalten wie für CreateSurfaceQueue.  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parameter**

*pDesc* \[ in Einer Struktur, die eine Beschreibung des zu \] erstellenden Klonobjekts enthält. Dieser Parameter sollte initialisiert werden.  
*ppQueue* \[ out \] Gibt das initialisierte Objekt zurück.  
</dl>

**Anmerkungen**

Sie können aus jedem vorhandenen Warteschlangenobjekt klonen, auch wenn es sich nicht um das Stammobjekt handelt.  
</dl>

### <a name="idxgixsurfaceconsumer"></a>IDXGIXSurfaceConsumer

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



**Parameter**  
*id* \[ in\]  
Die REFIID einer 2D-Oberfläche des verbrauchten Geräts.  

-   Für IDirect3DDevice9 sollte die REFIID \_ \_ uuidof(IDirect3DTexture9) sein.
-   Für eine ID3D10Device sollte die REFIID \_ \_ uuidof(ID3D10Texture2D) sein.
-   Für eine ID3D11Device sollte die REFIID \_ \_ uuidof(ID3D11Texture2D) sein.

*ppSurface* \[ out \] Gibt einen Zeiger auf die Oberfläche zurück.  
*pBuffer* \[ in, out Ein optionaler Parameter und wenn nicht NULL, enthält bei rückgabe die Metadaten, die beim entsprechenden \] Enqueue-Aufruf übergeben wurden.   
*pBufferSize* \[ in, out \] Die Größe *von pBuffer* in Bytes. Gibt die Anzahl der in *pBuffer* zurückgegebenen Bytes zurück. Wenn der Enqueue-Aufruf keine Metadaten enthält, *wird pBuffer* auf 0 festgelegt.  
*dwTimeout* \[ in \] Gibt einen Timeoutwert an. Weitere Informationen finden Sie in den Anmerkungen.  
</dl>

**Rückgabewerte**

Diese Funktion kann WAIT TIMEOUT zurückgeben, wenn ein Timeoutwert angegeben wird und die Funktion nicht \_ vor dem Timeoutwert zurück gibt. Siehe Hinweise. Wenn keine Oberflächen verfügbar sind, gibt die Funktion zurück, wenn *ppSurface* auf **NULL** und *pBufferSize* auf 0 festgelegt ist und der Rückgabewert 0x80070120 (WIN32 \_ TO \_ HRESULT(WAIT \_ TIMEOUT)) ist.  
</dl>

**Anmerkungen**

Diese API kann blockieren, wenn die Warteschlange leer ist. Der *dwTimeout-Parameter* funktioniert identisch mit den Windows Synchronisierungs-APIs, z. B. WaitForSingleObject. Verwenden Sie für nicht blockierende Verhalten ein Timeout von 0.  
</dl>

### <a name="isurfaceproducer"></a>ISurfaceProducer

Diese Schnittstelle stellt zwei Methoden bereit, die es der App ermöglichen, Oberflächen in die Queue zu enqueue. Nachdem eine Oberfläche in die Enqueued-2016-Oberfläche eingeändert wurde, ist der Oberflächenzeiger nicht mehr gültig und nicht sicher zu verwenden. Die einzige Aktion, die die Anwendung mit dem Zeiger ausführen sollte, ist die Freigabe.



| Methode                          | Beschreibung                                                                                                                                                      |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISurfaceProducer::Enqueue | Reiht eine Oberfläche in das Warteschlangenobjekt ein. Nach Abschluss dieses Aufrufs wird der Producer mit der Oberfläche und die Oberfläche für ein anderes Gerät vorbereitet. |
| ISurfaceProducer::Flush   | Wird verwendet, wenn die Anwendungen nicht blockierend sein sollen. Einzelheiten finden Sie in den Hinweisen.                                                                  |



 

**Einreihen in die Warteschlange**  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



**Parameter**  
*pSurface* \[ In\]  
Die Oberfläche des erzeugenden Geräts, das in die Queued- Enqueuing eingeändert werden muss. Diese Oberfläche muss eine Oberfläche sein, die aus demselben Warteschlangennetzwerk aus der Warteschlange entfernt wird. *pBuffer* \[ in \] Ein optionaler Parameter, der zum Übergeben von Metadaten verwendet wird. Er sollte auf die Daten verweisen, die an den Dequeue-Aufruf übergeben werden.  
*BufferSize* \[ in \] Die Größe von *pBuffer* in Bytes.  
*Flags* \[ in \] Ein optionaler Parameter, der das Verhalten dieser Funktion steuert. Das einzige Flag ist SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT. Weitere Informationen finden Sie in den Anmerkungen zu Flush. Wenn kein Flag übergeben wird (*Flags* == 0), wird das standardmäßige Blockierungsverhalten verwendet.  
</dl>

**Rückgabewerte**

Diese Funktion kann DXGI \_ ERROR WAS STILL DRAWING \_ \_ \_ zurückgeben, wenn ein SURFACE QUEUE FLAG \_ DO NOT \_ \_ \_ \_ WAIT-Flag verwendet wird.  
</dl>

**Anmerkungen**

-   Mit dieser Funktion wird die Oberfläche in die Warteschlange gestellt. Wenn die Anwendung SURFACE QUEUE FLAG DO NOT WAIT nicht anordnt, blockiert diese Funktion und führt eine \_ \_ \_ \_ GPU-CPU-Synchronisierung durch, um sicherzustellen, dass das gesamte Rendering auf der in die Warteschlange gestellten Oberfläche \_ abgeschlossen ist. Wenn diese Funktion erfolgreich ist, steht eine Oberfläche für das Aus der Queue zur Verfügung. Wenn Sie nicht blockierende Verhalten wünschen, verwenden Sie das Flag DO \_ NOT \_ WAIT. Weitere Informationen finden Sie unter Flush().
-   Die von Dequeue zurückgegebene Oberfläche ist nach den COM-Verweiszählungsregeln AddRef(), sodass die Anwendung dies nicht tun muss. Nach dem Aufruf von Enqueue muss die Anwendung die Oberfläche wieder frei geben, da sie sie nicht mehr verwendet.

**Leerung**  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



**Parameter**  
*Flags* \[ In\]  
Das einzige Flag ist SURFACE \_ QUEUE FLAG DO NOT \_ \_ \_ \_ WAIT. Siehe Hinweise. *nSurfaces* \[ out \] Gibt die Anzahl der Oberflächen zurück, die noch ausstehen und nicht geleert werden.  
</dl>

**Rückgabewerte**

Diese Funktion kann DXGI \_ ERROR WAS STILL DRAWING \_ \_ \_ zurückgeben, wenn das FLAG SURFACE QUEUE \_ FLAG DO NOT WAIT verwendet \_ \_ \_ \_ wird. Diese Funktion gibt S \_ OK zurück, wenn Oberflächen erfolgreich geleert wurden. Diese Funktion gibt DXGI \_ ERROR WAS STILL DRAWING nur dann \_ \_ \_ zurück, wenn keine Oberflächen geleert wurden. Zusammen geben der Rückgabewert und *nSurfaces* der Anwendung an, welche Arbeit erledigt wurde und ob noch arbeite.  
</dl>

**Anmerkungen**

Leeren ist nur sinnvoll, wenn beim vorherigen Aufruf der Enqueue das Flag DO NOT WAIT verwendet wurde. Andernfalls handelt es sich um \_ \_ ein No-Op-Flag. Wenn beim Enqueue-Aufruf das Flag DO NOT WAIT verwendet wurde, wird die Enqueue sofort zurückgegeben, und die \_ \_ GPU-CPU-Synchronisierung ist nicht garantiert. Die Oberfläche wird weiterhin als in die Queued-Enqueued betrachtet, das erzeugende Gerät kann sie nicht weiter verwenden, kann aber nicht aus der Queue entfernt werden. Um zu versuchen, die Oberfläche für das Aus der Queue zu commiten, muss Flush aufgerufen werden. Beim Leeren wird versucht, einen Commit für alle Oberflächen zu verwenden, die derzeit in die Queued-Enqueued-Enqueued-Enqueuing-Enque Wenn kein Flag an Flush übergeben wird, wird die gesamte Warteschlange blockiert und gelöscht, und alle Oberflächen in der Warteschlange können aus der Warteschlange entfernt werden. Wenn das Flag DO NOT WAIT verwendet wird, überprüft die Warteschlange die Oberflächen, um zu überprüfen, ob eine davon bereit ist. Dieser Schritt ist \_ \_ nicht blockierend. Oberflächen, die die GPU-CPU-Synchronisierung abgeschlossen haben, sind für das Consumergerät bereit. Oberflächen, die noch ausstehend sind, sind nicht betroffen. Die Funktion gibt die Anzahl der Oberflächen zurück, die noch geleert werden müssen.

> [!Note]  
> Leeren unterbricht die Warteschlangensemantik nicht. Die API garantiert, dass oberflächen, die zuerst in die Queued-Synchronisierung ein- und aus der Queued-Synchronisierung entfernt werden, vor der späteren Enqueuing von Oberflächen ausgeführt werden, unabhängig davon, wann die GPU-CPU-Synchronisierung erfolgt.

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a>Direct3D 9Ex und DXGI Interop Helper: How To Use

Wir gehen davon aus, dass die meisten Verwendungsfälle zwei Geräte umfassen, die eine Reihe von Oberflächen gemeinsam nutzen. Da dies auch das einfachste Szenario ist, wird in diesem Dokument erläutert, wie sie die APIs verwenden, um dieses Ziel zu erreichen, eine nicht blockierende Variante erläutert und mit einem kurzen Abschnitt zur Initialisierung für drei Geräte endet.

### <a name="two-devices"></a>Zwei Geräte

Die Beispielanwendung, die dieses Hilfs verwendet, kann Direct3D 9Ex und Direct3D 11 zusammen verwenden. Die Anwendung kann Inhalte mit beiden Geräten verarbeiten und Inhalte mit Direct3D 9 präsentieren. Die Verarbeitung kann das Rendern von Inhalten, das Decodieren von Videos, das Ausführen von Compute-Shadern und so weiter bedeuten. Für jeden Frame wird die Anwendung zuerst mit Direct3D 11, dann mit Direct3D 9 und schließlich mit Direct3D 9 verarbeiten. Darüber hinaus erzeugt die Verarbeitung mit Direct3D 11 einige Metadaten, die von Direct3D 9 verwendet werden müssen. In diesem Abschnitt wird die Verwendung des Hilfsers in drei Teilen behandelt, die dieser Sequenz entsprechen: Initialisierung, Hauptschleife und Bereinigung.

**Initialisierung**  
Die Initialisierung umfasst die folgenden Schritte:  

1.  Initialisieren Sie beide Geräte.
2.  Erstellen Sie die Stammwarteschlange m \_ 11to9Queue.
3.  Klonen aus der Stammwarteschlange: m \_ 9to11Queue.
4.  Rufen Sie OpenProducer/OpenConsumer in beiden Warteschlangen auf.

Die Warteschlangennamen verwenden die Zahlen 9 und 11, um anzugeben, welche API der Producer und welcher der Consumer ist: **m \_**_producer_*_to_*_consumer_*_Queue_*. Entsprechend gibt m 11to9Queue eine Warteschlange an, für die das Direct3D 11-Gerät Oberflächen erzeugt, die das \_ Direct3D 9-Gerät verbraucht. Entsprechend gibt m 9to11Queue eine Warteschlange an, für die Direct3D 9 Oberflächen erzeugt, die \_ Direct3D 11 verbraucht.  
Die Stammwarteschlange ist anfänglich voll, und alle geklonten Warteschlangen sind anfänglich leer. Dies sollte kein Problem für die Anwendung sein, mit Ausnahme des ersten Zyklus der Enqueues und Dequeues und der Verfügbarkeit von Metadaten. Wenn ein Aus der Enqueue nach Metadaten fragt, aber keine festgelegt wurden (entweder weil anfänglich nichts enthalten ist oder die Enqueue nichts festgelegt hat), erkennt das Aus der Enqueue, dass keine Metadaten empfangen wurden.  

1.  **Initialisieren Sie beide Geräte.**  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  **Erstellen Sie die Stammwarteschlange.**  
    In diesem Schritt werden auch die Oberflächen erstellt. Größen- und Formatbeschränkungen sind identisch mit dem Erstellen einer freigegebenen Ressource. Die Größe des Metadatenpuffers wird zur Erstellungszeit festgelegt, und in diesem Fall übergeben wir nur einen UINT.  
    Die Warteschlange muss mit einer festen Anzahl von Oberflächen erstellt werden. Die Leistung variiert je nach Szenario. Die Verwendung mehrerer Oberflächen erhöht die Wahrscheinlichkeit, dass Geräte ausgelastet sind. Wenn beispielsweise nur eine Oberfläche verfügbar ist, gibt es keine Parallelisierung zwischen den beiden Geräten. Andererseits erhöht die Erhöhung der Anzahl von Oberflächen den Speicherbedarf, was die Leistung beeinträchtigen kann. In diesem Beispiel werden zwei Oberflächen verwendet.  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  **Klonen Sie die Stammwarteschlange.**  
    Jede geklonte Warteschlange muss die gleichen Oberflächen verwenden, kann jedoch unterschiedliche Metadatenpuffergrößen und flags haben. In diesem Fall gibt es keine Metadaten von Direct3D 9 zu Direct3D 11.  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  **Öffnen Sie die Producer- und Consumergeräte.**  
    Die Anwendung muss diesen Schritt ausführen, bevor sie Enqueue und Dequeue aufruft. Beim Öffnen eines Producers und Consumers werden Schnittstellen zurückgegeben, die die Enqueue/Dequeue-APIs enthalten.  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

**Main-Schleife**  
Die Verwendung der Warteschlange wird nach dem klassischen Producer/Consumer-Problem modelliert. Stellen Sie sich dies aus Gerätesicht vor. Jedes Gerät muss die folgenden Schritte ausführen: Entfernen aus der Warteschlange, Verarbeiten auf der Oberfläche und anschließendes Einreiten in die Produktionswarteschlange. Für das Direct3D 11-Gerät ist die Verwendung von Direct3D 9 nahezu identisch.  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



**Bereinigen**  
Dieser Schritt ist sehr einfach. Zusätzlich zu den normalen Schritten zum Bereinigen von Direct3D-APIs muss die Anwendung die rückgaben COM-Schnittstellen veröffentlichen.  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a>Nicht blockierende Verwendung

Das vorherige Beispiel ist für einen Multithread-Verwendungsfall sinnvoll, bei dem jedes Gerät über einen eigenen Thread verfügt. Im Beispiel werden die blockierenden Versionen der APIs verwendet: INFINITE für Timeout und kein Flag zum Einsperren in die Enqueue. Wenn Sie das Hilfsfeld auf nicht blockierende Weise verwenden möchten, müssen Sie nur wenige Änderungen vornehmen. In diesem Abschnitt wird die nicht blockierende Verwendung mit beiden Geräten in einem Thread veranschaulicht.

**Initialisierung**  
Die Initialisierung ist mit Ausnahme der Flags identisch. Da die Anwendung singlethreaded ist, verwenden Sie dieses Flag für die Erstellung. Dadurch wird ein Teil des Synchronisierungscodes deaktiviert, wodurch die Leistung möglicherweise verbessert wird.  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



Das Öffnen der Producer- und Consumergeräte ist mit dem im Blockierungsbeispiel identisch.  
**Verwenden der Warteschlange**  
Es gibt viele Möglichkeiten, die Warteschlange auf nicht blockierende Weise mit verschiedenen Leistungsmerkmalen zu verwenden. Das folgende Beispiel ist einfach, hat jedoch aufgrund übermäßiger Spin- und Abrufe eine schlechte Leistung. Trotz dieser Probleme zeigt das Beispiel die Verwendung des Hilfsers. Der Ansatz besteht in der kontinuierlichen Schleife und dem Aussetzen, Verarbeiten, Ein- und Leeren in die Quege. Wenn einer der Schritte fehlschlägt, weil die Ressource nicht verfügbar ist, versucht die Anwendung einfach erneut, die nächste Schleife zu verwenden.  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



Eine komplexere Lösung könnte den Rückgabewert aus der Enqueue und der Leerung überprüfen, um festzustellen, ob eine Leerung erforderlich ist.  
</dl>

### <a name="three-devices"></a>Drei Geräte

Das Erweitern der vorherigen Beispiele auf mehrere Geräte ist einfach. Der folgende Code führt die Initialisierung aus. Nachdem die Producer-/Consumer-Objekte erstellt wurden, ist der Code für deren Verwendung identisch. Dieses Beispiel verfügt über drei Geräte und somit über drei Warteschlangen. Oberflächen fließen von Direct3D 9 zu Direct3D 10 zu Direct3D 11.


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



Wie bereits erwähnt, funktioniert das Klonen auf die gleiche Weise, unabhängig davon, welche Warteschlange geklont wird. Beispielsweise hätte der zweite Clone-Aufruf aus dem m \_ 9to10Queue-Objekt sein können.


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a>Zusammenfassung

Sie können Lösungen erstellen, die Interoperabilität verwenden, um die Leistungsfähigkeit mehrerer DirectX-APIs zu nutzen. Windows Grafik-API-Interoperabilität bietet jetzt eine allgemeine Oberflächenverwaltungslaufzeit DXGI 1.1. Diese Runtime ermöglicht die Unterstützung der synchronisierten Oberflächenfreigabe innerhalb neu entwickelter APIs wie Direct3D 11, Direct3D 10.1 und Direct2D. Interoperabilitätsverbesserungen zwischen neuen APIs und vorhandenen APIs unterstützen die Anwendungsmigration und Abwärtskompatibilität. Direct3D 9Ex- und DXGI 1.1-Consumer-APIs können zusammenarbeiten, wie mit dem Synchronisierungsmechanismus gezeigt, der über Beispiel-Hilfscode im MSDN Code Gallery bereitgestellt wird.

 

 