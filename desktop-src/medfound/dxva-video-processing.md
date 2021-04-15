---
description: Die DXVA-Videoverarbeitung kapselt die Funktionen der Grafikhardware, die für die Verarbeitung von nicht komprimierten Videobildern verwendet werden. Die Video Verarbeitungsdienste umfassen Deinterlacing und Video Mischung.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: DXVA-Video Verarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524544"
---
# <a name="dxva-video-processing"></a>DXVA-Video Verarbeitung

Die DXVA-Videoverarbeitung kapselt die Funktionen der Grafikhardware, die für die Verarbeitung von nicht komprimierten Videobildern verwendet werden. Die Video Verarbeitungsdienste umfassen Deinterlacing und Video Mischung.

Dieses Thema enthält folgende Abschnitte:

-   [Übersicht](#overview)
-   [Erstellen eines Video Verarbeitungs Geräts](#creating-a-video-processing-device)
    -   [Get the idirectxvideoprocess orservice-Zeiger](#get-the-idirectxvideoprocessorservice-pointer)
    -   [Auflisten der Video Verarbeitungsgeräte](#enumerate-the-video-processing-devices)
    -   [Render-Target Formate aufzählen](#enumerate-render-target-formats)
    -   [Abfragen der Gerätefunktionen](#query-the-device-capabilities)
    -   [Erstellen des Geräts](#create-the-device)
-   [Video Prozess Blit](#video-process-blit)
    -   [Blit-Parameter](#blit-parameters)
    -   [Eingabe Beispiele](#input-samples)
-   [Bildkomposition](#image-composition)
    -   [Beispiel 1: Briefkasten](#example-1-letterboxing)
    -   [Beispiel 2: Stretching von substreamimages](#example-2-stretching-substream-images)
    -   [Beispiel 3: nicht übereinstimmende streamhöhen](#example-3-mismatched-stream-heights)
    -   [Beispiel 4: Ziel Rechteck kleiner als Ziel Oberfläche](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [Beispiel 5: Quell Rechtecke](#example-5-source-rectangles)
    -   [Beispiel 6: überschneidende Ziel Rechtecke](#example-6-intersecting-destination-rectangles)
    -   [Beispiel 7: Stretching und Zuschneiden von Videos](#example-7-stretching-and-cropping-video)
-   [Eingabe Beispiel Reihenfolge](#input-sample-order)
    -   [Beispiel 1](#example-1-letterboxing)
    -   [Beispiel 2](#example-2-stretching-substream-images)
    -   [Beispiel 3](#example-3-mismatched-stream-heights)
    -   [Beispiel 4](#example-4-target-rectangle-smaller-than-destination-surface)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Grafikhardware kann die GPU (Graphics Processing Unit) zum Verarbeiten von nicht komprimierten Videobildern verwenden. Bei einem *Video Verarbeitungs* Gerät handelt es sich um eine Softwarekomponente, die diese Funktionen kapselt. Anwendungen können ein Video Verarbeitungs Gerät zum Ausführen von Funktionen verwenden, wie z. b.:

-   Deinterlacing und Inverse Telecine
-   Mischen von videosubstreams auf das Hauptvideo Bild
-   Farbanpassung (ProcAmp) und Bildfilterung
-   Bildskalierung
-   Farb Raum Konvertierung
-   Alpha Blending

Das folgende Diagramm zeigt die Phasen in der Video Verarbeitungs Pipeline. Das Diagramm soll keine tatsächliche Implementierung darstellen. Beispielsweise kann der Grafiktreiber mehrere Stufen zu einem einzigen Vorgang zusammenfassen. Alle diese Vorgänge können mit einem einzelnen-Befehl für das Video Verarbeitungs Gerät durchgeführt werden. Einige der hier gezeigten Phasen, z. b. das Filtern von Filtern und Filtern, werden möglicherweise nicht vom Treiber unterstützt.

![das Diagramm zeigt die Phasen der DXVA-Videoverarbeitung an.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

Die Eingabe für die Video Verarbeitungs Pipeline enthält immer einen *primären* Videostream, der die Daten des Haupt Bilds enthält. Der primäre Videostream bestimmt die Framerate für das Ausgabevideo. Jeder Frame des Ausgabevideos wird relativ zu den Eingabedaten aus dem primären Videostream berechnet. Pixel im primären Stream sind immer transparent, ohne Pixel-Alpha-Daten. Der primäre Videostream kann progressiv oder mit Zeilen Sprung sein.

Optional kann die Video Verarbeitungs Pipeline bis zu 15 videosubstreams empfangen. Ein unter Datenstrom enthält zusätzliche Bilddaten, z. b. geschlossene Beschriftungen oder DVD-Teilbilder. Diese Bilder werden über den primären Videostream angezeigt und sind im Allgemeinen nicht für sich selbst zu sehen. Substreambilder können Alpha Daten pro Pixel enthalten und sind immer progressive Frames. Das Video für die Videoverarbeitung verbindet die substreambilder mit dem aktuellen deintercherungs-Frame aus dem primären Videostream.

Im restlichen Teil dieses Themas wird der Begriff *Bild* für die Eingabedaten für ein Video Verarbeitungs Gerät verwendet. Ein Bild kann aus einem progressiven Frame, einem einzelnen Feld oder zwei verschachtelten Feldern bestehen. Die Ausgabe ist immer ein Deinterlacing-Frame.

Ein Videotreiber kann mehr als ein Video Verarbeitungs Gerät implementieren, um unterschiedliche Sätze von Video Verarbeitungsfunktionen bereitzustellen. Geräte werden anhand der GUID identifiziert. Die folgenden GUIDs sind vordefiniert:

-   **DXVA2 \_ Videoprocbobdevice**. Dieses Gerät führt Bob Deinterlacing aus.
-   **DXVA2 \_ Videoprocprogressivedevice**. Dieses Gerät wird verwendet, wenn das Video nur progressive Frames ohne Zeilen Sprung enthält. (Einige Videoinhalte enthalten eine Mischung aus progressiven und Zeilen Sprung enden Frames. Das progressive Gerät kann nicht für diese Art von "gemischtem" Videoinhalt verwendet werden, da für die Zeilen Sprung Rahmen ein Deinterlacing-Schritt erforderlich ist.)

Jeder Grafiktreiber, der die DXVA-Videoverarbeitung unterstützt, muss mindestens diese beiden Geräte implementieren. Der Grafiktreiber kann auch andere Geräte bereitstellen, die durch Treiber spezifische GUIDs identifiziert werden. Ein Treiber könnte z. b. einen proprietären deinterlacingalgorithmus implementieren, der eine bessere Qualitäts Ausgabe als Bob Deinterlacing erzeugt. Einige deinterlacingalgorithmen erfordern möglicherweise Forward-oder rückwärts Verweis Bilder aus dem primären Datenstrom. Wenn dies der Fall ist, muss der Aufrufer diese Bilder dem Treiber in der richtigen Reihenfolge bereitstellen, wie weiter unten in diesem Abschnitt beschrieben.

Außerdem wird ein Referenz Software-Gerät bereitgestellt. Das Software Gerät ist für die Qualität und nicht für die Geschwindigkeit optimiert und eignet sich möglicherweise nicht für die Echt Zeit Videoverarbeitung. Das Referenz Software Gerät verwendet den GUID-Wert DXVA2 \_ videoprocsoftwaredevice.

## <a name="creating-a-video-processing-device"></a>Erstellen eines Video Verarbeitungs Geräts

Vor der Verwendung der DXVA-Videoverarbeitung muss von der Anwendung ein Video Verarbeitungs Gerät erstellt werden. Im folgenden finden Sie eine kurze Übersicht über die Schritte, die im restlichen Teil dieses Abschnitts ausführlicher erläutert werden:

1.  Einen Zeiger auf die [**idirectxvideoprocess orservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) -Schnittstelle erhalten.
2.  Erstellen Sie eine Beschreibung des Video Formats für den primären Videostream. Verwenden Sie diese Beschreibung, um eine Liste der Video Verarbeitungsgeräte zu erhalten, die das Videoformat unterstützen. Geräte werden anhand der GUID identifiziert.
3.  Für ein bestimmtes Gerät wird eine Liste der vom Gerät unterstützten renderzielformate angezeigt. Die Formate werden als Liste von **D3DFORMAT** -Werten zurückgegeben. Wenn Sie das Mischen von Substreams planen, können Sie auch eine Liste der unterstützten substreamformate erhalten.
4.  Fragen Sie die Funktionen der einzelnen Geräte ab.
5.  Erstellen Sie das Video für die Verarbeitung von Geräten.

Manchmal können Sie einige dieser Schritte weglassen. Anstatt z. b. die Liste der renderzielformate zu erhalten, können Sie einfach versuchen, das Video Verarbeitungs Gerät in Ihrem bevorzugten Format zu erstellen, und überprüfen, ob es erfolgreich ist. Ein gängiges Format, z \_ . b. D3DFMT X8R8G8B8, ist wahrscheinlich erfolgreich.

Im restlichen Teil dieses Abschnitts werden diese Schritte ausführlich beschrieben.

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a>Get the idirectxvideoprocess orservice-Zeiger

Die [**idirectxvideoprocess orservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) -Schnittstelle wird vom Direct3D-Gerät abgerufen. Es gibt zwei Möglichkeiten, einen Zeiger auf diese Schnittstelle zu erhalten:

-   Von einem Direct3D-Gerät aus.
-   Aus dem [Direct3D-Device Manager](direct3d-device-manager.md).

Wenn Sie einen Zeiger auf ein Direct3D-Gerät haben, können Sie einen [**idirectxvideoprocess orservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) -Zeiger abrufen, indem Sie die [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) -Funktion aufrufen. Übergeben Sie einen Zeiger auf die **IDirect3DDevice9** -Schnittstelle des Geräts, und geben Sie **IID \_ idirectxvideoprocess orservice** für den *riid* -Parameter an, wie im folgenden Code gezeigt:


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



in einigen Fällen wird das Direct3D-Gerät von einem Objekt erstellt und dann über das [Direct3D-Device Manager](direct3d-device-manager.md)mit anderen Objekten geteilt. In dieser Situation können Sie [**IDirect3DDeviceManager9:: getvideoservice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) auf dem Geräte-Manager aufrufen, um den [**idirectxvideoprocess orservice**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) -Zeiger abzurufen, wie im folgenden Code gezeigt:


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a>Auflisten der Video Verarbeitungsgeräte

Um eine Liste der Video Verarbeitungsgeräte zu erhalten, geben Sie eine [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) -Struktur mit dem Format des primären Videostreams ein, und übergeben Sie diese Struktur an die [**idirectxvideoprocess orservice:: getvideoprocess ordeviceguids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) -Methode. Die-Methode gibt ein Array von GUIDs zurück, eines für jedes Video Verarbeitungs Gerät, das in diesem Videoformat verwendet werden kann.

Stellen Sie sich eine Anwendung vor, die einen Videostream im im YUY2-Format rendert, indem Sie die BT. 709-Definition von YUV Color mit einer Frame Rate von 29,97 Frames pro Sekunde verwendet. Nehmen Sie an, dass der Videoinhalt vollständig aus progressiven Frames besteht. Das folgende Code Fragment zeigt, wie Sie die Formatbeschreibung ausfüllen und die Geräte-GUIDs erhalten:


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



Der Code für dieses Beispiel stammt aus dem [DXVA2 \_ videoproc](dxva2-videoproc-sample.md) SDK-Beispiel.

Das *pguids* -Array in diesem Beispiel wird von der [**getvideoprocess ordeviceguids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) -Methode zugeordnet, sodass die Anwendung das Array durch Aufrufen von [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)freigeben muss. Die verbleibenden Schritte können mithilfe der von dieser Methode zurückgegebenen Geräte-GUIDs ausgeführt werden.

### <a name="enumerate-render-target-formats"></a>Render-Target Formate aufzählen

Um die Liste der vom Gerät unterstützten renderzielformate zu erhalten, übergeben Sie die Geräte-GUID und die [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) -Struktur an die [**idirectxvideoprocess orservice:: getvideoprocesorrendertargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) -Methode, wie im folgenden Code gezeigt:


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



Die-Methode gibt ein Array von **D3DFORMAT** -Werten zurück. In diesem Beispiel, in dem der Eingabetyp "im YUY2" ist, kann eine typische Liste von Formaten D3DFMT \_ X8R8G8B8 (32 Bit RGB) und D3DMFT \_ im YUY2 (Eingabeformat) sein. Die genaue Liste hängt jedoch vom Treiber ab.

Die Liste der verfügbaren Formate für die untergeordneten Datenströme kann je nach Format des Renderziels und des Eingabe Formats variieren. Um die Liste der substreamformate zu erhalten, übergeben Sie die Geräte-GUID, die Format Struktur und das renderzielformat an die [**idirectxvideoprocess orservice:: getvideoprocesorsubstreamformats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) -Methode, wie im folgenden Code gezeigt:


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



Diese Methode gibt ein weiteres Array von **D3DFORMAT** -Werten zurück. Typische substreamformate sind ayuv und AI44.

### <a name="query-the-device-capabilities"></a>Abfragen der Gerätefunktionen

Wenn Sie die Funktionen eines bestimmten Geräts nutzen möchten, übergeben Sie die Geräte-GUID, die Format Struktur und ein renderzielformat an die [**idirectxvideoprocess orservice:: getvideoprocess orcaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) -Methode. Die-Methode füllt eine [**DXVA2 \_ videoprocess orcaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) -Struktur Struktur mit den Gerätefunktionen auf.


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a>Erstellen des Geräts

Um das Video Processing-Gerät zu erstellen, rufen Sie [**idirectxvideoprocessorservice:: "kreatevideoprocessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor)" auf. Die Eingabe für diese Methode ist die Geräte-GUID, die Formatbeschreibung, das renderzielformat und die maximale Anzahl der zu mischenden Substreams. Die-Methode gibt einen Zeiger auf die [**idirectxvideoprocessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) -Schnittstelle zurück, die das Video Verarbeitungs Gerät darstellt.


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a>Video Prozess Blit

Der Hauptvideo Verarbeitungsvorgang ist das *Video Processing Blit*. (Ein *Blit* ist jeder Vorgang, bei dem zwei oder mehr Bitmaps zu einer einzelnen Bitmap kombiniert werden. Ein Video Processing Blit kombiniert Eingabe Bilder, um einen Ausgabe Frame zu erstellen.) Um ein Blit für die Videoverarbeitung auszuführen, nennen Sie [**idirectxvideoprocessor:: videoprocessblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt). Diese Methode übergibt eine Reihe von Videobeispielen an das Video Verarbeitungs Gerät. Als Antwort verarbeitet das Video Verarbeitungs Gerät die Eingabe Bilder und generiert einen Ausgabe Frame. Die Verarbeitung kann Deinterlacing, Farb Raum Konvertierung und unter Datenstrom-Vermischung einschließen. Die Ausgabe wird auf eine vom Aufrufer bereitgestellte Ziel Oberfläche geschrieben.

Die [**videoprocess BLT**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) -Methode übernimmt die folgenden Parameter:

-   *PRT* verweist auf eine **IDirect3DSurface9** -Renderziel-Oberfläche, die den verarbeiteten Videorahmen empfängt.
-   *pbltparameams* verweist auf eine [**DXVA2 \_ videoprocess bltparameams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) -Struktur, die die Parameter für den Blit angibt.
-   *psamples* ist die Adresse eines Arrays von [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Strukturen. Diese Strukturen enthalten die Eingabe Beispiele für den Blit.
-   *NumSamples* gibt die Größe des *psamples* -Arrays an.
-   Der *reservierte* Parameter ist reserviert und sollte auf **null** festgelegt werden.

Im *psamples* -Array muss der Aufrufer die folgenden Eingabe Beispiele bereitstellen:

-   Das aktuelle Bild aus dem primären Videostream.
-   Vorwärts-und rückwärts Verweis Bilder, wenn dies für den Deinterlacing-Algorithmus erforderlich ist.
-   0 (null) oder mehr substreambilder, maximal 15 unter Ströme.

Der Treiber erwartet, dass dieses Array in einer bestimmten Reihenfolge angezeigt wird, wie in der [Eingabe Stichprobe-Reihenfolge](#input-sample-order)beschrieben.

### <a name="blit-parameters"></a>Blit-Parameter

Die [**DXVA2 \_ videoprocess bltparameams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) -Struktur enthält allgemeine Parameter für den Blit. Die wichtigsten Parameter werden in den folgenden Membern der-Struktur gespeichert:

-   **TargetFrame** ist die Präsentationszeit des Ausgabe Frames. Bei progressivem Inhalt muss dieser Zeitrahmen der Startzeit für den aktuellen Frame aus dem primären Videostream entsprechen. Diese Zeit wird im **StartMember** der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur für dieses Eingabe Beispiel angegeben.

    Beim Zeilen Sprung Inhalt erzeugt ein Frame mit zwei verschachtelten Feldern zwei Deinterlacing-Ausgabe Frames. Beim ersten Ausgabe Frame muss die Präsentationszeit mit der Startzeit des aktuellen Bilds im primären Videostream identisch sein, ebenso wie progressiver Inhalt. Im zweiten Ausgabe Frame muss die Startzeit der Mitte zwischen der Startzeit des aktuellen Bilds im primären Videostream und der Startzeit des nächsten Bilds im Stream entsprechen. Wenn das Eingabe Video z. b. 25 Frames pro Sekunde (50 Felder pro Sekunde) ist, haben die Ausgabe Rahmen die in der folgenden Tabelle angezeigten Zeitstempel. Zeitstempel werden in Einheiten von 100 Nanosekunden angezeigt.

    

    | Eingabebild | **TargetFrame** (1) | **TargetFrame** (2) |
    |---------------|---------------------|---------------------|
    | 0             | 0                   | 200.000              |
    | 400000        | 0                   | 600000              |
    | 800000        | 800000              | 1000000             |
    | 1,2 Millionen       | 1,2 Millionen             | 1,4 Millionen             |

    

     

    Wenn der Zeilen Sprung Inhalt aus einzelnen Feldern anstelle von verschachtelten Feldern besteht, entsprechen die Ausgabe Zeiten immer den Eingabe Zeiten, wie bei progressivem Inhalt.

-   **Targetrect** definiert einen rechteckigen Bereich innerhalb der Ziel Oberfläche. Die Ausgabe wird von Blit in diese Region geschrieben. Insbesondere wird jedes Pixel innerhalb von **targetrect** geändert, und es werden keine Pixel außerhalb von **targetrect** geändert. Das Ziel Rechteck definiert das Begrenzungs Rechteck für alle eingabevideostreams. Die Platzierung einzelner Streams innerhalb dieses Rechtecks wird über den *psamples* -Parameter von [**idirectxvideoprocessor:: videoprocessblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)gesteuert.
-   **BackgroundColor** gibt die Hintergrundfarbe an, wo kein Video Bild angezeigt wird. Wenn z. b. ein Video mit einer Größe von 16 x 9 in einem 4 x 3-Bereich (Letterboxing) angezeigt wird, werden die in einem Briefkasten enthaltenen Bereiche mit der Hintergrundfarbe angezeigt. Die Hintergrundfarbe ist nur innerhalb des Ziel Rechtecks (**targetrect**) anwendbar. Alle Pixel außerhalb von **targetrect** werden nicht geändert.
-   **Destformat** beschreibt den Farbraum für das Ausgabevideo – beispielsweise, ob die Farbe "ITU-R BT. 709" oder "BT. 601" verwendet wird. Diese Informationen können sich darauf auswirken, wie das Bild angezeigt wird. Weitere Informationen finden Sie unter [Erweiterte Farbinformationen](extended-color-information.md).

Andere Parameter werden auf der Referenzseite für die [**DXVA2 \_ videoprocess bltparameams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) -Struktur beschrieben.

### <a name="input-samples"></a>Eingabe Beispiele

Der *psamples* -Parameter von [**idirectxvideoprocessor:: videoprocessblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) verweist auf ein Array von [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Strukturen. Jede dieser Strukturen enthält Informationen zu einem Eingabe Beispiel und einen Zeiger auf die Direct3D-Oberfläche, die das Beispiel enthält. Jedes Beispiel ist einer der folgenden:

-   Das aktuelle Bild aus dem primären Datenstrom.
-   Ein vorwärts-oder rückwärts Verweis Bild aus dem primären Stream, das für Deinterlacing verwendet wird.
-   Ein substreambild.

Die genaue Reihenfolge, in der die Stichproben im Array angezeigt werden müssen, wird später im Abschnitt [Eingabe Stichprobe-Reihenfolge](#input-sample-order)beschrieben.

Es können bis zu 15 substreambilder bereitgestellt werden, obwohl die meisten Videoanwendungen höchstens einen teilstream benötigen. Die Anzahl der untergeordneten Datenströme kann bei jedem Aufrufen von [**videoprocess BLT**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt)geändert werden. Substreambilder werden angezeigt, indem das **Sampleformat. Sampleformat** -Member der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur auf DXVA2 \_ samplesubstream festgelegt wird. Für den primären Videostream beschreibt dieser Member das Zeilen Sprung des Eingabe Videos. Weitere Informationen finden Sie unter [**DXVA2 \_ Sampleformat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) -Enumeration.

Für den primären Videostream geben die **Start** -und **Endelemente** der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur die Start-und Endzeiten der Eingabe Stichprobe an. Legen Sie für substreambilder diese Werte auf 0 (null) fest, da die Präsentationszeit immer aus dem primären Stream berechnet wird. Die Anwendung ist für die Nachverfolgung zuständig, wenn jedes subnetzbild präsentiert und zum richtigen Zeitpunkt an [**videoprocstinblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) übermittelt werden soll.

Zwei Rechtecke definieren, wie das Quellvideo für jeden Stream positioniert wird:

-   Der **srcRect** -Member der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur gibt das *Quell Rechteck* an, einem rechteckigen Bereich des Quell Bilds, der im zusammengesetzten Ausgabe Rahmen angezeigt wird. Legen Sie diese Einstellung auf einen Wert fest, der kleiner als die Frame Größe ist, um das Bild zu zuschneiden Legen Sie andernfalls die Größe der Frame Größe fest.
-   Der **dstrect** -Member der gleichen Struktur gibt das *Ziel Rechteck* an, einen rechteckigen Bereich der Ziel Oberfläche, auf dem der Videoframe angezeigt wird.

Der Treiber blitet Pixel aus dem Quell Rechteck in das Ziel Rechteck. Die zwei Rechtecke können unterschiedliche Größen oder Seitenverhältnisse aufweisen. der Treiber skaliert das Image nach Bedarf. Außerdem kann jeder Eingabedaten Strom einen anderen Skalierungsfaktor verwenden. Tatsächlich kann eine Skalierung erforderlich sein, um das richtige Seitenverhältnis im Ausgabe Rahmen zu schaffen. Der Treiber übernimmt nicht das Pixel Seitenverhältnis der Quelle. wenn das Quell Image also nicht quadratische Pixel verwendet, liegt es an der Anwendung, das richtige Ziel Rechteck zu berechnen.

Die bevorzugten substreamformate sind ayuv und AI44. Letzteres ist ein Palettenformat mit 16 Farben. Paletteneinträge werden im **PAL** -Member der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur angegeben. (Wenn das Quellvideo Format ursprünglich als Media Foundation Medientyp ausgedrückt wird, werden die Paletteneinträge im [**MF \_ MT- \_ palettenattribut**](mf-mt-palette-attribute.md) gespeichert.) Deaktivieren Sie dieses Array bei nicht-palettenformaten auf 0 (null).

## <a name="image-composition"></a>Bildkomposition

Jeder Blit-Vorgang wird durch die folgenden drei Rechtecke definiert:

-   Das *Ziel* Rechteck (**targetrect**) definiert den Bereich innerhalb der Ziel Oberfläche, in dem die Ausgabe angezeigt wird. Das Ausgabe Bild wird auf dieses Rechteck zugeschnitten.
-   Das *Ziel* Rechteck für jeden Datenstrom (**dstrect**) definiert, wo der Eingabestream im zusammengesetzten Image angezeigt wird.
-   Das *Quell* Rechteck für jeden Stream (**srcRect**) definiert, welcher Teil des Quell Bilds angezeigt wird.

Die Ziel-und Ziel Rechtecke werden relativ zur Ziel Oberfläche angegeben. Das Quell Rechteck wird relativ zum Quell Abbild angegeben. Alle Rechtecke werden in Pixel angegeben.

![Diagramm, das Quell-, Ziel-und Ziel Rechtecke anzeigt](images/dxva-vp-rects.gif)

Der Video Verarbeitungs Gerät Alpha kombiniert die Eingabe Bilder und verwendet dabei eine der folgenden Quellen für Alpha Daten:

-   Pro-Pixel-Alpha Daten aus untergeordneten Datenströmen.
-   Ein planarer Alpha Wert für jeden Videostream, der im **planaralpha** -Member der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur angegeben ist.
-   Der planare Alpha Wert des zusammengesetzten Bilds, das im **Alpha** -Member der [**DXVA2 \_ videoprocess bltparameams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) -Struktur angegeben ist. Dieser Wert wird verwendet, um das gesamte zusammengesetzte Bild mit der Hintergrundfarbe zu kombinieren.

Dieser Abschnitt enthält eine Reihe von Beispielen, die zeigen, wie das Video Verarbeitungs Gerät das Ausgabe Image erstellt.

### <a name="example-1-letterboxing"></a>Beispiel 1: Briefkasten

In diesem Beispiel wird gezeigt, wie das Quell Abbild durch das Ziel Rechteck als kleiner als das Ziel Rechteck festgelegt wird. Der primäre Videostream in diesem Beispiel ist ein 720 × 480-Bild, das mit einem 16:9-Seitenverhältnis angezeigt werden soll. Die Ziel Oberfläche ist 640 × 480 Pixel (4:3 Seitenverhältnis). Um das richtige Seitenverhältnis zu erreichen, muss das Ziel Rechteck 640 × 360 sein. Der Einfachheit halber enthält dieses Beispiel keinen substream. Das folgende Diagramm zeigt die Quell-und Ziel Rechtecke.

![Diagramm, das Letterboxing anzeigt.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

Das vorangehende Diagramm zeigt die folgenden Rechtecke:

-   Ziel Rechteck: {0, 0, 640, 480}
-   Primäres Video:

    -   Quell Rechteck: {0, 0, 720, 480}
    -   Ziel Rechteck: {0, 60, 640, 420}

Der Treiber deinstalhnt das Video, verkleinert den deinterllingframe auf 640 × 360 und Blit den Frame in das Ziel Rechteck. Das Ziel Rechteck ist größer als das Ziel Rechteck, daher verwendet der Treiber die Hintergrundfarbe, um die horizontalen Balken oberhalb und unterhalb des Rahmens zu füllen. Die Hintergrundfarbe wird in der [**DXVA2 \_ videoprocess bltparameams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) -Struktur angegeben.

### <a name="example-2-stretching-substream-images"></a>Beispiel 2: Stretching von substreamimages

Substreambilder können über das primäre Video Bild hinaus erweitert werden. In DVD-Videos kann der primäre Videostream z. b. ein 4:3-Seitenverhältnis aufweisen, während der unter Datenstrom 16:9 ist. In diesem Beispiel verfügen beide Videostreams über die gleichen Quell Dimensionen (720 × 480), der unter Datenstrom sollte jedoch mit einem 16:9-Seitenverhältnis angezeigt werden. Um dieses Seitenverhältnis zu erreichen, wird das substreambild horizontal gestreckt. Die Quell-und Ziel Rechtecke werden im folgenden Diagramm dargestellt.

![Diagramm, das die Bild Streckung des Substreams anzeigt.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

Das vorangehende Diagramm zeigt die folgenden Rechtecke:

-   Ziel Rechteck: {0, 0, 854, 480}
-   Primäres Video:

    -   Quell Rechteck: {0, 0, 720, 480}
    -   Ziel Rechteck: {0, 107, 474, 480}

-   Unter Datenstrom
    -   Quell Rechteck: {0, 0, 720, 480}
    -   Ziel Rechteck: {0, 0, 854, 480}

Diese Werte behalten die Bildhöhe bei und Skalieren beide Bilder horizontal. In den Regionen, in denen beide Bilder angezeigt werden, sind Sie Alpha gemischt. Wenn das substreambild über das primay-Video hinausgeht, wird der unter Datenstrom mit der Hintergrundfarbe mit Alpha gemischt. Mit diesem Alpha werden die Konten für die geänderten Farben auf der rechten Seite des Diagramms gemischt.

### <a name="example-3-mismatched-stream-heights"></a>Beispiel 3: nicht übereinstimmende streamhöhen

Im vorherigen Beispiel weisen der unter Datenstrom und der primäre Stream dieselbe Höhe auf. Streams können auch eine nicht übereinstimmende Höhe aufweisen, wie in diesem Beispiel gezeigt. Bereiche innerhalb des Ziel Rechtecks, in denen kein Video angezeigt wird, werden mit der Hintergrundfarbe gezeichnet – schwarz in diesem Beispiel. Die Quell-und Ziel Rechtecke werden im folgenden Diagramm dargestellt.

![Diagramm mit nicht übereinstimmenden streamhöhen,](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

Das vorangehende Diagramm zeigt die folgenden Rechtecke:

-   Ziel Rechteck: {0, 0, 150, 85}
-   Primäres Video:
    -   Quell Rechteck: {0, 0, 150, 50}
    -   Ziel Rechteck: {0,0, 150, 67}
-   Unter Datenstrom
    -   Quell Rechteck: {0, 0, 100, 85}
    -   Ziel Rechteck: {25, 0, 125, 85}

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a>Beispiel 4: Ziel Rechteck kleiner als Ziel Oberfläche

Dieses Beispiel zeigt einen Fall, bei dem das Ziel Rechteck kleiner als die Ziel Oberfläche ist.

![Diagramm, das einen Blit zu einem Ziel Rechteck anzeigt.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

Das vorangehende Diagramm zeigt die folgenden Rechtecke:

-   Ziel Oberfläche: {0, 0, 300, 200}
-   Ziel Rechteck: {0, 0, 150, 85}
-   Primäres Video:
    -   Quell Rechteck: {0, 0, 150, 50}
    -   Ziel Rechteck: {0,0, 150, 67}
-   Unter Datenstrom
    -   Quell Rechteck: {0, 0, 100, 85}
    -   Ziel Rechteck: {25, 0, 125, 85}

Pixel außerhalb des Ziel Rechtecks werden nicht geändert, sodass die Hintergrundfarbe nur innerhalb des Ziel Rechtecks angezeigt wird. Der gepunktete Bereich gibt Teile der Ziel Oberfläche an, die vom Blit nicht betroffen sind.

### <a name="example-5-source-rectangles"></a>Beispiel 5: Quell Rechtecke

Wenn Sie ein Quell Rechteck angeben, das kleiner als das Quellbild ist, wird der Treiber nur diesen Teil des Bilds blitten. In diesem Beispiel geben die Quell Rechtecke den unteren rechten Quadranten des primären Videodaten Stroms und den unteren linken Quadranten des Substreams an (angegeben durch Hash Zeichen im Diagramm). Die Ziel Rechtecke sind identisch mit den Quell Rechtecke, sodass das Video nicht gestreckt wird. Die Quell-und Ziel Rechtecke werden im folgenden Diagramm dargestellt.

![Diagramm, das einen Blit aus zwei Quell Rechtecke anzeigt.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

Das vorangehende Diagramm zeigt die folgenden Rechtecke:

-   Ziel Rechteck: {0, 0, 720, 576}
-   Primäres Video:
    -   Quell Oberflächen Größe: {0, 0, 720, 480}
    -   Quell Rechteck: {360, 240, 720, 480}
    -   Ziel Rechteck: {0, 0, 360, 240}
-   Unter Datenstrom
    -   Quell Oberflächen Größe: {0, 0, 640, 576}
    -   Quell Rechteck: {0, 288, 320, 576}
    -   Ziel Rechteck: {400, 0, 720, 288}

### <a name="example-6-intersecting-destination-rectangles"></a>Beispiel 6: überschneidende Ziel Rechtecke

Dieses Beispiel ähnelt dem vorherigen, aber die Ziel Rechtecke überschneiden sich. Die Oberflächen Dimensionen sind identisch mit denen im vorherigen Beispiel, die Quell-und Ziel Rechtecke hingegen nicht. Auch hier wird das Video beschnitten, aber nicht gestreckt. Die Quell-und Ziel Rechtecke werden im folgenden Diagramm dargestellt.

![Diagramm, das sich überschneidende Ziel Rechtecke zeigt.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

Das vorangehende Diagramm zeigt die folgenden Rechtecke:

-   Ziel Rechteck: {0, 0, 720, 576}
-   Primäres Video:
    -   Quell Oberflächen Größe: {0, 0, 720, 480}
    -   Quell Rechteck: {260, 92, 720, 480}
    -   Ziel Rechteck: {0, 0, 460, 388}
-   Unter Datenstrom
    -   Quell Oberflächen Größe: {0, 0, 640, 576}
    -   Quell Rechteck: {0, 0, 460, 388}
    -   Ziel Rechteck: {260, 188, 720, 576}

### <a name="example-7-stretching-and-cropping-video"></a>Beispiel 7: Stretching und Zuschneiden von Videos

In diesem Beispiel wird das Video gestreckt und abgeschnitten. Eine 180 × 120-Region aus jedem Stream wird gestreckt, um einen 360 × 240-Bereich im Ziel Rechteck abzudecken.

![Diagramm, das Stretching und Zuschneiden anzeigt.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

Das vorangehende Diagramm zeigt die folgenden Rechtecke:

-   Ziel Rechteck: {0, 0, 720, 480}
-   Primäres Video:
    -   Quell Oberflächen Größe: {0, 0, 360, 240}
    -   Quell Rechteck: {180, 120, 360, 240}
    -   Ziel Rechteck: {0, 0, 360, 240}
-   Unter Datenstrom
    -   Quell Oberflächen Größe: {0, 0, 360, 240}
    -   Quell Rechteck: {0, 0, 180, 120}
    -   Ziel Rechteck: {360, 240, 720, 480}

## <a name="input-sample-order"></a>Eingabe Beispiel Reihenfolge

Der *psamples* -Parameter der [**videoprocess BLT**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) -Methode ist ein Zeiger auf ein Array von Eingabe Beispielen. Beispiele aus dem primären Videostream werden zuerst angezeigt, gefolgt von unter Datenstrom-Bildern in Z-Reihenfolge. Beispiele müssen in der folgenden Reihenfolge in das Array eingefügt werden:

-   Die Beispiele für den primären Videostream werden zuerst in der zeitlichen Reihenfolge im Array angezeigt. Abhängig vom Deinterlacing-Modus benötigt der Treiber möglicherweise ein oder mehrere Verweis Beispiele aus dem primären Videostream. Die Member **numforwardrefsamples** und **numbackwardrefsamples** der [**DXVA2 \_ videoprocess orcaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) -Struktur geben an, wie viele vorwärts-und rückwärts Verweis Beispiele benötigt werden. Der Aufrufer muss diese Verweis Beispiele auch dann bereitstellen, wenn der Videoinhalt progressiv ist und Deinterlacing nicht erfordert. (Dies kann vorkommen, wenn progressive Frames an ein Deinterlacing-Gerät übergeben werden, z. b. wenn die Quelle eine Mischung aus Zeilen Sprung-und progressivem Rahmen enthält.)
-   Nach den Beispielen für den primären Videostream kann das Array bis zu 15 substreambeispiele enthalten, die in der Z-Reihenfolge von unten nach oben angeordnet sind. Unter Ströme sind immer progressiv und erfordern keine Referenzbilder.

Der primäre Videostream kann jederzeit zwischen Zeilen Sprung-und progressivem Inhalt wechseln, und die Anzahl der untergeordneten Datenströme kann sich ändern.

Der **Sampleformat. Sampleformat** -Member der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur gibt den Bildtyp an. Legen Sie für substreambilder diesen Wert auf DXVA2 \_ samplesubstream fest. Für Progressive Bilder lautet der Wert DXVA2 \_ sampleprogressiveframe. Für Zeilen Sprung Bilder hängt der Wert vom Feld Layout ab.

Wenn der Treiber Forward-und rückwärts Verweis Beispiele erfordert, ist die vollständige Anzahl von Samplings möglicherweise zu Beginn der Videosequenz nicht verfügbar. Fügen Sie in diesem Fall Einträge für Sie in das *psamples* -Array ein, aber markieren Sie die fehlenden Beispiele als Typ DXVA2 \_ sampleunknown.

Das **Start** -und das **Endelement** der [**DXVA2 \_ Videosample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) -Struktur gibt den temporalen Speicherort jeder Stichprobe an. Diese Werte werden nur für Beispiele aus dem primären Videostream verwendet. Legen Sie für substreambilder beide Elemente auf 0 (null) fest.

Die folgenden Beispiele helfen Ihnen möglicherweise dabei, diese Anforderungen zu verdeutlichen.

### <a name="example-1"></a>Beispiel 1

Der einfachste Fall tritt auf, wenn keine untergeordneten Datenströme vorhanden sind und der Deinterlacing-Algorithmus keine Verweis Beispiele erfordert (**numforwardrefsamples** und **numbackwardrefsamples** sind gleich null). Bob Deinterlacing ist ein Beispiel für einen solchen Algorithmus. In diesem Fall sollte das *psamples* -Array eine einzelne Eingabe Oberfläche enthalten, wie in der folgenden Tabelle dargestellt.



| Index           | Surface-Typ        | Temporaler Speicherort |
|-----------------|---------------------|-------------------|
| *psamples* \[ 1,0\] | Zeilen Sprung Bild. | *T*               |



 

Der Zeitwert *T* wird als Startzeit des aktuellen Video Rahmens angenommen.

### <a name="example-2"></a>Beispiel 2

In diesem Beispiel werden von der Anwendung zwei untergeordnete Datenströme mit dem primären Stream gemischt. Der Deinterlacing-Algorithmus benötigt keine Verweis Beispiele. In der folgenden Tabelle wird gezeigt, wie diese Beispiele im *psamples* -Array angeordnet werden.



| Index           | Surface-Typ       | Temporaler Speicherort | Z-Reihenfolge |
|-----------------|--------------------|-------------------|---------|
| *psamples* \[ 1,0\] | Zeilen Sprung Bild | *T*               | 0       |
| *psamples* \[ 1\] | Unter Datenstrom          | 0                 | 1       |
| *psamples* \[ 2,2\] | Unter Datenstrom          | 0                 | 2       |



 

### <a name="example-3"></a>Beispiel 3

Nehmen Sie nun an, dass für den Deinterlacing-Algorithmus ein abwärts Verweis Beispiel und ein vorwärts Verweis Beispiel erforderlich sind. Außerdem werden zwei substreambilder bereitgestellt, die insgesamt fünf Oberflächen enthalten. Die richtige Reihenfolge wird in der folgenden Tabelle gezeigt.



| Index           | Surface-Typ                   | Temporaler Speicherort | Z-Reihenfolge        |
|-----------------|--------------------------------|-------------------|----------------|
| *psamples* \[ 1,0\] | Zeilen Sprung Bild (Referenz) | *T* -1            | Nicht verfügbar |
| *psamples* \[ 1\] | Zeilen Sprung Bild             | *T*               | 0              |
| *psamples* \[ 2,2\] | Zeilen Sprung Bild (Referenz) | *T* + 1            | Nicht verfügbar |
| *psamples* \[ €\] | Unter Datenstrom                      | 0                 | 1              |
| *psamples* \[ 0:\] | Unter Datenstrom                      | 0                 | 2              |



 

Die Zeit *t* − 1 ist die Startzeit des Frames vor dem aktuellen Frame, und *T* + 1 ist die Startzeit des folgenden Frames.

Wenn der Videostream in den progressiven Inhalt wechselt, muss die Anwendung dieselbe Anzahl von Stichproben bereitstellen, wie in der folgenden Tabelle gezeigt.



| Index           | Surface-Typ                    | Temporaler Speicherort | Z-Reihenfolge        |
|-----------------|---------------------------------|-------------------|----------------|
| *psamples* \[ 1,0\] | Progressives Bild (Referenz) | *T* -1            | Nicht verfügbar |
| *psamples* \[ 1\] | Progressives Bild             | *T*               | 0              |
| *psamples* \[ 2,2\] | Progressives Bild (Referenz) | *T* + 1            | Nicht verfügbar |
| *psamples* \[ €\] | Unter Datenstrom                       | 0                 | 1              |
| *psamples* \[ 0:\] | Unter Datenstrom                       | 0                 | 2              |



 

### <a name="example-4"></a>Beispiel 4

Zu Beginn einer Videosequenz sind möglicherweise vorwärts-und rückwärts Verweis Beispiele nicht verfügbar. In diesem Fall sind Einträge für die fehlenden Stichproben im *psamples* -Array mit dem Beispieltyp DXVA2 \_ sampleunknown enthalten.

Vorausgesetzt, dass der Deinterlacing-Modus ein vorwärts-und ein abwärts Verweis Beispiel benötigt, verfügen die ersten drei Aufrufe an [**videoprocesblt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) über die Sequenzen von Eingaben, die in den folgenden drei Tabellen angezeigt werden.



| Index           | Surface-Typ                   | Temporaler Speicherort |
|-----------------|--------------------------------|-------------------|
| *psamples* \[ 1,0\] | Unbekannt                        | 0                 |
| *psamples* \[ 1\] | Unbekannt                        | 0                 |
| *psamples* \[ 2,2\] | Zeilen Sprung Bild (Referenz) | *T* + 1            |



 



| Index           | Surface-Typ                   | Temporaler Speicherort |
|-----------------|--------------------------------|-------------------|
| *psamples* \[ 1,0\] | Unbekannt                        | 0                 |
| *psamples* \[ 1\] | Zeilen Sprung Bild             | *T*               |
| *psamples* \[ 2,2\] | Zeilen Sprung Bild (Referenz) | *T* + 1            |



 



| Index           | Surface-Typ                   | Temporaler Speicherort |
|-----------------|--------------------------------|-------------------|
| *psamples* \[ 1,0\] | Zeilen Sprung Bild             | *T* -1            |
| *psamples* \[ 1\] | Zeilen Sprung Bild             | *T*               |
| *psamples* \[ 2,2\] | Zeilen Sprung Bild (Referenz) | *T* + 1            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA2 \_ videoproc-Beispiel](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
