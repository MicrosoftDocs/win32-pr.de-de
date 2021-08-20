---
description: Festlegen von DXVA-HD-Zuzuständen
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Festlegen von DXVA-HD-Zuzuständen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 293057c5452eec45b8377b5cddbe8fe959214f5f11f445171ecf22ba752242c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118057816"
---
# <a name="setting-dxva-hd-states"></a>Festlegen von DXVA-HD-Zuzuständen

Während der Videoverarbeitung behält das Gerät DXVA-HD (Microsoft DirectX Video Acceleration High Definition) einen persistenten Zustand von einem Frame zum nächsten bei. Jeder Zustand verfügt über einen dokumentierten Standardwert. Nachdem Sie das Gerät konfiguriert haben, legen Sie alle Zustände fest, die Sie von den Standardwerten ändern möchten. Bevor Sie die einzelnen Frames verarbeiten, aktualisieren Sie alle Zustände, die sich ändern sollten.

> [!Note]  
> Dieser Entwurf unterscheidet sich von DXVA-VP. In DXVA-VP muss die Anwendung alle VP-Parameter mit jedem Frame angeben.

 

Gerätezustände lassen sich in zwei Kategorien unterteilen:

-   *Streamzustände* wenden jeden Eingabestream separat an. Sie können auf jeden Stream unterschiedliche Einstellungen anwenden.
-   *Blit-Zustände* gelten global für den gesamten Blit-Videoverarbeitungs-Blit.

Die folgenden Streamzustände werden definiert.



| Streamzustand                                   | Beschreibung                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **DXVAHD \_ STREAM \_ STATE \_ D3DFORMAT**           | Eingabevideoformat.                                                                                             |
| **DXVAHD \_ STREAM \_ STATE \_ FRAME \_ FORMAT**       | Interlacing.                                                                                                    |
| **DXVAHD \_ STREAM \_ STATE \_ INPUT \_ COLOR \_ SPACE** | Eingabefarbraum. Dieser Zustand gibt den RGB-Farbbereich und die YCbCr-Übertragungsmatrix für den Eingabestream an. |
| **DXVAHD \_ STREAM \_ STATE \_ OUTPUT \_ RATE**        | Ausgabebildrate. Dieser Zustand steuert die Konvertierung der Framerate.                                                   |
| **DXVAHD \_ STREAM \_ STATE \_ SOURCE \_ RECT**        | Quellrechteck.                                                                                               |
| **DXVAHD \_ STREAM \_ STATE \_ DESTINATION \_ RECT**   | Zielrechteck.                                                                                          |
| **DXVAHD \_ STREAM \_ STATE \_ ALPHA**               | Planares Alpha.                                                                                                   |
| **DXVAHD \_ STREAM \_ STATE \_ PALETTE**             | Farbpalette. Dieser Status gilt nur für palettierte Eingabeformate.                                             |
| **DXVAHD \_ STREAM \_ STATE \_ LUMA \_ KEY**           | Luma-Taste.                                                                                                       |
| **DXVAHD \_ STREAM \_ STATE \_ ASPECT \_ RATIO**       | Pixel-Seitenverhältnis.                                                                                             |
| **DXVAHD \_ STREAM \_ STATE \_ FILTER \_ Xxxx**        | Bildfiltereinstellungen. Der Treiber kann Helligkeit, Kontrast und andere Bildfilter unterstützen.                    |



 

Die folgenden Blitzustände sind definiert:



| Blitzustand                                   | Beschreibung                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| **DXVAHD \_ BLT \_ STATE \_ TARGET \_ RECT**         | Zielrechteck.                                                            |
| **DXVAHD \_ BLT \_ STATE \_ BACKGROUND \_ COLOR**    | Hintergrundfarbe.                                                            |
| **DXVAHD \_ BLT \_ STATE \_ OUTPUT \_ COLOR \_ SPACE** | Ausgabefarbraum.                                                          |
| **DXVAHD \_ BLT \_ STATE \_ ALPHA \_ FILL**          | Alphafüllmodus.                                                             |
| **DXVAHD \_ BLT \_ STATE \_ CONSTRICTION**         | Verengung. Dieser Zustand steuert, ob das Gerät die Ausgabe heruntersampelt. |



 

Rufen Sie zum Festlegen eines Streamzustands die [**IDXVAHD \_ VideoProcessor::SetVideoProcessStreamState-Methode**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) auf. Rufen Sie zum Festlegen eines Blitzustands die [**IDXVAHD \_ VideoProcessor::SetVideoProcessBltState-Methode**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) auf. In beiden Methoden gibt ein -Enumerationswert den festgelegten Zustand an. Die Zustandsdaten werden mithilfe einer zustandsspezifischen Datenstruktur angegeben, die von der Anwendung in einen void-Typ **umgeformt \*** wird.

Im folgenden Codebeispiel werden das Eingabeformat und das Zielrechteck für Stream 0 und die Hintergrundfarbe auf Schwarz fest.


```C++
HRESULT SetDXVAHDStates(HWND hwnd, D3DFORMAT inputFormat)
{
    // Set the initial stream states.

    // Set the format of the input stream

    DXVAHD_STREAM_STATE_D3DFORMAT_DATA d3dformat = { inputFormat };

    HRESULT hr = g_pDXVAVP->SetVideoProcessStreamState(
        0,  // Stream index
        DXVAHD_STREAM_STATE_D3DFORMAT,
        sizeof(d3dformat),
        &d3dformat
        );

    if (SUCCEEDED(hr))
    { 
        // For this example, the input stream contains progressive frames.

        DXVAHD_STREAM_STATE_FRAME_FORMAT_DATA frame_format = { DXVAHD_FRAME_FORMAT_PROGRESSIVE };
        
        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index
            DXVAHD_STREAM_STATE_FRAME_FORMAT,
            sizeof(frame_format),
            &frame_format
            );
    }

    if (SUCCEEDED(hr))
    { 
        // Compute the letterbox area.

        RECT rcDest;
        GetClientRect(hwnd, &rcDest);

        RECT rcSrc;
        SetRect(&rcSrc, 0, 0, VIDEO_WIDTH, VIDEO_HEIGHT);

        rcDest = LetterBoxRect(rcSrc, rcDest);

        // Set the destination rectangle, so the frame is displayed within the 
        // letterbox area. Otherwise, the frame is stretched to cover the 
        // entire surface.

        DXVAHD_STREAM_STATE_DESTINATION_RECT_DATA DstRect = { TRUE, rcDest };

        hr = g_pDXVAVP->SetVideoProcessStreamState(
            0, // Stream index 
            DXVAHD_STREAM_STATE_DESTINATION_RECT,
            sizeof(DstRect),
            &DstRect
            );
    }

    if (SUCCEEDED(hr))
    { 
        DXVAHD_COLOR_RGBA rgbBackground = { 0.0f, 0.0f, 0.0f, 1.0f };  // RGBA

        DXVAHD_BLT_STATE_BACKGROUND_COLOR_DATA background = { FALSE, rgbBackground };

        hr = g_pDXVAVP->SetVideoProcessBltState(
            DXVAHD_BLT_STATE_BACKGROUND_COLOR,
            sizeof (background),
            &background
            );
    }

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



