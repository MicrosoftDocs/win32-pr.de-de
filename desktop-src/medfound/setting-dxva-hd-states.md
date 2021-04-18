---
description: .
ms.assetid: 7f339ee8-01e6-4bbb-8563-020ff0e02499
title: Festlegen von DXVA-HD-Zuständen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e539796aa5d3997b35739e75c80b438a7b5da50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347854"
---
# <a name="setting-dxva-hd-states"></a>Festlegen von DXVA-HD-Zuständen

Während der Videoverarbeitung behält das Microsoft DirectX Video Acceleration High Definition-Gerät (DXVA-HD) einen persistenten Zustand von einem Frame zum nächsten bei. Jeder Status weist einen dokumentierten Standardwert auf. Nachdem Sie das Gerät konfiguriert haben, legen Sie alle Zustände fest, die Sie von den Standardeinstellungen ändern möchten. Aktualisieren Sie vor dem Verarbeiten der einzelnen Frames alle Zustände, die sich ändern sollten.

> [!Note]  
> Dieser Entwurf unterscheidet sich von DXVA-VP. In DXVA-VP muss die Anwendung alle VP-Parameter für jeden Frame angeben.

 

Gerätezustände werden in zwei Kategorien unterteilt:

-   *Streamzustände* wenden jeden Eingabedaten Strom separat an. Sie können für jeden Stream verschiedene Einstellungen anwenden.
-   *Blit* -Zustände gelten global für den gesamten Video Verarbeitungs Blit.

Die folgenden streamzustände sind definiert.



| Streamstatus                                   | BESCHREIBUNG                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **Dxvahd \_ - \_ streamstatus \_ D3DFORMAT**           | Eingabe Videoformat.                                                                                             |
| **dxvahd \_ Stream \_ State- \_ Frame \_ Format**       | Zeilen Sprung.                                                                                                    |
| **dxvahd-Daten \_ Strom- \_ Zustands \_ Eingabe- \_ Farbraum \_** | Eingabefarbraum. Dieser Zustand gibt den RGB-Farbbereich und die YCbCr-Übertragungs Matrix für den Eingabestream an. |
| **dxvahd-Daten \_ Strom- \_ Status- \_ Ausgabe \_ Rate**        | Ausgabe Frame Rate. Dieser Zustand steuert die Konvertierung von Frameraten.                                                   |
| **dxvahd \_ Stream- \_ Zustands \_ Quelle \_ Rect**        | Quell Rechteck.                                                                                               |
| **dxvahd \_ Stream \_ State \_ \_ Rect**   | Ziel Rechteck.                                                                                          |
| **dxvahd \_ Stream \_ State \_ Alpha**               | Planar alpha.                                                                                                   |
| **dxvahd-Daten \_ Strom- \_ Status \_ Palette**             | Farbpalette. Dieser Zustand gilt nur für Paletten-Eingabeformate.                                             |
| **dxvahd- \_ streamstatuszustandsschlüssel \_ \_ \_**           | Luma-Taste.                                                                                                       |
| **dxvahd-Daten \_ Strom- \_ Status \_ Seiten \_ Verhältnis**       | Pixel Seitenverhältnis.                                                                                             |
| **Dxvahd \_ Stream \_ State \_ Filter \_ xxxx**        | Bild Filtereinstellungen. Der Treiber kann Helligkeit, Kontrast und andere Bild Filter unterstützen.                    |



 

Die folgenden Blit-Zustände sind definiert:



| Blit-Status                                   | BESCHREIBUNG                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------|
| **dxvahd \_ blt- \_ Zustands \_ Ziel \_ Rect**         | Ziel Rechteck.                                                            |
| **dxvahd \_ blt- \_ Status \_ Hintergrund \_ Farbe**    | Hintergrundfarbe.                                                            |
| **dxvahd \_ blt- \_ Zustands \_ Ausgabe \_ Farbraum \_** | Ausgabe Farbraum.                                                          |
| **dxvahd \_ blt \_ State \_ alpha \_ Fill**          | Alpha Füllmodus.                                                             |
| **dxvahd \_ blt- \_ Zustands \_ Einschränkung**         | Einschränkungen. Mit diesem Status wird gesteuert, ob die Ausgabe des Geräts herabgestuft wird. |



 

Um einen streamstatus festzulegen, müssen Sie die [**idxvahd \_ videoprocessor:: setvideoprocessstreamstate**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate) -Methode aufrufen. Um einen Blit-Status festzulegen, müssen Sie die [**idxvahd \_ videoprocessor:: setvideoprocessbltstate**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate) -Methode aufrufen. Bei beiden Methoden gibt ein Enumerationswert den festzulegenden Zustand an. Die Zustandsdaten werden mithilfe einer Zustands spezifischen Datenstruktur angegeben, die von der Anwendung in einen **void \*** -Typ umgewandelt wird.

Im folgenden Codebeispiel werden das Eingabeformat und das Ziel Rechteck für Stream 0 festgelegt, und die Hintergrundfarbe wird auf schwarz festgelegt.


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

 

 



