---
title: Oberflächenfreigabe für Windows Graphics-APIs
description: Dieses Thema bietet eine technische Übersicht über die Interoperabilität mithilfe der Oberflächen Freigabe zwischen Windows-Grafik-APIs, einschließlich Direct3D 11, Direct2D, DirectWrite, Direct3D 10 und Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d889797902c964e603adefc51b25039afca7d46
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730761"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a>Oberflächenfreigabe für Windows Graphics-APIs

Dieses Thema bietet eine technische Übersicht über die Interoperabilität mithilfe der Oberflächen Freigabe zwischen Windows-Grafik-APIs, einschließlich Direct3D 11, Direct2D, DirectWrite, Direct3D 10 und Direct3D 9Ex. Wenn Sie bereits über Kenntnisse dieser APIs verfügen, kann dieses Whitepaper Ihnen helfen, mehrere APIs zu verwenden, um in einer Anwendung, die für die Betriebssysteme Windows 7 oder Windows Vista entwickelt wurde, dieselbe Oberfläche zu erzeugen. Dieses Thema enthält außerdem Richtlinien für bewährte Methoden und Zeiger auf Weitere Ressourcen.

> [!Note]  
> Für Direct2D-und DirectWrite-Interoperabilität in der DirectX 11,1-Laufzeit können Sie [Direct2D-Geräte und-Geräte Kontexte](/windows/desktop/Direct2D/devices-and-device-contexts) verwenden, um direkt auf Direct3D 11-Geräten zu gereinigen.

 

Dieses Thema enthält folgende Abschnitte:

-   [Introduction (Einführung)](#introduction)
-   [Übersicht über API-Interoperabilität](#api-interoperability-overview)
-   [Interoperabilitäts Szenarien](#interoperability-scenarios)
    -   [Direct3D 10,1 Geräte Freigabe mit Direct2D](#direct3d-101-device-sharing-with-direct2d)
    -   [DXGI 1,1 synchronisierte freigegebene Oberflächen](#dxgi-11-synchronized-shared-surfaces)
    -   [Interoperabilität zwischen Direct3D 9Ex und DXGI-basierten APIs](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [Zusammenfassung](#conclusion)

## <a name="introduction"></a>Einführung

In diesem Dokument bezieht sich die Interoperabilität der Windows-Grafik-API auf die gemeinsame Nutzung derselben Renderingoberfläche durch verschiedene APIs. Diese Art von Interoperabilität ermöglicht es Anwendungen, überzeugende Anzeigen durch Nutzung mehrerer Windows-Grafik-APIs zu erstellen und die Migration zu neuen Technologien zu vereinfachen, indem die Kompatibilität mit vorhandenen APIs gewahrt bleibt.

In Windows 7 (und Windows Vista SP2 mit Windows 7 Interop Pack, Vista 7ip) sind die Grafik Rendering-APIs Direct3D 11, Direct2D, Direct3D 10,1, Direct3D 10,0, Direct3D 9Ex, Direct3D 9c und frühere Direct3D-APIs sowie GDI und GDI+. Windows Imaging Component (WIC) und DirectWrite sind verwandte Technologien für die Bildverarbeitung, und Direct2D führt Text Rendering aus. Die DirectX-Videobeschleunigung-API (DXVA), die auf Direct3D 9c und Direct3D 9Ex basiert, wird für die Video Verarbeitung verwendet.

Da sich Windows-Grafik-APIs in Bezug auf Direct3D entwickeln, investiert Microsoft mehr Aufwand, um Interoperabilität über APIs hinweg zu gewährleisten. Neu entwickelte Direct3D-APIs und APIs auf höherer Ebene, die auf Direct3D-APIs basieren, bieten auch Unterstützung für die Überbrückung der Kompatibilität mit älteren APIs. Zur Veranschaulichung können Direct2D-Anwendungen Direct3D 10,1 verwenden, indem Sie ein Direct3D 10,1-Gerät freigeben. Außerdem können die APIs Direct3D 11, Direct2D und Direct3D 10,1 die DirectX Graphics Infrastructure (DXGI) 1,1 nutzen, wodurch synchronisierte freigegebene Oberflächen aktiviert werden, die die Interoperabilität zwischen diesen APIs vollständig unterstützen. DXGI 1,1-basierte APIs interagieren mit GDI und mit GDI+ by Association, indem Sie den GDI-Gerätekontext von einer DXGI 1,1-Oberfläche abrufen. Weitere Informationen finden Sie in der DXGI-und GDI-Interoperabilitäts Dokumentation auf MSDN.

Nicht synchronisierte Oberflächen Freigabe wird von der Direct3D 9Ex-Laufzeit unterstützt. Auf DXVA basierende Videoanwendungen können das Direct3D 9Ex-und DXGI-Interoperabilitäts Hilfsprogramm für die Direct3D 9Ex-basierte DXVA-Interoperabilität mit Direct3D 11 für den Compute-Shader verwenden, oder Sie können mit Direct2D für 2D-Steuerelemente oder Text Rendering interagieren. WIC und DirectWrite interagieren auch mit GDI, Direct2D und by Association, anderen Direct3D-APIs.

Direct3D 10,0, Direct3D 9c und ältere Direct3D-Laufzeiten unterstützen keine freigegebenen Oberflächen. System Speicher Kopien werden weiterhin für die Interoperabilität mit GDI-oder DXGI-basierten APIs verwendet.

Beachten Sie, dass die Interoperabilitäts Szenarien in diesem Dokument auf mehrere Grafiken-APIs verweisen, die auf eine freigegebene Renderingoberfläche und nicht auf das gleiche Anwendungsfenster rendern. Die Synchronisierung für separate APIs, die auf verschiedene Oberflächen abzielen, die anschließend in das gleiche Fenster zusammengesetzt werden, liegt außerhalb des Umfangs dieses Papiers.

## <a name="api-interoperability-overview"></a>Übersicht über API-Interoperabilität

Die Interoperabilität der Oberflächen Freigabe von Windows-Grafik-APIs kann in Bezug auf API-zu-API-Szenarien und die entsprechenden Interoperabilitäts Funktionen beschrieben werden. Ab Windows 7 und ab Windows Vista SP2 mit 7ip enthalten neue APIs und zugehörige Laufzeiten Direct2D und verwandte Technologien: Direct3D 11 und DXGI 1,1. Die GDI-Leistung wurde in Windows 7 ebenfalls verbessert. Direct3D 10,1 wurde in Windows Vista SP1 eingeführt. Das folgende Diagramm zeigt die Interoperabilitäts Unterstützung zwischen APIs.

![Diagramm der Interoperabilitäts Unterstützung zwischen Windows-Grafik-APIs](images/surface-sharing-interoperability.png)

In diesem Diagramm zeigen Pfeile Interoperabilitäts Szenarien, in denen die verbundenen APIs auf die gleiche Oberfläche zugreifen können. Blaue Pfeile weisen auf die in Windows Vista eingeführten Interoperabilitäts Mechanismen hin. Grüne Pfeile zeigen die Interoperabilitäts Unterstützung für neue APIs oder Verbesserungen an, die älteren APIs helfen, mit neueren APIs zu interagieren. Grüne Pfeile stellen z. b. die Geräte Freigabe, synchronisierte Shared Surface-Unterstützung, Direct3D 9Ex/DXGI-Synchronisierungs Hilfe und das Abrufen eines GDI-Geräte Kontexts von einer kompatiblen Oberfläche dar.

## <a name="interoperability-scenarios"></a>Interoperabilitäts Szenarien

Ab Windows 7 und Windows Vista 7ip unterstützen die gängigen Angebote von Windows-Grafik-APIs das Rendering mehrerer APIs zur gleichen DXGI 1,1-Oberfläche.

**Direct3D 11, Direct3D 10,1, Direct2D – Interoperabilität untereinander**

Direct3D 11-, Direct3D 10,1-und Direct2D-APIs (und die zugehörigen APIs wie DirectWrite und WIC) können miteinander interagieren, indem Sie entweder die Freigabe von Direct3D 10,1-Geräten oder synchronisierte freigegebene Oberflächen verwenden.

### <a name="direct3d-101-device-sharing-with-direct2d"></a>Direct3D 10,1 Geräte Freigabe mit Direct2D

Die Geräte Freigabe zwischen Direct2D und Direct3D 10,1 ermöglicht es einer Anwendung, beide APIs zu verwenden, um nahtlos und effizient auf derselben DXGI 1,1-Oberfläche zu renderarbeiten, wobei dasselbe zugrunde liegende Direct3D-Geräte Objekt verwendet wird. Direct2D bietet die Möglichkeit, Direct2D-APIs über ein vorhandenes Direct3D 10,1-Gerät aufzurufen. dabei wird die Tatsache genutzt, dass Direct2D auf Direct3D 10,1-und DXGI 1,1-Laufzeiten aufbaut. Die folgenden Code Ausschnitte veranschaulichen, wie Direct2D das Direct3D 10,1 Device-Renderziel von einer DXGI 1,1-Oberfläche erhält, die dem Gerät zugeordnet ist. Das Direct3D 10,1-geräterrenderziel kann Direct2D-Zeichnungs Aufrufe zwischen beginDraw-und EndDraw-APIs ausführen.


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

-   Das zugehörige Direct3D 10,1-Gerät muss das BGRA-Format unterstützen. Dieses Gerät wurde durch Aufrufen von D3D10CreateDevice1 mit dem Parameter \_ d3d10 \_ \_ BGRA- \_ Unterstützung für das Gerät erstellt. Das BGRA-Format wird ab Direct3D 10-Featureebene 9,1 unterstützt.
-   Die Anwendung sollte nicht mehrere ID2D1RenderTargets erstellen, die demselben Direct3D 10.1-Gerät zugeordnet ist.
-   Um eine optimale Leistung zu erzielen, sollten Sie mindestens eine Ressource jederzeit herum aufbewahren, z. b. Texturen oder Oberflächen, die dem Gerät zugeordnet sind.

Die Geräte Freigabe eignet sich für die Prozess interne, Single Thread-Verwendung eines renderinggeräts, das von den Direct3D 10,1-und Direct2D-Rendering-APIs gemeinsam genutzt wird. Synchronisierte freigegebene Oberflächen ermöglichen Multithread-, Prozess interne und prozessübergreifende Verwendung mehrerer renderinggeräte, die von Direct3D 10,1-, Direct2D-und Direct3D 11-APIs verwendet werden.

Eine weitere Methode der Direct3D 10,1-und Direct2D-Interoperabilität ist die Verwendung von ID3D1RenderTarget:: foatesharedbitmap, die ein ID2D1Bitmap-Objekt aus idxgisurface erstellt. Sie können eine Direct3D 10.1-Szene in die Bitmap schreiben und Sie mit Direct2D Rendering. Weitere Informationen finden Sie unter [ID2D1RenderTarget:: kreatesharedbitmap-Methode](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).

### <a name="direct2d-software-rasterization"></a>Direct2D Software rasterization

Die Geräte Freigabe mit Direct3D 10,1 wird nicht unterstützt, wenn der Software-Renderer Direct2D verwendet wird, z. b. durch Angeben von D2D1 \_ \_ \_ \_ Renderziel-Verwendungs Erzwingen von \_ Software \_ Rendering in D2D1 \_ renderzielverwendung \_ \_ beim Erstellen eines Direct2D Renderziels.

Direct2D kann das WARP10 Software Raster verwenden, um das Gerät für Direct3D 10 oder Direct3D 11 freizugeben, aber die Leistung sinkt erheblich.

### <a name="dxgi-11-synchronized-shared-surfaces"></a>DXGI 1,1 synchronisierte freigegebene Oberflächen

Direct3D 11, Direct3D 10,1-und Direct2D-APIs verwenden alle DXGI 1,1, das die Funktionalität zum Synchronisieren von Lese-und Schreib vorlese-und Schreib vorschreiben auf derselben Grafikspeicher Oberfläche (DXGISurface1) durch mindestens zwei Direct3D-Geräte bietet. Die renderinggeräte mit synchronisierten freigegebenen Oberflächen können Direct3D 10,1-oder Direct3D 11-Geräte sein, die jeweils in demselben Prozess oder prozessübergreifenden Prozess ausgeführt werden.

Anwendungen können synchronisierte freigegebene Oberflächen verwenden, um zwischen allen DXGI 1,1-basierten Geräten, z. b. Direct3D 11 und Direct3D 10,1, oder zwischen Direct3D 11 und Direct2D zu interagieren, indem das Direct3D 10,1-Gerät vom Direct2D-Renderziel Objekt erhalten wird.

Stellen Sie in den APIs Direct3D 10,1 und höher für die Verwendung von DXGI 1,1 sicher, dass das Direct3D-Gerät mithilfe eines DXGI 1,1-Adapter Objekts erstellt wird, das aus dem DXGI 1,1 Factory-Objekt aufgeführt wird. Rufen Sie CreateDXGIFactory1 auf, um das IDXGIFactory1-Objekt zu erstellen, und EnumAdapters1, um das IDXGIAdapter1-Objekt aufzulisten. Das IDXGIAdapter1-Objekt muss als Teil des D3D10CreateDevice-oder D3D10CreateDeviceAndSwapChain-Aufrufes aufgerufen werden. Weitere Informationen zu DXGI 1,1-APIs finden Sie im [Programmier Handbuch für DXGI](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).

### <a name="apis"></a>APIs

**D3d10 \_ \_ ressourcenmisc \_ Shared \_ keyedmutex**  
Wenn Sie die synchronisierte freigegebene Ressource erstellen, legen Sie d3d10 \_ Resource \_ misc \_ Shared \_ keyedmutex in das \_ Flag d3d10 Resource \_ misc fest \_ .  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



**D3d10 \_ \_ ressourcenmisc \_ Shared \_ keyedmutex**  
Ermöglicht die Synchronisierung der erstellten Ressource mithilfe der idxgikeyedmutex:: acquiresync-und releasesync-APIs. Die folgende Ressourcen Erstellung Direct3D 10,1-APIs, die alle einen d3d10- \_ ressourcenmisc-Flag-Parameter annehmen, wurden \_ \_ erweitert, um das neue Flag zu unterstützen.  

-   ID3D10Device1::CreateTexture1D
-   ID3D10Device1::CreateTexture2D
-   ID3D10Device1::CreateTexture3D
-   ID3D10Device1:: up Buffer

  
Wenn eine der aufgelisteten Funktionen mit dem "d3d10 \_ Resource \_ misc \_ Shared \_ keyedmutex"-Flag aufgerufen wird, kann die zurückgegebene Schnittstelle für eine idxgikeyedmutex-Schnittstelle abgefragt werden, die die acquiresync-und releasesync-APIs implementiert, um den Zugriff auf die-Oberfläche zu synchronisieren. Das Gerät, das die Oberfläche erstellt, und alle anderen Geräte, die die Oberfläche öffnen (mit opensharedresource), müssen idxgikeyedmutex:: acquiresync aufrufen, bevor alle renderingbefehle auf der Oberfläche ausgeführt werden, und idxgikeyedmutex:: releasesync beim Rendering.  
Von Warp-und ref-Geräten werden keine freigegebenen Ressourcen unterstützt. Wenn Sie versuchen, eine Ressource mit diesem Flag entweder auf einem Warp-oder ref-Gerät zu erstellen, gibt die Create-Methode einen E \_ outo fmemory-Fehlercode zurück.  
**idxgikeyedmutex-Schnittstelle**  
Eine neue Schnittstelle in DXGI 1,1, idxgikeyedmutex, stellt einen Schlüssel gebundenen Mutex dar, der exklusiven Zugriff auf eine freigegebene Ressource ermöglicht, die von mehreren Geräten verwendet wird. Eine Referenz Dokumentation zu dieser Schnittstelle und den beiden Methoden acquiresync und releasesync finden Sie unter [idxgikeyedmutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a>Beispiel: synchronisierte Oberflächen Freigabe zwischen zwei Direct3D 10,1-Geräten

Im folgenden Beispiel wird die gemeinsame Nutzung einer Oberfläche zwischen zwei Direct3D 10,1-Geräten veranschaulicht. Die synchronisierte freigegebene Oberfläche wird von einem Direct3D 10.1-Gerät erstellt.


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



Das gleiche Direct3D 10.1-Gerät kann die synchronisierte freigegebene Oberfläche für das Rendering abrufen, indem es acquiresync aufrufen und dann die Oberfläche für das Rendering des anderen Geräts durch Aufrufen von releasesync freigibt. Wenn Sie die synchronisierte freigegebene Oberfläche nicht mit einem anderen Direct3D-Gerät freigeben, kann der Ersteller die synchronisierte freigegebene Oberfläche (zum Starten und Beenden des Renderings) abrufen und freigeben, indem er den gleichen Schlüsselwert verwendet.


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



Das zweite Direct3D 10.1-Gerät kann die synchronisierte freigegebene Oberfläche für das Rendering abrufen, indem es acquiresync aufrufen und dann die Oberfläche für das erste Rendern des Geräts durch Aufrufen von releasesync freigibt. Beachten Sie, dass Gerät 2 die synchronisierte freigegebene Oberfläche mithilfe desselben Schlüssel Werts abrufen kann, der im releasesync-Aufruf von Gerät 1 angegeben wurde.


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



Weitere Geräte, die dieselbe Oberfläche gemeinsam nutzen, können die Oberfläche mithilfe zusätzlicher Schlüssel abrufen und freigeben, wie in den folgenden Aufrufen gezeigt.


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



Beachten Sie, dass eine reale Anwendung immer auf eine zwischen Oberfläche renderierender ist, die dann auf die freigegebene Oberfläche kopiert wird, um zu verhindern, dass ein Gerät auf ein anderes Gerät wartet, das die Oberfläche nutzt

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a>Verwenden von synchronisierten freigegebenen Oberflächen mit Direct2D und Direct3D 11

Ebenso kann für die gemeinsame Nutzung zwischen Direct3D 11-und Direct3D 10,1-APIs eine synchronisierte freigegebene Oberfläche entweder von API-Geräten aus erstellt und für die anderen API-Geräte, in oder außerhalb des Prozesses, freigegeben werden.

Anwendungen, die Direct2D verwenden, können ein Direct3D 10,1-Gerät freigeben und eine synchronisierte freigegebene Oberfläche verwenden, um mit Direct3D 11 oder anderen Direct3D 10,1-Geräten zusammenzuarbeiten, unabhängig davon, ob Sie zum gleichen Prozess oder zu unterschiedlichen Prozessen gehören. Für Single-Process-Anwendungen mit nur einem Thread ist die Geräte Freigabe jedoch die leistungsfähigsten und effizientesten Interoperabilitäts Methode zwischen Direct2D und Direct3D 10 oder Direct3D 11.

### <a name="software-rasterizer"></a>Software-Rasterizer

Synchronisierte freigegebene Oberflächen werden nicht unterstützt, wenn Anwendungen die Direct3D-oder Direct2D-Software-Raster verwenden, einschließlich des verweisrasterizers und des Warp, anstelle der Hardwarebeschleunigung.

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a>Interoperabilität zwischen Direct3D 9Ex und DXGI-basierten APIs

Die Direct3D 9Ex-APIs enthielten das Konzept der Oberflächen Freigabe, damit andere APIs von der freigegebenen Oberfläche lesen können. Um Lese-und Schreibvorgänge für eine freigegebene Direct3D 9Ex-Oberfläche zu verwenden, müssen Sie der Anwendung selbst eine manuelle Synchronisierung hinzufügen.

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a>Direct3D 9Ex Shared-Oberflächen Plus Manuelles Synchronisieren-Hilfsprogramm

Die grundlegendste Aufgabe bei der Interoperabilität von Direct3D 9Ex und Direct3D 10 oder 11 besteht darin, eine einzige Oberfläche vom ersten Gerät (Gerät a) an das zweite Gerät (Gerät b) zu übergeben, sodass das Rendering von Gerät a vollständig abgeschlossen ist. Daher kann Gerät B diese Oberfläche ohne Sorgen nutzen. Diese Vorgehensweise ähnelt dem klassischen Producer-Consumer-Problem, und dieses Problem wird auf diese Weise modelliert. Das erste Gerät, das die-Oberfläche verwendet und dann aufgibt, ist der Producer (Gerät A), und das Gerät, das anfänglich wartet, ist der Consumer (Gerät B). Alle realen Anwendungen sind komplexer als dies, und Sie verketten mehrere Producer-Consumer-Bausteine, um die gewünschte Funktionalität zu erzielen.

Die Producer-Consumer-Bausteine werden mithilfe einer Warteschlange von Oberflächen in das Hilfsprogramm implementiert. Oberflächen werden vom Producer in die Warteschlange eingereiht und vom Consumer aus der Warteschlange entfernt. Das Hilfsprogramm führt drei COM-Schnittstellen ein: isurfacequeue, isurfaceproducer und isurfaceconsumer.

### <a name="high-level-overview-of-helper"></a>High-Level Übersicht über das Hilfsprogramm

Das isurfakequeue-Objekt ist der Baustein für die Verwendung der freigegebenen Oberflächen. Es wird mit einem initialisierten Direct3D-Gerät und einer Beschreibung erstellt, um eine Fixed-Anzahl von freigegebenen Oberflächen zu erstellen. Das Queue-Objekt verwaltet die Erstellung von Ressourcen und das Öffnen von Code. Anzahl und Typ der Oberflächen werden korrigiert. Nachdem die Oberflächen erstellt wurden, kann Sie von der Anwendung nicht mehr hinzugefügt oder entfernt werden.

Jede Instanz des isurfakequeue-Objekts stellt eine unidirektionale Straße dar, die zum Senden von Oberflächen vom produzierenden Gerät an das verarbeitende Gerät verwendet werden kann. Mehrere unidirektionale Straßen können verwendet werden, um Oberflächen Freigabe Szenarien zwischen Geräten spezifischer Anwendungen zu ermöglichen.

**Erstellung/Objekt Lebensdauer**  
Es gibt zwei Möglichkeiten, das Warteschlangen Objekt zu erstellen: über "kreatesurfacequeue" oder über die Klon Methode von isurfacequeue. Da es sich bei den Schnittstellen um COM-Objekte handelt, gilt die Standard Verwaltung von com  
**Producer/Consumer-Modell**  
Enqueue (): der Producer ruft diese Funktion auf, um anzugeben, dass Sie mit der-Oberfläche abgeschlossen ist, die jetzt für ein anderes Gerät verfügbar sein kann. Nach dem Zurückgeben dieser Funktion hat das Producer-Gerät keine Rechte mehr auf die Oberfläche, und es ist unsicher, Sie weiterhin zu verwenden.  
Dequeue (): das verarbeitende Gerät ruft diese Funktion auf, um eine freigegebene Oberfläche zu erhalten. Die API stellt sicher, dass alle aus der Warteschlange eingereihten Oberflächen zur Verwendung bereit sind.  
**Metadaten**  
Die API unterstützt das Zuordnen von Metadaten zu den freigegebenen Oberflächen.  
In der Warteschlange () haben Sie die Möglichkeit, zusätzliche Metadaten anzugeben, die an das verarbeitende Gerät weitergeleitet werden. Die Metadaten müssen kleiner als der zum Erstellungs Zeitpunkt bekannte Höchstwert sein.  
Aus Queue () kann optional ein Puffer und ein Zeiger auf die Größe des Puffers übergeben werden. Die Warteschlange füllt den Puffer mit den Metadaten aus dem entsprechenden aufrufeschlangenbefehl.  
**Klonen?**  
Jedes isurfakequeue-Objekt löst eine unidirektionale Synchronisierung. Wir gehen davon aus, dass die große Mehrheit der Anwendungen, die diese API verwenden, ein geschlossenes System verwenden wird. Das einfachste geschlossene System mit zwei Geräten, die die Oberflächen hin-und Hersenden, erfordert zwei Warteschlangen. Das isurfacequeue-Objekt verfügt über eine Clone ()-Methode, um das Erstellen mehrerer Warteschlangen zu ermöglichen, die alle Teil derselben größeren Pipeline sind.  
Klon erstellt ein neues isurfakequeue-Objekt aus einem vorhandenen Objekt und teilt alle geöffneten Ressourcen auf. Das resultierende-Objekt verfügt über genau die gleichen Oberflächen wie die Quell Warteschlange. Geklonte Warteschlangen können über unterschiedliche metadatengrößen verfügen.  
**Surface**  
Isurfakequeue übernimmt die Verantwortung für das Erstellen und Verwalten seiner Oberflächen. Es ist nicht zulässig, beliebige Oberflächen in die Warteschlange zu stellen. Außerdem sollte eine Oberfläche nur über einen aktiven "Besitzer" verfügen. Er sollte sich entweder in einer bestimmten Warteschlange befinden oder von einem bestimmten Gerät verwendet werden. Es ist nicht zulässig, es in mehreren Warteschlangen zu verwenden, oder die Oberfläche kann von Geräten weiterhin verwendet werden, nachdem Sie in die Warteschlange eingereiht wurde.  
</dl>

### <a name="api-details"></a>API-Details

### <a name="isurfacequeue"></a>Isurfakequeue

Die Warteschlange ist für das Erstellen und Verwalten der freigegebenen Ressourcen zuständig. Außerdem bietet es die Funktionalität zum Verketten mehrerer Warteschlangen mithilfe von Klonen. Die Warteschlange verfügt über Methoden, die das erbende Gerät und ein consumergerät öffnen. Es kann immer nur jeweils einer der beiden geöffnet werden.

Die Warteschlange stellt die folgenden APIs bereit:



|                             |                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------|
| "Kreatesurfakequeue"          | Erstellt ein isurfakequeue-Objekt (die Stamm Warteschlange).                              |
| Isurfakequeue:: openconsumer | Gibt eine Schnittstelle für das zu entmittelende Gerät zurück.                        |
| Isurfakequeue:: openproducer | Gibt eine Schnittstelle für das herzustellende Gerät in die Warteschlange zurück                        |
| Isurfakequeue:: Clone        | Erstellt ein isurfakequeue-Objekt, das Oberflächen mit dem Stamm Warteschlangen Objekt freigibt. |



 

**"Kreatesurfakequeue"**  


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

**Breite**, **Höhe**  der Dimensionen der freigegebenen Oberflächen. Alle freigegebenen Oberflächen müssen die gleichen Dimensionen aufweisen.  
**Format** Das Format der freigegebenen Oberflächen. Alle freigegebenen Oberflächen müssen das gleiche Format aufweisen. Die gültigen Formate sind abhängig von den Geräten, die verwendet werden, da verschiedene Geräte Paare verschiedene Format Typen gemeinsam nutzen können.  
**Numoberflächen**  Die Anzahl der Oberflächen, die Teil der Warteschlange sind. Dies ist eine Fixed-Nummer.  
 **MetaDataSize**  Die maximale Größe des metadatenpuffers.  
**Flags**  Flags zum Steuern des Verhaltens der Warteschlange. Siehe Hinweise.  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parameter**

 *PDE SC* \[ in \]  der Beschreibung der zu erstellenden freigegebenen Oberflächen Warteschlange.  

 *pdevice* \[ auf \]  dem Gerät, das zum Erstellen der freigegebenen Oberflächen verwendet werden soll. Dies ist ein expliziter Parameter aufgrund eines Features in Windows Vista. Für Oberflächen, die von Direct3D 9 und Direct3D 10 gemeinsam genutzt werden, müssen die Oberflächen mit Direct3D 9 erstellt werden.  

 *ppqueue* \[ Out \]  bei der Rückgabe enthält einen Zeiger auf das isurfakequeue-Objekt.  


**Rückgabewerte**

Wenn *pdevice* Ressourcen nicht freigeben kann, gibt diese Funktion einen ungültigen DXGI- \_ Fehler zurück \_ \_ . Diese Funktion erstellt die Ressourcen. Wenn ein Fehler auftritt, wird ein Fehler zurückgegeben. Wenn der Vorgang erfolgreich ist, wird S OK zurückgegeben \_ .

**Anmerkungen**

Beim Erstellen des Warteschlangen Objekts werden auch alle-Oberflächen erstellt. Bei allen Oberflächen handelt es sich um 2D-Renderziele. Sie werden mit den \_ \_ \_ Ressourcenflags d3d10 BIND-Renderziel und d3d10 \_ Bind- \_ Shader erstellt \_ (oder die entsprechenden Flags für die unterschiedlichen Laufzeiten).

Der Entwickler kann ein Flag angeben, das angibt, ob mehrere Threads auf die Warteschlange zugreifen werden. Wenn keine Flags festgelegt sind (**Flags** = = 0), wird die Warteschlange von mehreren Threads verwendet. Der Entwickler kann einen Single Thread-Zugriff angeben, der den Synchronisierungs Code deaktiviert und eine Leistungsverbesserung für diese Fälle bietet. Jede geklonte Warteschlange verfügt über ein eigenes Flag, daher ist es möglich, dass für unterschiedliche Warteschlangen im System verschiedene Synchronisierungs Steuerungen vorhanden sind.

 **Einen Producer öffnen**  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



**Parameter**  

*pdevice* \[ in\]  

Das Producer-Gerät, das in die Warteschlange für die Warteschlange eingereiht wird. 

*ppproducer* \[ Out \] gibt ein Objekt an die Producer-Schnittstelle zurück.  


**Rückgabewerte**

Wenn das Gerät keine Oberflächen freigeben kann, wird der ungültige DXGI-Fehler zurückgegeben \_ \_ \_ .

**Einen Consumer öffnen**  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



**Parameter**  
 *pdevice* \[ in\]  
 Das consumergerät, das die Oberfläche aus der Warteschlange entfernt. 
 *ppconsumer* \[ Out \]  gibt ein Objekt an die consumerschnittstelle zurück.  


**Rückgabewerte**

Wenn das Gerät keine Oberflächen freigeben kann, wird der ungültige DXGI-Fehler zurückgegeben \_ \_ \_ .

**Anmerkungen**

Diese Funktion öffnet alle Oberflächen in der Warteschlange für das Eingabegerät und speichert Sie zwischen. Nachfolgende Aufrufe von Dequeue werden einfach in den Cache übergegangen und müssen die Oberflächen nicht jedes Mal erneut öffnen.



### <a name="cloning-an-idxgixsurfacequeue"></a>Klonen eines idxgixsurfakequeue




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



 Member **MetaDataSize** und **Flags** haben das gleiche Verhalten wie bei "kreatesurfagequeue".  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Parameter**

*PDE SC* \[ in \] einer Struktur, die eine Beschreibung des zu erstellenden Klon Objekts bereitstellt. Dieser Parameter muss initialisiert werden.  
*ppqueue* \[ Out \] gibt das initialisierte Objekt zurück.  
</dl>

**Anmerkungen**

Sie können aus jedem vorhandenen Warteschlangen Objekt klonen, auch wenn es nicht der Stamm ist.  
</dl>

### <a name="idxgixsurfaceconsumer"></a>Idxgixsurfakeconsumer

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
*ID* \[ in\]  
Die refi-ID einer 2D-Oberfläche des nutzenden Geräts.  

-   Bei einem IDirect3DDevice9 muss die refi-ID \_ \_ uuidof (IDirect3DTexture9) sein.
-   Bei einem ID3D10Device muss die refi-ID \_ \_ uuidof (ID3D10Texture2D) sein.
-   Bei einem ID3D11Device muss die refi-ID \_ \_ uuidof (ID3D11Texture2D) sein.

*ppsurface* \[ Out \] gibt einen Zeiger auf die-Oberfläche zurück.  
*pbuffer* \[ in, out \] ein optionaler Parameter, und wenn not **null** ist, enthält bei der Rückgabe die Metadaten, die an den entsprechenden aufruteschlangen-Befehl übergeben wurden.  
*pbuffersize* \[ in \] die Größe von *pbuffer* in Bytes. Gibt die Anzahl von Bytes zurück, die in *pbuffer* zurückgegeben werden. Wenn der einreihen-Rückruf keine Metadaten bereitstellt, wird *pbuffer* auf 0 festgelegt.  
*dwtimeout* \[ in \] gibt einen Timeout Wert an. Weitere Details finden Sie in den hinweisen.  
</dl>

**Rückgabewerte**

Diese Funktion kann das Timeout Timeout zurückgeben, \_ Wenn ein Timeout Wert angegeben wird und die Funktion nicht vor dem Timeout Wert zurückgegeben wird. Siehe Hinweise. Wenn keine Oberflächen verfügbar sind, gibt die Funktion zurück, wobei *ppsurface* auf **null**, *pbuffersize* auf 0 und der Rückgabewert 0x80070120 (Win32 \_ zu \_ HRESULT (Wartezeit \_ Timeout)) festgelegt ist.  
</dl>

**Anmerkungen**

Diese API kann blockieren, wenn die Warteschlange leer ist. Der Parameter " *dwtimeout* " funktioniert identisch mit den Windows-Synchronisierungs-APIs, z. b. "WaitForSingleObject". Verwenden Sie für ein nicht blockierendes Verhalten einen Timeout Wert von 0.  
</dl>

### <a name="isurfaceproducer"></a>Isurfaceproducer

Diese Schnittstelle bietet zwei Methoden, mit denen die APP Oberflächen in die Warteschlange eingereiht. Nachdem eine Oberfläche in die Warteschlange eingereiht wurde, ist der Surface-Zeiger nicht mehr gültig und kann nicht sicher verwendet werden. Die einzige Aktion, die die Anwendung mit dem Zeiger ausführen sollte, besteht darin, Sie freizugeben.



|                           |                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Isurfaceproducer:: Einreihen in Warteschlange | Fügt eine Oberfläche in die Warteschlange des Warteschlangen Objekts ein. Nachdem dieser Vorgang abgeschlossen wurde, erfolgt der Producer mit der Oberfläche, und die Oberfläche ist für ein anderes Gerät bereit. |
| Isurfaceproducer:: Flush   | Wird verwendet, wenn die Anwendungen nicht blockierende Verhalten aufweisen sollten. Einzelheiten finden Sie in den Hinweisen.                                                                  |



 

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
*pSurface* \[ in\]  
Die Oberfläche des produzierenden Geräts, das in die Warteschlange eingereiht werden muss. Dabei muss es sich um eine aus der Warteschlange entfernte Oberfläche aus demselben Warteschlangen Netzwerk handeln. *pbuffer* \[ in \] einem optionalen Parameter, der verwendet wird, um Metadaten zu übergeben. Er sollte auf die Daten zeigen, die an den Befehl zum Entfernen aus der Warteschlange weitergegeben werden.  
*BufferSize* \[ in \] der Größe von *pbuffer*(in Bytes).  
*Flags* \[ in \] einem optionalen Parameter, der das Verhalten dieser Funktion steuert. Das einzige Flag ist das Surface \_ Queue- \_ Flag \_ \_ nicht \_ warten. Weitere Informationen finden Sie in den Hinweisen zum leeren. Wenn kein Flag (*Flags* = = 0) überschritten wird, wird das standardmäßige Blockierungs Verhalten verwendet.  
</dl>

**Rückgabewerte**

Diese Funktion kann den DXGI-Fehler zurückgeben, \_ \_ Wenn das \_ \_ \_ Flag für die nicht Wartezeit der Surface-Warteschlange \_ \_ \_ \_ verwendet wird.  
</dl>

**Anmerkungen**

-   Diese Funktion setzt die-Oberfläche in die Warteschlange. Wenn die Anwendung kein Surface \_ Queue \_ -Flag angibt \_ \_ \_ , wird diese Funktion blockiert und führt eine GPU-CPU-Synchronisierung durch, um sicherzustellen, dass das gesamte Rendering auf der in die Warteschlange eingereihten Oberfläche vollständig ist. Wenn diese Funktion erfolgreich ausgeführt wird, steht eine Oberfläche zum Entfernen aus der Warteschlange zur Verfügung. Wenn Sie ein nicht blockierendes Verhalten wünschen, verwenden Sie das \_ \_ Flag nicht warten. Weitere Informationen finden Sie unter Flush ().
-   Gemäß den Regeln für die COM-Verweis Zählung wird die von "toqueue" zurückgegebene Oberfläche "adressf ()" verwendet, damit die Anwendung dies nicht tun muss. Nach dem Aufrufen von Enqueue muss die Anwendung die Oberfläche freigeben, da Sie Sie nicht mehr verwenden.

**Leerung**  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



**Parameter**  
*Flags* \[in\]  
Das einzige Flag ist das Surface \_ Queue- \_ Flag \_ \_ nicht \_ warten. Siehe Hinweise. *noberflächen* \[ Out \] gibt die Anzahl der Oberflächen zurück, die noch ausstehend sind und nicht geleert werden.  
</dl>

**Rückgabewerte**

Diese Funktion kann den DXGI-Fehler zurückgeben, \_ \_ \_ \_ Wenn das Flag für die Surface- \_ Warteschlange \_ \_ \_ nicht \_ gewartet wird. Diese Funktion gibt S \_ OK zurück, wenn beliebige Oberflächen erfolgreich geleert wurden. Diese Funktion gibt den DXGI-Fehler zurück, der \_ \_ \_ nur gezeichnet wurde, \_ Wenn keine Oberflächen geleert wurden. Zusammen geben der Rückgabewert und die *Oberflächen* für die Anwendung an, welche Arbeit durchgeführt wurde und ob eine beliebige Arbeit zu erledigen ist.  
</dl>

**Anmerkungen**

Der Löschvorgang ist nur sinnvoll, wenn der vorherige aufrubungsvorgang das Flag "nicht warten" verwendet \_ \_ hat, andernfalls ist es ein No-op. Wenn der aufzurufende aufrubungsvorgang das \_ \_ Flag nicht warten verwendet hat, wird der einreihen-Vorgang sofort zurückgegeben, und die GPU-CPU-Synchronisierung Die Oberfläche wird weiterhin in die Warteschlange eingereiht, das ermittelende Gerät kann Sie jedoch nicht mehr verwenden, ist aber nicht zum Entfernen aus der Warteschlange verfügbar. Um zu versuchen, ein Commit für die-Oberfläche zum Entfernen aus der Warteschlange auszuführen, muss Flush aufgerufen werden. "Flush" versucht, alle Oberflächen zu übertragen, die gerade in die Warteschlange eingereiht werden. Wenn kein Flag an Flush weitergegeben wird, wird die gesamte Warteschlange blockiert und gelöscht, und alle darin ausgefallenen Oberflächen werden zum Entfernen aus der Warteschlange gelöscht. Wenn das \_ Flag nicht \_ warten verwendet wird, überprüft die Warteschlange die Oberflächen, um festzustellen, ob Sie bereit sind. dieser Schritt ist nicht blockierend. Oberflächen, die die GPU-CPU-Synchronisierung abgeschlossen haben, sind für das consumergerät bereit. Noch ausstehende Oberflächen sind nicht betroffen. Die-Funktion gibt die Anzahl der Oberflächen zurück, die noch geleert werden müssen.

> [!Note]  
> Das leeren führt nicht zu einer Unterbrechung der Warteschlangen Semantik. Die API stellt sicher, dass für in die Warteschlange eingereihte Oberflächen zuerst ein Commit ausgeführt wird, bevor die Oberflächen später in die Warteschlange eingereiht werden.

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a>Direct3D 9Ex und DXGI Interop Helper: Verwendung

Wir gehen davon aus, dass die meisten Verwendungs Fälle zwei Geräte umfassen, die eine Reihe von Oberflächen gemeinsam nutzen. Da dies auch das einfachste Szenario ist, wird in diesem Dokument ausführlich erläutert, wie die APIs verwendet werden, um dieses Ziel zu erreichen, eine nicht blockierende Variation erläutert und mit einem kurzen Abschnitt über die Initialisierung von drei Geräten endet.

### <a name="two-devices"></a>Zwei Geräte

Die Beispielanwendung, die dieses Hilfsprogramm verwendet, kann Direct3D 9Ex und Direct3D 11 gleichzeitig verwenden. Die Anwendung kann Inhalte mit beiden Geräten verarbeiten und Inhalte mithilfe von Direct3D 9 präsentieren. Die Verarbeitung kann das Rendern von Inhalten, das Decodieren von Videos, das Ausführen von Compute-Shadern usw. bedeuten. Die Anwendung wird für jeden Frame zuerst mit Direct3D 11 verarbeitet und dann mit Direct3D 9 und schließlich mit Direct3D 9 verarbeitet. Darüber hinaus werden bei der Verarbeitung mit Direct3D 11 einige Metadaten erzeugt, die der vorhandene Direct3D 9 verbrauchen muss. In diesem Abschnitt wird die Verwendung von Hilfsprogrammen in drei Teilen behandelt, die dieser Sequenz entsprechen: Initialisierung, Hauptschleife und Cleanup.

**Initialisierung**  
Die Initialisierung umfasst die folgenden Schritte:  

1.  Initialisieren Sie beide Geräte.
2.  Erstellen Sie die Stamm Warteschlange: m \_ 11warte Schlange.
3.  Aus der Stamm Warteschlange Klonen: m \_ 9on11queue.
4.  Openproducer/openconsumer in beiden Warteschlangen aufzurufen.

In den Warteschlangen Namen werden die Nummern 9 und 11 verwendet, um anzugeben, welche API der Producer ist und welche der Consumer: **m \_ ***Producer*** to ***Consumer*** Queue** ist. Entsprechend gibt m \_ 11warte Schlange eine Warteschlange an, für die das Gerät Direct3D 11 Oberflächen erzeugt, die vom Direct3D 9-Gerät genutzt werden. Entsprechend \_ gibt die Warteschlange "m 9to 11" eine Warteschlange an, für die Direct3D 9 Oberflächen erzeugt, die Direct3D 11 nutzt.  
Die Stamm Warteschlange ist anfänglich voll und alle geklonten Warteschlangen sind anfänglich leer Dies sollte für die Anwendung kein Problem darstellen, mit Ausnahme des ersten Durchlaufs der Enqueues und aus der Warteschlange und der Verfügbarkeit von Metadaten. Wenn ein aus der Warteschlange eingereiht wird, dass keine Metadaten vorhanden sind, aber keine festgelegt wurde (weil anfänglich nichts vorhanden ist oder die einreihen nichts festgelegt hat), wird von der Warteschlange festgestellt, dass keine Metadaten  

1.  **Initialisieren Sie beide Geräte.**  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  **Erstellen Sie die Stamm Warteschlange.**  
    Dieser Schritt erstellt auch die-Oberflächen. Größen-und Format Einschränkungen sind identisch mit der Erstellung einer freigegebenen Ressource. Die Größe des metadatenpuffers ist zur Erstellungszeit korrigiert, und in diesem Fall wird nur ein uint übergeben.  
    Die Warteschlange muss mit einer bestimmten Anzahl von Oberflächen erstellt werden. Die Leistung variiert abhängig vom jeweiligen Szenario. Das vorhanden sein mehrerer Oberflächen erhöht die Wahrscheinlichkeit, dass Geräte ausgelastet sind. Wenn es z. b. nur eine Oberfläche gibt, erfolgt keine Parallelisierung zwischen den beiden Geräten. Andererseits erhöht das Erhöhen der Anzahl der Oberflächen den Speicherbedarf, wodurch die Leistung beeinträchtigt werden kann. In diesem Beispiel werden zwei Oberflächen verwendet.  
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

    

3.  **Klonen Sie die Stamm Warteschlange.**  
    Jede geklonte Warteschlange muss die gleichen Oberflächen verwenden, kann jedoch unterschiedliche metadatenpuffergrößen und andere Flags aufweisen. In diesem Fall sind keine Metadaten von Direct3D 9 bis Direct3D 11 vorhanden.  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  **Öffnen Sie die Geräte Producer und Consumer.**  
    Die Anwendung muss diesen Schritt ausführen, bevor Enqueue und Dequeue aufgerufen wird. Beim Öffnen eines Producer und Consumer werden Schnittstellen zurückgegeben, die die Enqueue-/Dequeue-APIs enthalten.  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

**Hauptschleife**  
Die Verwendung der Warteschlange wird nach dem klassischen Producer/Consumer-Problem modelliert. Stellen Sie sich dies aus der Perspektive pro Gerät vor. Jedes Gerät muss die folgenden Schritte ausführen: Entfernen Sie die Warteschlange, um eine Oberfläche von der Warteschlange zu erhalten, und verarbeiten Sie Sie auf der Oberfläche. Für das Gerät Direct3D 11 ist die Verwendung von Direct3D 9 nahezu identisch.  


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
Dieser Schritt ist sehr unkompliziert. Zusätzlich zu den normalen Schritten zum Bereinigen von Direct3D-APIs muss die Anwendung die Rückgabe-com-Schnittstellen freigeben.  


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

Das vorherige Beispiel ist für einen multithreadnutzungsfall sinnvoll, bei dem jedes Gerät über einen eigenen Thread verfügt. In diesem Beispiel werden die blockierenden Versionen der APIs verwendet: unendlich für Timeout und kein Flag zum Einreihen in die Warteschlange. Wenn Sie das Hilfsprogramm auf nicht blockierende Weise verwenden möchten, müssen Sie nur einige Änderungen vornehmen. In diesem Abschnitt wird die nicht blockierende Verwendung für beide Geräte in einem Thread veranschaulicht.

**Initialisierung**  
Die Initialisierung ist mit Ausnahme der Flags identisch. Da es sich bei der Anwendung um einen Single Thread handelt, verwenden Sie dieses Flag für die Erstellung. Dadurch wird ein Teil des Synchronisierungs Codes deaktiviert, wodurch die Leistung möglicherweise verbessert wird.  


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



Das Öffnen von Producer-und Consumer-Geräten ist dasselbe wie im Blockierungs Beispiel.  
**Verwenden der Warteschlange**  
Es gibt viele Möglichkeiten, die Warteschlange in einer nicht blockierenden Weise mit verschiedenen Leistungsmerkmalen zu verwenden. Das folgende Beispiel ist einfach, hat jedoch aufgrund übermäßiger Drehung und Abruf eine schlechte Leistung. Trotz dieser Probleme zeigt das Beispiel, wie das Hilfsprogramm verwendet werden kann. Der Ansatz besteht darin, ständig in einer Schleife zu sitzen und aus der Warteschlange zu entfernen, Sie zu verarbeiten, in die Warteschlange zu stellen Wenn einer der Schritte fehlschlägt, weil die Ressource nicht verfügbar ist, versucht die Anwendung einfach erneut, die nächste Schleife auszuführen.  


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



Eine komplexere Lösung könnte den Rückgabewert von einreihen und von Flush überprüfen, um zu bestimmen, ob eine Leerung erforderlich ist.  
</dl>

### <a name="three-devices"></a>Drei Geräte

Das Erweitern der vorherigen Beispiele auf mehrere Geräte ist einfach. Der folgende Code führt die Initialisierung aus. Nachdem die Producer/Consumer-Objekte erstellt wurden, ist der Code für die Verwendung identisch. Dieses Beispiel enthält drei Geräte und somit drei Warteschlangen. Die Oberflächen werden von Direct3D 9 bis Direct3D 10 bis Direct3D 11 abgeleitet.


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



Wie bereits erwähnt, funktioniert das Klonen auf dieselbe Weise, unabhängig davon, welche Warteschlange geklont wird. Beispielsweise könnte der zweite Klon-Befehl aus dem Objekt "m \_ 9to 10queue" entfernt worden sein.


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

Sie können Lösungen erstellen, die mithilfe von Interoperabilität die Leistungsfähigkeit mehrerer DirectX-APIs nutzen. Die Interoperabilität der Windows-Grafik-API bietet nun eine Common Surface Management Runtime DXGI 1,1. Diese Laufzeit ermöglicht die Unterstützung synchroner Oberflächen Freigabe in neu entwickelten APIs, z. b. Direct3D 11, Direct3D 10,1 und Direct2D. Die Verbesserungen der Interoperabilität zwischen neuen APIs und vorhandenen APIs unterstützen die Anwendungs Migration und Abwärtskompatibilität. Die Consumer-APIs Direct3D 9Ex und DXGI 1,1 können zusammenarbeiten, wie Sie mit dem Synchronisierungs Mechanismus veranschaulicht werden, der durch Sample Helper Code in der MSDN Code Gallery bereitgestellt wird.

 

 