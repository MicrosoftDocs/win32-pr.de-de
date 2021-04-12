---
description: Windows 8 deaktiviert standardmäßige Windows 2000-Anzeigetreiber Modell (XDDM)-Spiegelungs Treiber und bietet stattdessen die desktopduplikats-API.
ms.assetid: 523FBFAD-5D78-4EE3-A3B7-8FD5BA39DC46
title: Desktopduplizierungs-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad27f545318254404beb6372344d8dd0cdfdf604
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481078"
---
# <a name="desktop-duplication-api"></a>Desktopduplizierungs-API

Windows 8 deaktiviert standardmäßige Windows 2000-Anzeigetreiber Modell (XDDM)-Spiegelungs Treiber und bietet stattdessen die desktopduplikats-API. Die Desktop Duplizierungs-API bietet Remote Zugriff auf ein Desktop Image für Zusammenarbeits Szenarien. Apps können die Desktop Duplizierungs-API verwenden, um auf Frame-an-Frame-Aktualisierungen auf dem Desktop zuzugreifen. Da apps Aktualisierungen des Desktop Abbilds auf einer DXGI-Oberfläche erhalten, können die apps die gesamte Leistungsfähigkeit der GPU nutzen, um die Abbild Aktualisierungen zu verarbeiten.

-   [Aktualisieren der Desktop Image Daten](#updating-the-desktop-image-data)
-   [Drehen des Desktop Bilds](#rotating-the-desktop-image)
-   [Aktualisieren des Desktop Zeigers](#updating-the-desktop-pointer)
-   [Zugehörige Themen](#related-topics)

## <a name="updating-the-desktop-image-data"></a>Aktualisieren der Desktop Image Daten

DXGI bietet eine Oberfläche, die ein aktuelles Desktop Bild durch die neue [**idxgioutputdupli:: acquunesextframe**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) -Methode enthält. Das Format des Desktop Bilds lautet immer [**DXGI- \_ Format \_ B8G8R8A8 \_ unorm**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) , unabhängig vom aktuellen Anzeigemodus. Zusammen mit dieser Oberfläche geben diese [**idxgioutputdupliduplizierungsmethoden**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) die angezeigten Arten von Informationen zurück, die Ihnen helfen zu bestimmen, welche Pixel auf der Oberfläche verarbeitet werden müssen:

-   [**Idxgioutputdupli:: getframedirtyrects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects) gibt geänderte Bereiche zurück, bei denen es sich um nicht überlappende Rechtecke handelt, die die Bereiche des Desktop Bilds angeben, die das Betriebssystem seit der Verarbeitung des vorherigen Desktop Abbilds aktualisiert hat.
-   [**Idxgioutputduplizierung:: getframemoverects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects) gibt Verschiebungs Bereiche zurück, bei denen es sich um Rechtecke im Desktop Bild handelt, die das Betriebssystem an einen anderen Speicherort innerhalb desselben Bilds verschoben hat. Jeder Verschiebungs Bereich besteht aus einem Ziel Rechteck und einem Quellpunkt. Der Quellpunkt gibt den Speicherort an, von dem aus das Betriebssystem den Bereich kopiert hat, und das Ziel Rechteck gibt an, wohin das Betriebssystem diese Region verschoben hat. Verschiebungs Bereiche sind immer nicht gestreckte Bereiche, sodass die Quelle immer dieselbe Größe wie das Ziel hat.

Angenommen, das Desktop Image wurde über eine langsame Verbindung mit der Remote Client-App übertragen. Die Menge der Daten, die über die Verbindung gesendet wird, wird verringert, indem nur Daten darüber empfangen werden, wie die Client-App Bereiche von Pixeln und nicht die eigentlichen Pixeldaten verschieben muss. Zum Verarbeiten der Verschiebungen muss Ihre Client-App das gesamte letzte Abbild gespeichert haben.

Wenngleich das Betriebssystem nicht verarbeitete Desktop Abbild Aktualisierungen akkumuliert, kann es nicht mehr genügend Speicherplatz für die genaue Speicherung der Update Regionen gibt. In dieser Situation nimmt das Betriebssystem an, die Updates zu sammeln, indem Sie Sie mit vorhandenen Update Regionen zusammenfügen, um alle neuen Updates abzudecken. Folglich deckt das Betriebssystem Pixel ab, die in diesem Frame noch nicht aktualisiert wurden. Diese Situation erzeugt jedoch keine visuellen Probleme in Ihrer Client-App, da Sie das gesamte Desktop Image und nicht nur die aktualisierten Pixel erhalten.

Um das korrekte Desktop Abbild zu rekonstruieren, muss Ihre Client-App zunächst alle Verschiebungs Regionen verarbeiten und dann alle geänderten Regionen verarbeiten. Diese Listen mit den geänderten und verschiebenden Regionen können vollständig leer sein. Der Beispielcode aus dem Beispiel für eine [Desktop Duplizierung](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) zeigt, wie die Änderungs-und Verschiebungs Bereiche in einem einzelnen Frame verarbeitet werden:


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



## <a name="rotating-the-desktop-image"></a>Drehen des Desktop Bilds

Sie müssen Ihrer Client-App zur Desktop Duplizierung expliziten Code hinzufügen, um gedrehte Modi zu unterstützen In einem gedrehten Modus befindet sich die Oberfläche, die Sie von [**idxgioutputdupli:: acquunenextframe**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) erhalten, immer in der nicht gedrehten Ausrichtung, und das Desktop Bild wird innerhalb der Oberfläche gedreht. Wenn der Desktop z. b. auf 768x1024 bei 90 °-Drehung festgelegt ist, gibt **acquunenextframe** eine 1024 x 768-Oberfläche zurück, wobei das Desktop Bild darin gedreht wird. Hier finden Sie einige Beispiele für die Rotation.



| Anzeigemodus in der Anzeige-Systemsteuerung festgelegt | Von GDI oder DXGI zurückgegebener Anzeigemodus | Von " [ **acquunesextframe** " zurückgegebene Oberfläche](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)                |
|---------------------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------------|
| 1024 x 768-Querformat                          | -Drehung mit 1024 x 768 0 Grad           | 1024 x 768 Zeilen \[ zeiligen Zeilen\] ![nicht gedrehter Remote Desktop](images/dxgi-outdupl-0-rotate.png)<br/>            |
| 1024 x 768-Hochformat                           | 768x 1024 90 Grad Drehung          | 1024 x 768 Zeilen \[ zeiligen Zeilen\] ![90-Grad-Remote Desktop gedreht](images/dxgi-outdupl-90-rotate.png)<br/>   |
| 1024 x 768-Querformat (gekippt)                | 1024 x 768 180 Grad Drehung         | 1024 x 768 Zeilen \[ zeiligen Zeilen\] ![180-Grad-Remote Desktop gedreht](images/dxgi-outdupl-180-rotate.png)<br/> |
| 1024 x 768-Hochformat (gekippt)                 | 768x 1024 270 Grad Drehung         | 1024 x 768 Zeilen \[ zeiligen Zeilen\] ![270-Grad-Remote Desktop gedreht](images/dxgi-outdupl-270-rotate.png)<br/> |



 

Der Code in der Client-App für die Desktop Duplizierung muss das Desktop Image entsprechend drehen, bevor Sie das Desktop Bild anzeigen.

> [!Note]  
> In Szenarios mit mehreren Monitoren können Sie das Desktop Abbild für jeden Monitor unabhängig voneinander drehen.

 

## <a name="updating-the-desktop-pointer"></a>Aktualisieren des Desktop Zeigers

Sie müssen die Desktop Duplizierungs-API verwenden, um zu bestimmen, ob Ihre Client-App die Mauszeiger Form auf das Desktop Bild zeichnen muss. Entweder ist der Mauszeiger bereits auf dem Desktop Bild gezeichnet, das [**idxgioutputdupliziert:: acquirren-extframe**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) bereitstellt, oder der Mauszeiger ist vom Desktop Bild getrennt. Wenn der Mauszeiger auf das Desktop Bild gezeichnet wird, zeigt der Zeiger Positionsdaten an, die von **acquunenextframe** (im **pointerposition** -Member der [**DXGI \_ outdupl- \_ Frame \_ Info**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) , auf die der *pframeinfo* -Parameter verweist) gemeldet wird, um anzuzeigen, dass ein separater Zeiger nicht sichtbar ist. Wenn der Grafikadapter den Mauszeiger oberhalb des Desktop Bilds überlagert, meldet " **acquiriesextframe** ", dass ein separater Zeiger sichtbar ist. Daher muss Ihre Client-App die Mauszeiger Form auf das Desktop Bild zeichnen, um genau darzustellen, was dem aktuellen Benutzer auf dem Monitor angezeigt wird.

Um den Mauszeiger des Desktops zu zeichnen, verwenden Sie den **pointerposition** -Member der [**DXGI \_ outdupl- \_ Frame \_ Info**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_outdupl_frame_info) aus dem *pframeinfo* -Parameter von [**acquunenextframe**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe) , um zu bestimmen, wo die linke obere Ecke des Mauszeigers auf dem Desktop Bild zu finden ist. Wenn Sie den ersten Frame zeichnen, müssen Sie die [**idxgioutputdupli:: getframepointershape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) -Methode verwenden, um Informationen über die Form des Mauszeigers abzurufen. Jeder aufzurufende aufzurufende **Befehl zum Abrufen** des nächsten Frames liefert auch die aktuelle Zeigerposition für diesen Frame. Andererseits müssen Sie **getframepointershape** nur dann erneut verwenden, wenn sich die Form ändert. Behalten Sie also eine Kopie des letzten Zeiger Bilds bei, und verwenden Sie diese zum Zeichnen auf dem Desktop, es sei denn, die Form des Mauszeigers ändert sich.

> [!Note]  
> Zusammen mit dem Zeiger Form Bild gibt [**getframepointershape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape) die Größe der Hotspot Position an. Der Hotspot wird nur zu Informationszwecken angegeben. Der Speicherort, an dem das Zeiger Bild gezeichnet werden soll, ist unabhängig vom Hotspot.

 

Dieser Beispielcode aus dem Beispiel für eine [Desktop Duplizierung](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DXGI%20desktop%20duplication%20sample) zeigt, wie die Form des Mauszeigers angezeigt wird:


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

[DXGI 1,2-Verbesserungen](dxgi-1-2-improvements.md)
</dt> </dl>

 

 
