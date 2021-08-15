---
description: In diesem Thema wird beschrieben, wie DirectX Video Acceleration (DXVA) 2.0 in einem DirectShow-Decoderfilter unterstützt wird.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Unterstützen von DXVA 2.0 in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58631a407e42c0561ebee0ad2b3187e248fc2d25dc0bdf4e98ed0219d8dae916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238083"
---
# <a name="supporting-dxva-20-in-directshow"></a>Unterstützen von DXVA 2.0 in DirectShow

In diesem Thema wird beschrieben, wie DirectX Video Acceleration (DXVA) 2.0 in einem DirectShow-Decoderfilter unterstützt wird. Insbesondere wird die Kommunikation zwischen dem Decoder und dem Videorenderer beschrieben. In diesem Thema wird nicht beschrieben, wie die DXVA-Decodierung implementiert wird.

-   [Voraussetzungen](#prerequisites)
-   [Migrationshinweise](#migration-notes)
-   [Suchen einer Decoderkonfiguration](#finding-a-decoder-configuration)
-   [Benachrichtigen des Videorenderers](#notifying-the-video-renderer)
-   [Zuordnen von nicht komprimierten Puffern](#allocating-uncompressed-buffers)
-   [Decodierung](#decoding)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

In diesem Thema wird davon ausgegangen, dass Sie mit dem Schreiben von DirectShow-Filtern vertraut sind. Weitere Informationen finden Sie im Thema [Schreiben von DirectShow-Filtern](../directshow/writing-directshow-filters.md) in der DirectShow SDK-Dokumentation. In den Codebeispielen in diesem Thema wird davon ausgegangen, dass der Decoderfilter von der [**CTransformFilter-Klasse**](../directshow/ctransformfilter.md) mit der folgenden Klassendefinition abgeleitet ist:


```C++
class CDecoder : public CTransformFilter
{
public:
    static CUnknown* WINAPI CreateInstance(IUnknown *pUnk, HRESULT *pHr);

    HRESULT CompleteConnect(PIN_DIRECTION direction, IPin *pPin);

    HRESULT InitAllocator(IMemAllocator **ppAlloc);
    HRESULT DecideBufferSize(IMemAllocator *pAlloc, ALLOCATOR_PROPERTIES *pProp);

    // TODO: The implementations of these methods depend on the specific decoder.
    HRESULT CheckInputType(const CMediaType *mtIn);
    HRESULT CheckTransform(const CMediaType *mtIn, const CMediaType *mtOut);
    HRESULT CTransformFilter::GetMediaType(int,CMediaType *);

private:
    CDecoder(HRESULT *pHr);
    ~CDecoder();

    CBasePin * GetPin(int n);

    HRESULT ConfigureDXVA2(IPin *pPin);
    HRESULT SetEVRForDXVA2(IPin *pPin);

    HRESULT FindDecoderConfiguration(
        /* [in] */  IDirectXVideoDecoderService *pDecoderService,
        /* [in] */  const GUID& guidDecoder, 
        /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
        /* [out] */ BOOL *pbFoundDXVA2Configuration
        );

private:
    IDirectXVideoDecoderService *m_pDecoderService;

    DXVA2_ConfigPictureDecode m_DecoderConfig;
    GUID                      m_DecoderGuid;
    HANDLE                    m_hDevice;

    FOURCC                    m_fccOutputFormat;
};
```



Im weiteren Verlauf dieses Themas bezieht sich der Begriff *Decoder* auf den Decoderfilter, der komprimierte Videos empfängt und nicht komprimierte Videos ausgibt. Der Begriff *Decodergerät* bezieht sich auf eine Hardware-Videobeschleunigung, die vom Grafiktreiber implementiert wird.

Hier sind die grundlegenden Schritte, die ein Decoderfilter ausführen muss, um DXVA 2.0 zu unterstützen:

1.  Aushandeln eines Medientyps.
2.  Suchen Sie nach einer DXVA-Decoderkonfiguration.
3.  Benachrichtigen Sie den Videorenderer, dass der Decoder die DXVA-Decodierung verwendet.
4.  Stellen Sie eine benutzerdefinierte Zuweisung bereit, die Direct3D-Oberflächen zuordnet.

Diese Schritte werden im weiteren Verlauf dieses Themas ausführlicher beschrieben.

## <a name="migration-notes"></a>Migrationshinweise

Wenn Sie von DXVA 1.0 migrieren, sollten Sie einige wesentliche Unterschiede zwischen den beiden Versionen kennen:

-   DXVA 2.0 verwendet nicht die Schnittstellen [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) und [**IAMVideoAcceleratorNotify,**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) da der Decoder direkt über die [**IDirectXVideoDecoder-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) auf die DXVA 2.0-APIs zugreifen kann.
-   Während der Medientypaushandlung verwendet der Decoder keine Videobeschleunigungs-GUID als Untertyp. Stattdessen ist der Untertyp nur das unkomprimierte Videoformat (z. B. NV12), wie bei der Softwaredecodierung.
-   Das Verfahren zum Konfigurieren der Zugriffstaste wurde geändert. In DXVA 1.0 ruft der Decoder **Execute** mit einer **DXVA \_ ConfigPictureDecode-Struktur** auf, um den Accerlator zu konfigurieren. In DXVA 2.0 verwendet der Decoder die [**IDirectXVideoDecoderService-Schnittstelle,**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) wie im nächsten Abschnitt beschrieben.
-   Der Decoder ordnet die nicht komprimierten Puffer zu. Der Videorenderer ordnet sie nicht mehr zu.
-   Anstatt [**IAMVideoAccelerator::D isplayFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) aufzurufen, um den decodierten Frame anzuzeigen, übermittelt der Decoder den Frame an den Renderer, indem [**er IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive)aufruft, wie bei der Softwaredecodierung.
-   Der Decoder ist nicht mehr für die Überprüfung verantwortlich, wann Datenpuffer für Updates sicher sind. Daher verfügt DXVA 2.0 nicht über eine Methode, die [**IAMVideoAccelerator::QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus)entspricht.
-   Die Überblendung wird vom Videorenderer mithilfe der DXVA2.0-Videoprozessor-APIs durchgeführt. Decoder, die Unterbilder bereitstellen (z. B. DVD-Decoder), sollten Bildunterbilddaten an einen separaten Ausgabepin senden.

Für Decodierungsvorgänge verwendet DXVA 2.0 die gleichen Datenstrukturen wie DXVA 1.0.

Der filter enhanced video renderer (EVR) unterstützt DXVA 2.0. Die Filter des Videomischungsrenderers (VMR-7 und VMR-9) unterstützen nur DXVA 1.0.

## <a name="finding-a-decoder-configuration"></a>Suchen einer Decoderkonfiguration

Nachdem der Decoder den Ausgabemedientyp ausgehandelt hat, muss er eine kompatible Konfiguration für das DXVA-Decodergerät finden. Sie können diesen Schritt innerhalb der [**CBaseOutputPin::CompleteConnect-Methode**](../directshow/cbaseoutputpin-completeconnect.md) des Ausgabepins ausführen. Mit diesem Schritt wird sichergestellt, dass der Grafiktreiber die vom Decoder benötigten Funktionen unterstützt, bevor der Decoder für die Verwendung von DXVA committet wird.

Gehen Sie wie folgt vor, um eine Konfiguration für das Decodergerät zu finden:

1.  Fragen Sie den Eingabepin des Renderers nach der [**SCHNITTSTELLE "ENGETService"**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) ab.
2.  Rufen Sie [**DEN CURSORGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) auf, um einen Zeiger auf die [**IDirect3DDeviceManager9-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) abzurufen. Die Dienst-GUID ist MR \_ VIDEO \_ ACCELERATION \_ SERVICE.
3.  Rufen Sie [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) auf, um ein Handle für das Direct3D-Gerät des Renderers abzurufen.
4.  Rufen Sie [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) auf, und übergeben Sie das Gerätehandle. Diese Methode gibt einen Zeiger auf die [**IDirectXVideoDecoderService-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) zurück.
5.  Rufen Sie [**IDirectXVideoDecoderService::GetDecoderDeviceGuids auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids) Diese Methode gibt ein Array von Decodergeräte-GUIDs zurück.
6.  Durchlaufen Sie das Array von Decoder-GUIDs, um diejenigen zu finden, die der Decoderfilter unterstützt. Beispielsweise würden Sie für einen MPEG-2-Decoder nach **DXVA2 \_ ModeMPEG2 \_ MOCOMP,** **DXVA2 \_ ModeMPEG2 \_ IDCT** oder **DXVA2 \_ ModeMPEG2 \_ VLD** suchen.

7.  Wenn Sie eine Kandidaten-Decodergeräte-GUID finden, übergeben Sie die GUID an die [**IDirectXVideoDecoderService::GetDecoderRenderTargets-Methode.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) Diese Methode gibt ein Array von Renderzielformaten zurück, die als **D3DFORMAT-Werte** angegeben sind.
8.  Durchlaufen Sie die Renderzielformate, und suchen Sie nach einem Format, das Ihrem Ausgabeformat entspricht. In der Regel unterstützt ein Decodergerät ein einzelnes Renderzielformat. Der Decoderfilter sollte mit diesem Untertyp eine Verbindung mit dem Renderer herstellen. Beim ersten Aufruf von [**CompleteConnect**](../directshow/cbaseoutputpin-completeconnect.md)kann der Decoder das Renderzielformat bestimmen und dieses Format dann als bevorzugten Ausgabetyp zurückgeben.

9.  Rufen Sie [**IDirectXVideoDecoderService::GetDecoderConfigurations auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations) Übergeben Sie die gleiche Decodergeräte-GUID zusammen mit einer [**DXVA2 \_ VideoDesc-Struktur,**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) die das vorgeschlagene Format beschreibt. Die -Methode gibt ein Array von [**DXVA2-ConfigPictureDecode-Strukturen \_**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) zurück. Jede Struktur beschreibt eine mögliche Konfiguration für das Decodergerät.

10. Wenn die vorherigen Schritte erfolgreich sind, speichern Sie das Direct3D-Gerätehandle, die Decodergeräte-GUID und die Konfigurationsstruktur. Der Filter verwendet diese Informationen, um das Decodergerät zu erstellen.

Der folgende Code zeigt, wie Sie eine Decoderkonfiguration finden.


```C++
HRESULT CDecoder::ConfigureDXVA2(IPin *pPin)
{
    UINT    cDecoderGuids = 0;
    BOOL    bFoundDXVA2Configuration = FALSE;
    GUID    guidDecoder = GUID_NULL;

    DXVA2_ConfigPictureDecode config;
    ZeroMemory(&config, sizeof(config));

    // Variables that follow must be cleaned up at the end.

    IMFGetService               *pGetService = NULL;
    IDirect3DDeviceManager9     *pDeviceManager = NULL;
    IDirectXVideoDecoderService *pDecoderService = NULL;

    GUID   *pDecoderGuids = NULL; // size = cDecoderGuids
    HANDLE hDevice = INVALID_HANDLE_VALUE;

    // Query the pin for IMFGetService.
    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pGetService));

    // Get the Direct3D device manager.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(

            MR_VIDEO_ACCELERATION_SERVICE,
            IID_PPV_ARGS(&pDeviceManager)
            );
    }

    // Open a new device handle.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    } 

    // Get the video decoder service.
    if (SUCCEEDED(hr))
    {
        hr = pDeviceManager->GetVideoService(
            hDevice, IID_PPV_ARGS(&pDecoderService));
    }

    // Get the decoder GUIDs.
    if (SUCCEEDED(hr))
    {
        hr = pDecoderService->GetDecoderDeviceGuids(
            &cDecoderGuids, &pDecoderGuids);
    }

    if (SUCCEEDED(hr))
    {
        // Look for the decoder GUIDs we want.
        for (UINT iGuid = 0; iGuid < cDecoderGuids; iGuid++)
        {
            // Do we support this mode?
            if (!IsSupportedDecoderMode(pDecoderGuids[iGuid]))
            {
                continue;
            }

            // Find a configuration that we support. 
            hr = FindDecoderConfiguration(pDecoderService, pDecoderGuids[iGuid],
                &config, &bFoundDXVA2Configuration);
            if (FAILED(hr))
            {
                break;
            }

            if (bFoundDXVA2Configuration)
            {
                // Found a good configuration. Save the GUID and exit the loop.
                guidDecoder = pDecoderGuids[iGuid];
                break;
            }
        }
    }

    if (!bFoundDXVA2Configuration)
    {
        hr = E_FAIL; // Unable to find a configuration.
    }

    if (SUCCEEDED(hr))
    {
        // Store the things we will need later.

        SafeRelease(&m_pDecoderService);
        m_pDecoderService = pDecoderService;
        m_pDecoderService->AddRef();

        m_DecoderConfig = config;
        m_DecoderGuid = guidDecoder;
        m_hDevice = hDevice;
    }

    if (FAILED(hr))
    {
        if (hDevice != INVALID_HANDLE_VALUE)
        {
            pDeviceManager->CloseDeviceHandle(hDevice);
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pDeviceManager);
    SafeRelease(&pDecoderService);
    return hr;
}
HRESULT CDecoder::FindDecoderConfiguration(
    /* [in] */  IDirectXVideoDecoderService *pDecoderService,
    /* [in] */  const GUID& guidDecoder, 
    /* [out] */ DXVA2_ConfigPictureDecode *pSelectedConfig,
    /* [out] */ BOOL *pbFoundDXVA2Configuration
    )
{
    HRESULT hr = S_OK;
    UINT cFormats = 0;
    UINT cConfigurations = 0;

    D3DFORMAT                   *pFormats = NULL;     // size = cFormats
    DXVA2_ConfigPictureDecode   *pConfig = NULL;      // size = cConfigurations

    // Find the valid render target formats for this decoder GUID.
    hr = pDecoderService->GetDecoderRenderTargets(
        guidDecoder,
        &cFormats,
        &pFormats
        );

    if (SUCCEEDED(hr))
    {
        // Look for a format that matches our output format.
        for (UINT iFormat = 0; iFormat < cFormats;  iFormat++)
        {
            if (pFormats[iFormat] != (D3DFORMAT)m_fccOutputFormat)
            {
                continue;
            }

            // Fill in the video description. Set the width, height, format, 
            // and frame rate.
            DXVA2_VideoDesc videoDesc = {0};

            FillInVideoDescription(&videoDesc); // Private helper function.
            videoDesc.Format = pFormats[iFormat];

            // Get the available configurations.
            hr = pDecoderService->GetDecoderConfigurations(
                guidDecoder,
                &videoDesc,
                NULL, // Reserved.
                &cConfigurations,
                &pConfig
                );

            if (FAILED(hr))
            {
                break;
            }

            // Find a supported configuration.
            for (UINT iConfig = 0; iConfig < cConfigurations; iConfig++)
            {
                if (IsSupportedDecoderConfig(pConfig[iConfig]))
                {
                    // This configuration is good.
                    *pbFoundDXVA2Configuration = TRUE;
                    *pSelectedConfig = pConfig[iConfig];
                    break;
                }
            }

            CoTaskMemFree(pConfig);
            break;

        } // End of formats loop.
    }

    CoTaskMemFree(pFormats);

    // Note: It is possible to return S_OK without finding a configuration.
    return hr;
}
```



Da dieses Beispiel generisch ist, wurde ein Teil der Logik in Hilfsfunktionen platziert, die vom Decoder implementiert werden müssten. Der folgende Code zeigt die Deklarationen für diese Funktionen:


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a>Benachrichtigen des Videorenderers

Wenn der Decoder eine Decoderkonfiguration findet, besteht der nächste Schritt darin, den Videorenderer zu benachrichtigen, dass der Decoder die Hardwarebeschleunigung verwendet. Sie können diesen Schritt innerhalb der [**CompleteConnect-Methode**](../directshow/cbaseoutputpin-completeconnect.md) ausführen. Dieser Schritt muss ausgeführt werden, bevor die Zuweisung ausgewählt wird, da sie sich darauf auswirkt, wie die Zuweisung ausgewählt wird.

1.  Fragen Sie den Eingabepin des Renderers nach der [**SCHNITTSTELLE "ENGETService"**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) ab.
2.  Rufen Sie [**AUFGETService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) auf, um einen Zeiger auf die [**IDirectXVideoMemoryConfiguration-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) abzurufen. Die Dienst-GUID ist **MR \_ VIDEO ACCELERATION \_ \_ SERVICE.**
3.  Rufen Sie [**IDirectXVideoMemoryConfiguration::GetAvailableSurfaceTypeByIndex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in einer Schleife auf, und erhöhen Sie dabei die Variable *dwTypeIndex* von 0 (null). Wird beendet, wenn die Methode den Wert **DXVA2 \_ SurfaceType \_ DecoderRenderTarget** im *pdwType-Parameter* zurückgibt. Dieser Schritt stellt sicher, dass der Videorenderer die hardwarebeschleunigte Decodierung unterstützt. Dieser Schritt ist für den EVR-Filter immer erfolgreich.
4.  Wenn der vorherige Schritt erfolgreich war, rufen Sie [**IDirectXVideoMemoryConfiguration::SetSurfaceType**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) mit dem Wert DXVA2 \_ SurfaceType \_ DecoderRenderTarget auf. Durch Aufrufen von **SetSurfaceType** mit diesem Wert wird der Videorenderer in den DXVA-Modus versetzt. Wenn sich der Videorenderer in diesem Modus befindet, muss der Decoder einen eigenen Allocator bereitstellen.

Der folgende Code zeigt, wie der Videorenderer benachrichtigt wird.


```C++
HRESULT CDecoder::SetEVRForDXVA2(IPin *pPin)
{
    HRESULT hr = S_OK;

    IMFGetService                       *pGetService = NULL;
    IDirectXVideoMemoryConfiguration    *pVideoConfig = NULL;

    // Query the pin for IMFGetService.
    hr = pPin->QueryInterface(__uuidof(IMFGetService), (void**)&pGetService);

    // Get the IDirectXVideoMemoryConfiguration interface.
    if (SUCCEEDED(hr))
    {
        hr = pGetService->GetService(
            MR_VIDEO_ACCELERATION_SERVICE, IID_PPV_ARGS(&pVideoConfig));
    }

    // Notify the EVR. 
    if (SUCCEEDED(hr))
    {
        DXVA2_SurfaceType surfaceType;

        for (DWORD iTypeIndex = 0; ; iTypeIndex++)
        {
            hr = pVideoConfig->GetAvailableSurfaceTypeByIndex(iTypeIndex, &surfaceType);
            
            if (FAILED(hr))
            {
                break;
            }

            if (surfaceType == DXVA2_SurfaceType_DecoderRenderTarget)
            {
                hr = pVideoConfig->SetSurfaceType(DXVA2_SurfaceType_DecoderRenderTarget);
                break;
            }
        }
    }

    SafeRelease(&pGetService);
    SafeRelease(&pVideoConfig);

    return hr;
}
```



Wenn der Decoder eine gültige Konfiguration findet und den Videorenderer erfolgreich benachrichtigt, kann der Decoder DXVA für die Decodierung verwenden. Der Decoder muss eine benutzerdefinierte Zuweisung für den Ausgabepin implementieren, wie im nächsten Abschnitt beschrieben.

## <a name="allocating-uncompressed-buffers"></a>Zuordnen von nicht komprimierten Puffern

In DXVA 2.0 ist der Decoder für die Zuweisung von Direct3D-Oberflächen verantwortlich, die als unkomprimierte Videopuffer verwendet werden sollen. Daher muss der Decoder eine benutzerdefinierte Zuweisung implementieren, die die Oberflächen erstellt. Die von dieser Zuweisung bereitgestellten Medienbeispiele enthalten Zeiger auf die Direct3D-Oberflächen. Die EVR ruft einen Zeiger auf die Oberfläche ab, indem SIE IM Medienbeispiel [**DENHERGETSERVICE::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) aufrufen. Der Dienstbezeichner ist **MR \_ BUFFER \_ SERVICE.**

Führen Sie die folgenden Schritte aus, um die benutzerdefinierte Zuweisung bereitzustellen:

1.  Definieren Sie eine Klasse für die Medienbeispiele. Diese Klasse kann von der [**CMediaSample-Klasse**](../directshow/cmediasample.md) abgeleitet werden. Gehen Sie in dieser Klasse wie folgt vor:
    -   Store einen Zeiger auf die Direct3D-Oberfläche.
    -   Implementieren Sie [**die INTERFACESGetService-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) Wenn die Dienst-GUID in der [**GetService-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) **MR BUFFER \_ \_ SERVICE** ist, fragen Sie die Direct3D-Oberfläche nach der angeforderten Schnittstelle ab. Andernfalls **kann GetService** **MF \_ E \_ UNSUPPORTED \_ SERVICE zurückgeben.**
    -   Überschreiben Sie [**die CMediaSample::GetPointer-Methode,**](../directshow/cmediasample-getpointer.md) um E \_ NOTIMPL zurück zu geben.
2.  Definieren Sie eine Klasse für die Zuweisung. Die Zuweisung kann von der [**CBaseAllocator-Klasse ableiten.**](../directshow/cbaseallocator.md) Gehen Sie in dieser Klasse wie folgt vor.
    -   Überschreiben Sie [**die CBaseAllocator::Alloc-Methode.**](../directshow/cbaseallocator-alloc.md) Rufen Sie in dieser Methode [**IDirectXVideoAccelerationService::CreateSurface auf,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) um die Oberflächen zu erstellen. (Die [**IDirectXVideoDecoderService-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) erbt diese Methode von [**IDirectXVideoAccelerationService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)
    -   Überschreiben Sie [**die CBaseAllocator::Free-Methode,**](../directshow/cbaseallocator-free.md) um die Oberflächen frei zu geben.
3.  Überschreiben Sie im Ausgabepin Ihres Filters die [**CBaseOutputPin::InitAllocator-Methode.**](../directshow/cbaseoutputpin-initallocator.md) Erstellen Sie in dieser Methode eine Instanz Ihrer benutzerdefinierten Zuweisung.
4.  Implementieren Sie in Ihrem Filter die [**CTransformFilter::D ecideBufferSize-Methode.**](../directshow/ctransformfilter-decidebuffersize.md) Der *pProperties-Parameter* gibt die Anzahl von Oberflächen an, die evr benötigt. Fügen Sie diesem Wert die Anzahl von Oberflächen hinzu, die ihr Decoder benötigt, und rufen Sie [**IMemAllocator::SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) für die Zuweisung auf.

Der folgende Code zeigt, wie die Medienbeispielklasse implementiert wird:


```C++
class CDecoderSample : public CMediaSample, public IMFGetService
{
    friend class CDecoderAllocator;

public:

    CDecoderSample(CDecoderAllocator *pAlloc, HRESULT *phr)
        : CMediaSample(NAME("DecoderSample"), (CBaseAllocator*)pAlloc, phr, NULL, 0),
          m_pSurface(NULL),
          m_dwSurfaceId(0)
    { 
    }

    // Note: CMediaSample does not derive from CUnknown, so we cannot use the
    //       DECLARE_IUNKNOWN macro that is used by most of the filter classes.

    STDMETHODIMP QueryInterface(REFIID riid, void **ppv)
    {
        CheckPointer(ppv, E_POINTER);

        if (riid == IID_IMFGetService)
        {
            *ppv = static_cast<IMFGetService*>(this);
            AddRef();
            return S_OK;
        }
        else
        {
            return CMediaSample::QueryInterface(riid, ppv);
        }
    }
    STDMETHODIMP_(ULONG) AddRef()
    {
        return CMediaSample::AddRef();
    }

    STDMETHODIMP_(ULONG) Release()
    {
        // Return a temporary variable for thread safety.
        ULONG cRef = CMediaSample::Release();
        return cRef;
    }

    // IMFGetService::GetService
    STDMETHODIMP GetService(REFGUID guidService, REFIID riid, LPVOID *ppv)
    {
        if (guidService != MR_BUFFER_SERVICE)
        {
            return MF_E_UNSUPPORTED_SERVICE;
        }
        else if (m_pSurface == NULL)
        {
            return E_NOINTERFACE;
        }
        else
        {
            return m_pSurface->QueryInterface(riid, ppv);
        }
    }

    // Override GetPointer because this class does not manage a system memory buffer.
    // The EVR uses the MR_BUFFER_SERVICE service to get the Direct3D surface.
    STDMETHODIMP GetPointer(BYTE ** ppBuffer)
    {
        return E_NOTIMPL;
    }

private:

    // Sets the pointer to the Direct3D surface. 
    void SetSurface(DWORD surfaceId, IDirect3DSurface9 *pSurf)
    {
        SafeRelease(&m_pSurface);

        m_pSurface = pSurf;
        if (m_pSurface)
        {
            m_pSurface->AddRef();
        }

        m_dwSurfaceId = surfaceId;
    }

    IDirect3DSurface9   *m_pSurface;
    DWORD               m_dwSurfaceId;
};
```



Der folgende Code zeigt, wie die [**Alloc-Methode**](../directshow/cbaseallocator-alloc.md) für die Zuweisung implementiert wird.


```C++
HRESULT CDecoderAllocator::Alloc()
{
    CAutoLock lock(this);

    HRESULT hr = S_OK;

    if (m_pDXVA2Service == NULL)
    {
        return E_UNEXPECTED;
    }

    hr = CBaseAllocator::Alloc();

    // If the requirements have not changed, do not reallocate.
    if (hr == S_FALSE)
    {
        return S_OK;
    }

    if (SUCCEEDED(hr))
    {
        // Free the old resources.
        Free();

        // Allocate a new array of pointers.
        m_ppRTSurfaceArray = new (std::nothrow) IDirect3DSurface9*[m_lCount];
        if (m_ppRTSurfaceArray == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
        else
        {
            ZeroMemory(m_ppRTSurfaceArray, sizeof(IDirect3DSurface9*) * m_lCount);
        }
    }

    // Allocate the surfaces.
    if (SUCCEEDED(hr))
    {
        hr = m_pDXVA2Service->CreateSurface(
            m_dwWidth,
            m_dwHeight,
            m_lCount - 1,
            (D3DFORMAT)m_dwFormat,
            D3DPOOL_DEFAULT,
            0,
            DXVA2_VideoDecoderRenderTarget,
            m_ppRTSurfaceArray,
            NULL
            );
    }

    if (SUCCEEDED(hr))
    {
        for (m_lAllocated = 0; m_lAllocated < m_lCount; m_lAllocated++)
        {
            CDecoderSample *pSample = new (std::nothrow) CDecoderSample(this, &hr);

            if (pSample == NULL)
            {
                hr = E_OUTOFMEMORY;
                break;
            }
            if (FAILED(hr))
            {
                break;
            }
            // Assign the Direct3D surface pointer and the index.
            pSample->SetSurface(m_lAllocated, m_ppRTSurfaceArray[m_lAllocated]);

            // Add to the sample list.
            m_lFree.Add(pSample);
        }
    }

    if (SUCCEEDED(hr))
    {
        m_bChanged = FALSE;
    }
    return hr;
}
```



Hier ist der Code für die [**Free-Methode:**](../directshow/cbaseallocator-free.md)


```C++
void CDecoderAllocator::Free()
{
    CMediaSample *pSample = NULL;

    do
    {
        pSample = m_lFree.RemoveHead();
        if (pSample)
        {
            delete pSample;
        }
    } while (pSample);

    if (m_ppRTSurfaceArray)
    {
        for (long i = 0; i < m_lAllocated; i++)
        {
            SafeRelease(&m_ppRTSurfaceArray[i]);
        }

        delete [] m_ppRTSurfaceArray;
    }
    m_lAllocated = 0;
}
```



Weitere Informationen zum Implementieren von benutzerdefinierten Zuweisungen finden Sie im Thema [Bereitstellen](../directshow/providing-a-custom-allocator.md) einer benutzerdefinierten Zuweisung in der DirectShow SDK-Dokumentation.

## <a name="decoding"></a>Decodierung

Rufen Sie zum Erstellen des Decodergeräts [**IDirectXVideoDecoderService::CreateVideoDecoder auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder) Die -Methode gibt einen Zeiger auf die [**IDirectXVideoDecoder-Schnittstelle**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) des Decodergeräts zurück.

Rufen Sie in jedem Frame [**IDirect3DDeviceManager9::TestDevice auf,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) um das Gerätehandy zu testen. Wenn das Gerät geändert wurde, gibt die Methode DXVA2 \_ E NEW VIDEO DEVICE \_ \_ \_ zurück. Gehen Sie in diesem Fall wie folgt vor:

1.  Schließen Sie das Gerätehandle, indem [**Sie IDirect3DDeviceManager9::CloseDeviceHandle aufrufen.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle)
2.  Geben Sie [**die Zeiger IDirectXVideoDecoderService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) und [**IDirectXVideoDecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) frei.
3.  Öffnen Sie ein neues Gerätehand handle.
4.  Aushandeln einer neuen Decoderkonfiguration, wie im Abschnitt [Suchen einer Decoderkonfiguration beschrieben.](#finding-a-decoder-configuration)
5.  Erstellen Sie ein neues Decodergerät.

Unter der Annahme, dass das Gerätehandy gültig ist, funktioniert der Decodierungsprozess wie folgt:

1.  Rufen [**Sie IDirectXVideoDecoder::BeginFrame auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)
2.  Führen Sie die folgenden Schritte mindestens einmal aus:
    1.  Rufen [**Sie IDirectXVideoDecoder::GetBuffer auf,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) um einen DXVA-Decoderpuffer zu erhalten.
    2.  Füllen Sie den Puffer aus.
    3.  Rufen [**Sie IDirectXVideoDecoder::ReleaseBuffer auf.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer)
3.  Rufen [**Sie IDirectXVideoDecoder::Execute auf,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) um die Decodierungsvorgänge für den Frame auszuführen.

DXVA 2.0 verwendet dieselben Datenstrukturen wie DXVA 1.0 für Decodierungsvorgänge. Für den ursprünglichen Satz von DXVA-Profilen (für H.261, H.263 und MPEG-2) werden diese Datenstrukturen in der [DXVA 1.0-Spezifikation beschrieben.](/windows-hardware/drivers/display/directx-video-acceleration)

Innerhalb jedes [**BeginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)Execute-Aufrufpaars können Sie GetBuffer mehrmals aufrufen, jedoch nur einmal für jeden / [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) DXVA-Puffertyp. [](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) Wenn Sie ihn zweimal mit dem gleichen Puffertyp aufrufen, überschreiben Sie die Daten.

Rufen Sie [**nach dem Aufruf**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute)von Execute [**IMemInputPin::Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) auf, um den Frame wie bei der Softwaredecodierung an den Videorenderer zu liefern. Die **Receive-Methode** ist asynchron. Nach der Rückgabe kann der Decoder mit der Decodierung des nächsten Frames fortfahren. Der Anzeigetreiber verhindert, dass Decodierungsbefehle den Puffer überschreiben, während der Puffer verwendet wird. Der Decoder sollte eine Oberfläche nicht wiederverwenden, um einen anderen Frame zu decodieren, bis der Renderer das Beispiel freigegeben hat. Wenn der Renderer das Beispiel frei gibt, setzt die Zuweisung das Beispiel wieder in den Pool der verfügbaren Beispiele. Um das nächste verfügbare Beispiel zu erhalten, rufen Sie [**CBaseOutputPin::GetDeliveryBuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md)auf, das wiederum [**IMemAllocator::GetBuffer aufruft.**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer) Weitere Informationen finden Sie im Thema [Overview of Data Flow in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) in der DirectShow-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Videobeschleunigung 2.0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
