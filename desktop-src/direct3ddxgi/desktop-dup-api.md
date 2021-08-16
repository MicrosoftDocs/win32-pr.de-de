---
description: Windows 8 deaktiviert Standardspiegelungstreiber für Windows 2000 Display Driver Model (XDDM) und bietet stattdessen die Desktopduplizierungs-API an.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: Desktopduplizierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c1960d064d7fd1e34748dcc2efb3c86459b498df91b52c1384ef8698a37c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518496"
---
# <a name="desktop-duplication-api"></a>Desktopduplizierungs-API

Windows 8 deaktiviert Standardspiegelungstreiber für Windows 2000 Display Driver Model (XDDM) und bietet stattdessen die Desktopduplizierungs-API an. Die Desktopduplizierungs-API bietet Remotezugriff auf ein Desktopimage für Zusammenarbeitsszenarien. Apps können die Desktopduplizierungs-API verwenden, um auf Frame-by-Frame-Updates für den Desktop zuzugreifen. Da Apps Updates für das Desktopimage auf einer DXGI-Oberfläche erhalten, können die Apps die volle Leistungsfähigkeit der GPU nutzen, um die Imageupdates zu verarbeiten.

-   [Aktualisieren der Desktopimagedaten](#updating-the-desktop-image-data)
-   [Rotieren des Desktopbilds](#rotating-the-desktop-image)
-   [Aktualisieren des Desktopzeigers](#updating-the-desktop-pointer)
-   [Zugehörige Themen](#related-topics)

## <a name="updating-the-desktop-image-data"></a>Aktualisieren der Desktopimagedaten

DXGI stellt über die neue [**IDXGIOutputDuplication::AcquireNextFrame-Methode**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) eine Oberfläche bereit, die ein aktuelles Desktopbild enthält. Das Format des Desktopbilds ist immer [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM,**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) unabhängig vom aktuellen Anzeigemodus. Zusammen mit dieser Oberfläche geben diese [**IDXGIOutputDuplication-Methoden**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) die angegebenen Informationstypen zurück, mit denen Sie bestimmen können, welche Pixel innerhalb der Oberfläche verarbeitet werden müssen:

-   [**IDXGIOutputDuplication::GetFrameDirtyRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) gibt geänderte Bereiche zurück. Dabei handelt es sich um nicht überlappende Rechtecke, die die Bereiche des Desktopimages angeben, die das Betriebssystem seit der Verarbeitung des vorherigen Desktopimages aktualisiert hat.
-   [**IDXGIOutputDuplication::GetFrameMoveRects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) gibt Verschiebungsregionen zurück. Dabei handelt es sich um Rechtecke von Pixeln im Desktopimage, die das Betriebssystem an eine andere Position innerhalb desselben Images verschoben hat. Jeder Verschiebungsbereich besteht aus einem Zielrechteck und einem Quellpunkt. Der Quellpunkt gibt den Speicherort an, von dem aus das Betriebssystem den Bereich kopiert hat, und das Zielrechteck gibt an, wohin das Betriebssystem diesen Bereich verschoben hat. Verschiebungsregionen sind immer nicht gestreckte Bereiche, sodass die Quelle immer die gleiche Größe wie das Ziel hat.

Angenommen, das Desktopimage wurde über eine langsame Verbindung mit Ihrer Remoteclient-App übertragen. Die Datenmenge, die über die Verbindung gesendet wird, wird reduziert, indem nur Daten darüber empfangen werden, wie Ihre Client-App Bereiche von Pixeln anstatt tatsächlichen Pixeldaten verschieben muss. Um die Verschiebungen zu verarbeiten, muss Ihre Client-App das vollständige letzte Image gespeichert haben.

Während das Betriebssystem nicht verarbeitete Desktopimageupdates sammelt, ist möglicherweise nicht mehr viel Speicherplatz verfügbar, um die Updatebereiche genau zu speichern. In dieser Situation beginnt das Betriebssystem, die Updates zu sammeln, indem es sie mit vorhandenen Updateregionen zusammensingt, um alle neuen Updates abzudecken. Daher deckt das Betriebssystem Pixel ab, die in diesem Frame noch nicht aktualisiert wurden. Diese Situation erzeugt jedoch keine visuellen Probleme in Ihrer Client-App, da Sie das gesamte Desktopbild und nicht nur die aktualisierten Pixel erhalten.

Um das richtige Desktopimage zu rekonstruieren, muss Ihre Client-App zuerst alle Verschiebungsregionen und dann alle geänderten Regionen verarbeiten. Eine dieser Listen mit geänderten und verschobenen Regionen kann vollständig leer sein. Der Beispielcode aus dem [Desktopduplizierungsbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) zeigt, wie sowohl die geänderten als auch die Verschiebungsregionen in einem einzelnen Frame verarbeitet werden:


```C++
//
// Get next frame and write it into Data
//
HRESULT DUPLICATIONMANAGER::GetFrame(_Out_ FRAME_DATA* Data)
{
    HRESULT hr = S_OK;

    IDXGIResource* DesktopResource = NULL;
    DXGI_OUTDUPL_FRAME_INFO FrameInfo;

    //Get new frame
    hr = DeskDupl->AcquireNextFrame(500, &FrameInfo, &DesktopResource);
    if (FAILED(hr))
    {
        if ((hr != DXGI_ERROR_ACCESS_LOST) && (hr != DXGI_ERROR_WAIT_TIMEOUT))
        {
            DisplayErr(L"Failed to acquire next frame in DUPLICATIONMANAGER", L"Error", hr);
        }
        return hr;
    }

    // If still holding old frame, destroy it
    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    // QI for IDXGIResource
    hr = DesktopResource->QueryInterface(__uuidof(ID3D11Texture2D), reinterpret_cast<void **>(&AcquiredDesktopImage));
    DesktopResource->Release();
    DesktopResource = NULL;
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to QI for ID3D11Texture2D from acquired IDXGIResource in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    // Get metadata
    if (FrameInfo.TotalMetadataBufferSize)
    {
        // Old buffer too small
        if (FrameInfo.TotalMetadataBufferSize > MetaDataSize)
        {
            if (MetaDataBuffer)
            {
                delete [] MetaDataBuffer;
                MetaDataBuffer = NULL;
            }
            MetaDataBuffer = new (std::nothrow) BYTE[FrameInfo.TotalMetadataBufferSize];
            if (!MetaDataBuffer)
            {
                DisplayErr(L"Failed to allocate memory for metadata in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
                MetaDataSize = 0;
                Data->MoveCount = 0;
                Data->DirtyCount = 0;
                return E_OUTOFMEMORY;
            }
            MetaDataSize = FrameInfo.TotalMetadataBufferSize;
        }

        UINT BufSize = FrameInfo.TotalMetadataBufferSize;

        // Get move rectangles
        hr = DeskDupl->GetFrameMoveRects(BufSize, reinterpret_cast<DXGI_OUTDUPL_MOVE_RECT*>(MetaDataBuffer), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame move rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->MoveCount = BufSize / sizeof(DXGI_OUTDUPL_MOVE_RECT);

        BYTE* DirtyRects = MetaDataBuffer + BufSize;
        BufSize = FrameInfo.TotalMetadataBufferSize - BufSize;

        // Get dirty rectangles
        hr = DeskDupl->GetFrameDirtyRects(BufSize, reinterpret_cast<RECT*>(DirtyRects), &BufSize);
        if (FAILED(hr))
        {
            if (hr != DXGI_ERROR_ACCESS_LOST)
            {
                DisplayErr(L"Failed to get frame dirty rects in DUPLICATIONMANAGER", L"Error", hr);
            }
            Data->MoveCount = 0;
            Data->DirtyCount = 0;
            return hr;
        }
        Data->DirtyCount = BufSize / sizeof(RECT);

        Data->MetaData = MetaDataBuffer;
    }

    Data->Frame = AcquiredDesktopImage;
    Data->FrameInfo = FrameInfo;

    return hr;
}

//
// Release frame
//
HRESULT DUPLICATIONMANAGER::DoneWithFrame()
{
    HRESULT hr = S_OK;

    hr = DeskDupl->ReleaseFrame();
    if (FAILED(hr))
    {
        DisplayErr(L"Failed to release frame in DUPLICATIONMANAGER", L"Error", hr);
        return hr;
    }

    if (AcquiredDesktopImage)
    {
        AcquiredDesktopImage->Release();
        AcquiredDesktopImage = NULL;
    }

    return hr;
}
```



## <a name="rotating-the-desktop-image"></a>Rotieren des Desktopbilds

Sie müssen Ihrer Desktopduplizierungsclient-App expliziten Code hinzufügen, um rotierte Modi zu unterstützen. In einem gedrehten Modus befindet sich die Oberfläche, die Sie von [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) erhalten, immer in der nicht gedrehten Ausrichtung, und das Desktopbild wird innerhalb der Oberfläche gedreht. Wenn der Desktop beispielsweise auf 768 x 1024 bei einer Drehung von 90 Grad festgelegt ist, gibt **AcquireNextFrame** eine 1024 x 768-Oberfläche mit dem darin gedrehten Desktopbild zurück. Hier sind einige Rotationsbeispiele.



| Anzeigemodussatz über die Anzeigesteuerung | Von GDI oder DXGI zurückgegebener Anzeigemodus | Von [ **AcquireNextFrame zurückgegebene** Oberfläche](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| 1024 x 768 Querformat                          | Drehung von 1024 x 768 0 Grad           | 1024x768 \[ newline\] ![Nichtrotierter Remotedesktop](images/dxgi-outdupl-0-rotate.png)<br/>            |
| 1024 x 768 Hochformat                           | Drehung von 768 x 1024 90 Grad          | 1024x768 \[ newline\] ![Gedreht um 90 Grad Remotedesktop](images/dxgi-outdupl-90-rotate.png)<br/>   |
| 1024 x 768 Querformat (gekippt)                | Drehung von 1024 x 768 180 Grad         | 1024x768 \[ newline\] ![Remotedesktop um 180 Grad gedreht](images/dxgi-outdupl-180-rotate.png)<br/> |
| 1024 x 768 Hochformat (gekippt)                 | Drehung von 768 x 1024 270 Grad         | 1024x768 \[ newline\] ![Remotedesktop um 270 Grad gedreht](images/dxgi-outdupl-270-rotate.png)<br/> |



 

Der Code in Ihrer Desktopduplizierungsclient-App muss das Desktopimage entsprechend drehen, bevor Sie das Desktopbild anzeigen.

> [!Note]  
> In Szenarien mit mehreren Monitoren können Sie das Desktopimage für jeden Monitor unabhängig drehen.

 

## <a name="updating-the-desktop-pointer"></a>Aktualisieren des Desktopzeigers

Sie müssen die Desktopduplizierungs-API verwenden, um zu bestimmen, ob Ihre Client-App die Mauszeigerform auf das Desktopbild zeichnen muss. Entweder wird der Mauszeiger bereits auf das Desktopbild gezeichnet, das [**IDXGIOutputDuplication::AcquireNextFrame**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) bereitstellt, oder der Mauszeiger ist vom Desktopbild getrennt. Wenn der Mauszeiger auf das Desktopbild gezeichnet wird, geben die Zeigerpositionsdaten, die von **AcquireNextFrame** gemeldet werden (im **PointerPosition-Element** von [**DXGI \_ OUTDUPL \_ FRAME \_ INFO,**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) auf das der *pFrameInfo-Parameter* zeigt), an, dass kein separater Zeiger sichtbar ist. Wenn der Grafikadapter den Mauszeiger über dem Desktopbild überlagert, meldet **AcquireNextFrame,** dass ein separater Zeiger sichtbar ist. Daher muss Ihre Client-App die Mauszeigerform auf das Desktopbild zeichnen, um genau darzustellen, was dem aktuellen Benutzer auf dem Monitor angezeigt wird.

Um den Mauszeiger des Desktops zu zeichnen, verwenden Sie das **PointerPosition-Element** von [**DXGI \_ OUTDUPL \_ FRAME \_ INFO**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) aus dem *pFrameInfo-Parameter* von [**AcquireNextFrame,**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) um zu bestimmen, wo sich die linke obere Ecke des Mauszeigers auf dem Desktopbild befindet. Wenn Sie den ersten Frame zeichnen, müssen Sie die [**IDXGIOutputDuplication::GetFramePointerShape-Methode**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) verwenden, um Informationen über die Form des Mauszeigers abzurufen. Jeder Aufruf von **AcquireNextFrame** zum Abrufen des nächsten Frames stellt auch die aktuelle Zeigerposition für diesen Frame bereit. Andererseits müssen Sie **GetFramePointerShape** nur dann erneut verwenden, wenn sich die Form ändert. Behalten Sie also eine Kopie des letzten Zeigerbilds bei, und verwenden Sie es, um auf dem Desktop zu zeichnen, es sei denn, die Form des Mauszeigers ändert sich.

> [!Note]  
> Zusammen mit dem Zeigerformbild stellt [**GetFramePointerShape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) die Größe des Hotspots bereit. Der Hot Spot wird nur zu Informationszwecken angegeben. Der Ort, an dem das Zeigerbild gezeichnet werden soll, ist unabhängig vom Hotspot.

 

Dieser Beispielcode aus dem [Desktopduplizierungsbeispiel](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) zeigt, wie Sie die Form des Mauszeigers abrufen:


```C++
//
// Retrieves mouse info and write it into PtrInfo
//
HRESULT DUPLICATIONMANAGER::GetMouse(_Out_ PTR_INFO* PtrInfo, _In_ DXGI_OUTDUPL_FRAME_INFO* FrameInfo, INT OffsetX, INT OffsetY)
{
    HRESULT hr = S_OK;

    // A non-zero mouse update timestamp indicates that there is a mouse position update and optionally a shape change
    if (FrameInfo->LastMouseUpdateTime.QuadPart == 0)
    {
        return hr;
    }

    bool UpdatePosition = true;

    // Make sure we don't update pointer position wrongly
    // If pointer is invisible, make sure we did not get an update from another output that the last time that said pointer
    // was visible, if so, don't set it to invisible or update.
    if (!FrameInfo->PointerPosition.Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber))
    {
        UpdatePosition = false;
    }

    // If two outputs both say they have a visible, only update if new update has newer timestamp
    if (FrameInfo->PointerPosition.Visible && PtrInfo->Visible && (PtrInfo->WhoUpdatedPositionLast != OutputNumber) && (PtrInfo->LastTimeStamp.QuadPart > FrameInfo->LastMouseUpdateTime.QuadPart))
    {
        UpdatePosition = false;
    }

    // Update position
    if (UpdatePosition)
    {
        PtrInfo->Position.x = FrameInfo->PointerPosition.Position.x + OutputDesc.DesktopCoordinates.left - OffsetX;
        PtrInfo->Position.y = FrameInfo->PointerPosition.Position.y + OutputDesc.DesktopCoordinates.top - OffsetY;
        PtrInfo->WhoUpdatedPositionLast = OutputNumber;
        PtrInfo->LastTimeStamp = FrameInfo->LastMouseUpdateTime;
        PtrInfo->Visible = FrameInfo->PointerPosition.Visible != 0;
    }

    // No new shape
    if (FrameInfo->PointerShapeBufferSize == 0)
    {
        return hr;
    }

    // Old buffer too small
    if (FrameInfo->PointerShapeBufferSize > PtrInfo->BufferSize)
    {
        if (PtrInfo->PtrShapeBuffer)
        {
            delete [] PtrInfo->PtrShapeBuffer;
            PtrInfo->PtrShapeBuffer = NULL;
        }
        PtrInfo->PtrShapeBuffer = new (std::nothrow) BYTE[FrameInfo->PointerShapeBufferSize];
        if (!PtrInfo->PtrShapeBuffer)
        {
            DisplayErr(L"Failed to allocate memory for pointer shape in DUPLICATIONMANAGER", L"Error", E_OUTOFMEMORY);
            PtrInfo->BufferSize = 0;
            return E_OUTOFMEMORY;
        }

        // Update buffer size
        PtrInfo->BufferSize = FrameInfo->PointerShapeBufferSize;
    }

    UINT BufferSizeRequired;
    // Get shape
    hr = DeskDupl->GetFramePointerShape(FrameInfo->PointerShapeBufferSize, reinterpret_cast<VOID*>(PtrInfo->PtrShapeBuffer), &BufferSizeRequired, &(PtrInfo->ShapeInfo));
    if (FAILED(hr))
    {
        if (hr != DXGI_ERROR_ACCESS_LOST)
        {
            DisplayErr(L"Failed to get frame pointer shape in DUPLICATIONMANAGER", L"Error", hr);
        }
        delete [] PtrInfo->PtrShapeBuffer;
        PtrInfo->PtrShapeBuffer = NULL;
        PtrInfo->BufferSize = 0;
        return hr;
    }

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXGI 1.2-Verbesserungen](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
