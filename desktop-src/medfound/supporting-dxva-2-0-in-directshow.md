---
description: In diesem Thema wird beschrieben, wie DirectX Video Acceleration (DXVA) 2,0 in einem DirectShow-Decoderfilter unterstützt wird.
ms.assetid: 40deaddb-bb17-4a34-8294-5c7dc8a8a457
title: Unterstützung von DXVA 2,0 in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda956b60d4905c2392e1a50bd62ee8421b944b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863407"
---
# <a name="supporting-dxva-20-in-directshow"></a>Unterstützung von DXVA 2,0 in DirectShow

In diesem Thema wird beschrieben, wie DirectX Video Acceleration (DXVA) 2,0 in einem DirectShow-Decoderfilter unterstützt wird. Insbesondere wird die Kommunikation zwischen dem Decoder und dem Videorenderer beschrieben. In diesem Thema wird nicht beschrieben, wie DXVA-Decodierung implementiert wird.

-   [Voraussetzungen](#prerequisites)
-   [Hinweise zur Migration](#migration-notes)
-   [Suchen einer decoderkonfiguration](#finding-a-decoder-configuration)
-   [Benachrichtigen des Videorenderers](#notifying-the-video-renderer)
-   [Zuordnen von nicht komprimierten Puffern](#allocating-uncompressed-buffers)
-   [Decodierung](#decoding)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Dieses Thema setzt voraus, dass Sie mit dem Schreiben von DirectShow-Filtern vertraut sind. Weitere Informationen finden Sie im Thema [Schreiben von DirectShow-Filtern](../directshow/writing-directshow-filters.md) in der DirectShow-SDK-Dokumentation. In den Codebeispielen in diesem Thema wird davon ausgegangen, dass der Decoderfilter von der [**ctransformfilter**](../directshow/ctransformfilter.md) -Klasse mit der folgenden Klassendefinition abgeleitet ist:


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



Im restlichen Teil dieses Themas verweist der Begriff " *Decoder* " auf den Decoder-Filter, der komprimierte Videos empfängt und unkomprimierte Videos ausgibt. Der Begriff " *Decoder-Gerät* " bezieht sich auf einen Hardware-Video Beschleuniger, der vom Grafiktreiber implementiert wird.

Dies sind die grundlegenden Schritte, die ein Decoder-Filter ausführen muss, um DXVA 2,0 zu unterstützen:

1.  Aushandeln eines Medientyps.
2.  Suchen Sie die Konfiguration des DXVA-Decoders.
3.  Benachrichtigen Sie den Videorenderer, dass der Decoder DXVA-Decodierung verwendet.
4.  Stellen Sie eine benutzerdefinierte Zuweisung bereit, die Direct3D-Oberflächen zuordnet.

Diese Schritte werden im weiteren Verlauf dieses Themas ausführlicher beschrieben.

## <a name="migration-notes"></a>Hinweise zur Migration

Wenn Sie von DXVA 1,0 migrieren, sollten Sie einige bedeutende Unterschiede zwischen den beiden Versionen beachten:

-   DXVA 2,0 verwendet nicht die [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) -und [**iamvideoacceleratornotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) -Schnittstellen, da der Decoder direkt über die [**idirectxvideodecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) -Schnittstelle auf die DXVA 2,0-APIs zugreifen kann.
-   Während der Medientyp Aushandlung verwendet der Decoder keine Video-Acceleration-GUID als Untertyp. Stattdessen ist der Untertyp nur das unkomprimierte Videoformat (z. b. NV12), wie bei der Software Decodierung.
-   Das Verfahren zum Konfigurieren der Zugriffstaste hat sich geändert. In DXVA 1,0 ruft der Decoder **Execute** mit einer **DXVA \_ configpicturedecode** -Struktur auf, um den accerlator zu konfigurieren. In DXVA 2,0 verwendet der Decoder die [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) -Schnittstelle, wie im nächsten Abschnitt beschrieben.
-   Der Decoder ordnet die nicht komprimierten Puffer zu. Der Videorenderer ordnet sie nicht mehr zu.
-   Anstelle des Aufrufs von [**iamvideoaccelerator::D isplayframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-displayframe) , um den decodierten Frame anzuzeigen, übergibt der Decoder den Frame an den Renderer, indem er [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive)anruft, wie beim Debuggen von Software.
-   Der Decoder ist nicht mehr dafür verantwortlich, zu überprüfen, wann Datenpuffer für Updates sicher sind. Daher weist DXVA 2,0 keine Methode auf, die [**iamvideoaccelerator:: queryrenderstatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus)entspricht.
-   Die unter Bild Mischung erfolgt durch den Videorenderer mithilfe der DXVA 2.0-Videoprozessor-APIs. Decoderer, die Teilbilder bereitstellen (z. b. DVD-Decoders), sollten Teil Bilddaten an eine separate Ausgabe-PIN senden.

Für Decodierungs Vorgänge verwendet DXVA 2,0 die gleichen Datenstrukturen wie DXVA 1,0.

Der EVR-Filter (Enhanced Video Renderer) unterstützt DXVA 2,0. Die Filter für die Video Mischung Renderer (VMR-7 und VMR-9) unterstützen nur DXVA 1,0.

## <a name="finding-a-decoder-configuration"></a>Suchen einer decoderkonfiguration

Nachdem der Decoder den Ausgabe Medientyp aushandiert hat, muss er eine kompatible Konfiguration für das DXVA-Decodergerät finden. Sie können diesen Schritt innerhalb der [**cbaseoutputpin:: completeconnect**](../directshow/cbaseoutputpin-completeconnect.md) -Methode der Ausgabe-PIN ausführen. Mit diesem Schritt wird sichergestellt, dass der Grafiktreiber die vom Decoder benötigten Funktionen unterstützt, bevor der Decoder die Verwendung von DXVA committet.

Gehen Sie folgendermaßen vor, um eine Konfiguration für das Decoder-Gerät zu finden:

1.  Fragen Sie die Eingabe-PIN des Renderers für die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle ab.
2.  Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , um einen Zeiger auf die [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) -Schnittstelle zu erhalten. Die Dienst-GUID ist der Mr- \_ Video \_ Acceleration \_ Service.
3.  Wenn Sie [**IDirect3DDeviceManager9:: opentovicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle) aufzurufen, erhalten Sie ein Handle für das Direct3D-Gerät des Renderers.
4.  Aufrufen von [**IDirect3DDeviceManager9:: getvideoservice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) und übergeben des Geräte Handles. Diese Methode gibt einen Zeiger auf die [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) -Schnittstelle zurück.
5.  Aufrufen von [**idirectxvideodecoderservice:: getdecoderdeviceguids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderdeviceguids). Diese Methode gibt ein Array von Decoder-Geräte-GUIDs zurück.
6.  Durchlaufen Sie das Array von decoderguids, um diejenigen zu finden, die der Decoder-Filter unterstützt. Für einen MPEG-2-Decoder würden Sie z. b. nach **DXVA2 \_ ModeMPEG2 \_ mucomp**, **DXVA2 \_ ModeMPEG2 \_ IDCT** oder **DXVA2 \_ ModeMPEG2 \_ VLD** suchen.

7.  Wenn Sie eine Geräte-GUID für den Kandidaten Decoder finden, übergeben Sie die GUID an die [**idirectxvideodecoderservice:: getdecoderrendertargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderrendertargets) -Methode. Diese Methode gibt ein Array von renderzielformaten zurück, die als **D3DFORMAT** -Werte angegeben werden.
8.  Durchlaufen Sie die renderzielformate, und suchen Sie nach einem, das Ihrem Ausgabeformat entspricht. In der Regel unterstützt ein Decoder-Gerät ein einzelnes renderzielformat. Der Decoderfilter sollte mithilfe dieses unter Typs eine Verbindung mit dem Renderer herstellen. Beim ersten Aufrufe von [**completeconnect**](../directshow/cbaseoutputpin-completeconnect.md)kann der Decoder das renderzielformat determinimieren und dieses Format dann als bevorzugten Ausgabetyp zurückgeben.

9.  Aufrufen von [**idirectxvideodecoderservice:: getdecoderkonfigurationen**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-getdecoderconfigurations). Übergeben Sie dieselbe Decoder-Geräte-GUID, zusammen mit einer [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) -Struktur, die das vorgeschlagene Format beschreibt. Die-Methode gibt ein Array von [**DXVA2 \_ configpicturedecode**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_configpicturedecode) -Strukturen zurück. Jede Struktur beschreibt eine mögliche Konfiguration für das Decoder-Gerät.

10. Wenn Sie davon ausgehen, dass die vorherigen Schritte erfolgreich ausgeführt wurden, speichern Sie das Direct3D-Geräte handle, die Decoder-Geräte-GUID und die Konfigurations Struktur. Der Filter verwendet diese Informationen zum Erstellen des Decoder-Geräts.

Der folgende Code zeigt, wie Sie eine decoderkonfiguration suchen.


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



Da dieses Beispiel generisch ist, wurde ein Teil der Logik in Hilfsfunktionen eingefügt, die vom Decoder implementiert werden müssen. Der folgende Code zeigt die Deklarationen für diese Funktionen:


```C++
// Returns TRUE if the decoder supports a given decoding mode.
BOOL IsSupportedDecoderMode(const GUID& mode);

// Returns TRUE if the decoder supports a given decoding configuration.
BOOL IsSupportedDecoderConfig(const DXVA2_ConfigPictureDecode& config);

// Fills in a DXVA2_VideoDesc structure based on the input format.
void FillInVideoDescription(DXVA2_VideoDesc *pDesc);
```



## <a name="notifying-the-video-renderer"></a>Benachrichtigen des Videorenderers

Wenn der Decoder eine decoderkonfiguration findet, besteht der nächste Schritt darin, den Videorenderer zu benachrichtigen, dass der Decoder die Hardwarebeschleunigung verwendet. Sie können diesen Schritt innerhalb der [**completeconnect**](../directshow/cbaseoutputpin-completeconnect.md) -Methode ausführen. Dieser Schritt muss ausgeführt werden, bevor der Zuweiser ausgewählt wird, da er sich auf die Auswahl der Zuweisung auswirkt.

1.  Fragen Sie die Eingabe-PIN des Renderers für die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle ab.
2.  Aufrufen von [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) , um einen Zeiger auf die [**idirectxvideomemoryconfiguration**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideomemoryconfiguration) -Schnittstelle zu erhalten. Die Dienst-GUID ist der **Mr- \_ Video \_ Acceleration \_ Service**.
3.  Aufrufen von [**idirectxvideomemoryconfiguration:: getavailablesurfacetypeer byindex**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-getavailablesurfacetypebyindex) in einer Schleife, um die *dwtypeindex* -Variable von NULL zu erhöhen. Beenden Sie, wenn die Methode den Wert **DXVA2 \_ surfacetype \_ decoderrendertarget** im *pdwtype* -Parameter zurückgibt. Mit diesem Schritt wird sichergestellt, dass der Videorenderer die hardwarebeschleunigte Decodierung unterstützt. Dieser Schritt ist für den EVR-Filter immer erfolgreich.
4.  Wenn der vorherige Schritt erfolgreich war, nennen Sie [**idirectxvideomemoryconfiguration:: setsurfacetype**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideomemoryconfiguration-setsurfacetype) mit dem Wert DXVA2 \_ surfacetype \_ decoderrendertarget. Durch den Aufruf von **setsurfaketype** mit diesem Wert wird der Videorenderer in den DXVA-Modus versetzt. Wenn sich der Videorenderer in diesem Modus befindet, muss der Decoder seine eigene Zuweisung bereitstellen.

Der folgende Code zeigt, wie Sie den Videorenderer benachrichtigen.


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



Wenn der Decoder eine gültige Konfiguration findet und den Videorenderer erfolgreich benachrichtigt, kann der Decoder DXVA für die Decodierung verwenden. Der Decoder muss eine benutzerdefinierte Zuweisung für seine Ausgabe-PIN implementieren, wie im nächsten Abschnitt beschrieben.

## <a name="allocating-uncompressed-buffers"></a>Zuordnen von nicht komprimierten Puffern

In DXVA 2,0 ist der Decoder für das Zuordnen von Direct3D-Oberflächen zur Verwendung als nicht komprimierte Video Puffer verantwortlich. Daher muss der Decoder einen benutzerdefinierten Zuweiser implementieren, der die Oberflächen erstellt. Die von dieser Zuweisung bereitgestellten Medien Beispiele enthalten Zeiger auf die Direct3D-Oberflächen. Der EVR Ruft einen Zeiger auf die-Oberfläche ab, indem er [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) im Medien Beispiel aufruft. Der Dienst Bezeichner ist der **Mr- \_ Puffer \_ Dienst**.

Führen Sie die folgenden Schritte aus, um die benutzerdefinierte Zuweisung bereitzustellen:

1.  Definieren Sie eine Klasse für die Medien Beispiele. Diese Klasse kann von der [**cmediasample**](../directshow/cmediasample.md) -Klasse abgeleitet werden. Führen Sie in dieser Klasse die folgenden Schritte aus:
    -   Speichert einen Zeiger auf die Direct3D-Oberfläche.
    -   Implementieren Sie die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle. Fragen Sie in der [**GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) -Methode, wenn es sich bei der Dienst-GUID um den **\_ Puffer \_ Dienst** handelt, die Direct3D-Oberfläche nach der angeforderten Schnittstelle Andernfalls kann **GetService** den **\_ \_ nicht unterstützten MF- \_ Dienst** zurückgeben.
    -   Überschreiben Sie die [**cmediasample:: getpointer**](../directshow/cmediasample-getpointer.md) -Methode, um E \_ notimpl zurückzugeben.
2.  Definieren Sie eine Klasse für die Zuweisung. Die Zuweisung kann von der [**cbasezucator**](../directshow/cbaseallocator.md) -Klasse abgeleitet werden. Führen Sie in dieser Klasse die folgenden Schritte aus:
    -   Überschreiben Sie die [**cbasezucator:: zugsc**](../directshow/cbaseallocator-alloc.md) -Methode. Rufen Sie in dieser Methode [**idirectxvideoaccelerationservice:: CreateSurface**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoaccelerationservice-createsurface) auf, um die Oberflächen zu erstellen. (Die [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) -Schnittstelle erbt diese Methode von [**idirectxvideoaccelerationservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoaccelerationservice).)
    -   Überschreiben Sie die [**cbasezucator:: Free**](../directshow/cbaseallocator-free.md) -Methode, um die Oberflächen freizugeben.
3.  Überschreiben Sie in der Ausgabe-PIN Ihres Filters die [**cbaseoutputpin:: init-**](../directshow/cbaseoutputpin-initallocator.md) Methode. Erstellen Sie innerhalb dieser Methode eine Instanz Ihrer benutzerdefinierten Zuweisung.
4.  Implementieren Sie in Ihrem Filter die [**ctransformfilter::D ecidebuffersize**](../directshow/ctransformfilter-decidebuffersize.md) -Methode. Der *pproperties* -Parameter gibt die Anzahl der für das EVR erforderlichen Oberflächen an. Fügen Sie diesem Wert die Anzahl der vom Decoder benötigten Oberflächen hinzu, und nennen Sie [**imemzuzucator:: SetProperties**](/windows/win32/api/strmif/nf-strmif-imemallocator-setproperties) für die Zuweisung.

Der folgende Code zeigt, wie die Beispiel Klasse "Media" implementiert wird:


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



Der folgende Code zeigt, wie die [**Zuordnungsmethode**](../directshow/cbaseallocator-alloc.md) für die Zuweisung implementiert wird.


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



Dies ist der Code für die [**Free**](../directshow/cbaseallocator-free.md) -Methode:


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



Weitere Informationen zum Implementieren von benutzerdefinierten Zuweisungen finden Sie im Thema [Bereitstellen einer benutzerdefinierten Zuweisung](../directshow/providing-a-custom-allocator.md) in der DirectShow-SDK-Dokumentation.

## <a name="decoding"></a>Decodierung

Um das Decoder-Gerät zu erstellen, rufen Sie [**idirectxvideodecoderservice:: createvideodecoder**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoderservice-createvideodecoder)auf. Die-Methode gibt einen Zeiger auf die [**idirectxvideodecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) -Schnittstelle des Decoder-Geräts zurück.

Bei jedem Frame wird [**IDirect3DDeviceManager9:: testdevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-testdevice) aufgerufen, um das Geräte Handle zu testen. Wenn sich das Gerät geändert hat, gibt die Methode DXVA2 \_ E \_ New \_ Video Device zurück \_ . Wenn dies der Fall ist, gehen Sie wie folgt vor:

1.  Schließen Sie das Geräte Handle durch Aufrufen von [**IDirect3DDeviceManager9:: closedevicehandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-closedevicehandle).
2.  Geben Sie die Zeiger [**idirectxvideodecoderservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoderservice) und [**idirectxvideodecoder**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideodecoder) frei.
3.  Öffnen Sie ein neues Geräte handle.
4.  Aushandeln Sie eine neue decoderkonfiguration, wie im Abschnitt Suchen [einer decoderkonfiguration](#finding-a-decoder-configuration)beschrieben.
5.  Erstellen Sie ein neues Decoder-Gerät.

Wenn das Geräte Handle gültig ist, funktioniert der Decodierungs Prozess wie folgt:

1.  Aufrufen von [**idirectxvideodecoder:: beginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe).
2.  Führen Sie die folgenden Schritte aus:
    1.  Aufrufen von [**idirectxvideodecoder:: GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) zum Abrufen eines DXVA-decoderpuffers.
    2.  Füllen Sie den Puffer aus.
    3.  Nennen Sie [**idirectxvideodecoder:: ReleaseBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-releasebuffer).
3.  Nennen Sie [**idirectxvideodecoder:: Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) , um die Decodierungs Vorgänge für den Frame auszuführen.

DXVA 2,0 verwendet die gleichen Datenstrukturen wie DXVA 1,0 für Decodierungs Vorgänge. Für den ursprünglichen Satz von DXVA-Profilen (für h. 261, h. 263 und MPEG-2) werden diese Datenstrukturen in der [Spezifikation DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration)beschrieben.

In jedem Paar von [**beginFrame**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-beginframe)- / [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) -aufrufen können Sie [**GetBuffer**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-getbuffer) mehrmals aufrufen, aber nur einmal für jeden DXVA-Puffer. Wenn Sie es zweimal mit dem gleichen Puffertyp aufzurufen, überschreiben Sie die Daten.

Rufen Sie nach dem Aufrufen von [**Execute**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideodecoder-execute) [**IMemInputPin:: Receive**](/windows/win32/api/strmif/nf-strmif-imeminputpin-receive) auf, um den Frame an den Videorenderer zu übermitteln, wie bei der Software Decodierung. Die **Receive** -Methode ist asynchron. nach dem zurückkehren kann der Decoder den nächsten Frame Decodierungs Vorgang fortsetzen. Der Anzeigetreiber verhindert, dass Decodierungs Befehle den Puffer überschreiben, während der Puffer verwendet wird. Der Decoder sollte keine Oberfläche wieder verwenden, um einen anderen Frame zu decodieren, bis der Renderer das Beispiel freigegeben hat. Wenn der Renderer das Beispiel freigibt, fügt die Zuweisung das Beispiel wieder in den Pool der verfügbaren Beispiele ein. Rufen Sie zum Abrufen des nächsten verfügbaren Beispiels [**cbaseoutputpin:: getdeliverybuffer**](../directshow/cbaseoutputpin-getdeliverybuffer.md)auf, das wiederum [**imemzuzukator:: GetBuffer**](/windows/win32/api/strmif/nf-strmif-imemallocator-getbuffer)aufruft. Weitere Informationen finden Sie im Thema [Übersicht über den Datenfluss in DirectShow](../directshow/overview-of-data-flow-in-directshow.md) in der DirectShow-Dokumentation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md)
</dt> </dl>

 

 
