---
description: Vorgehensweise beim Ausführen von Scrubbing
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Vorgehensweise beim Ausführen von Scrubbing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527686"
---
# <a name="how-to-perform-scrubbing"></a>Vorgehensweise beim Ausführen von Scrubbing

Das Scrubbing wird ausgeführt, um sofort bestimmte Punkte in einer Datei zu suchen, indem Sie mit einer visuellen Darstellung der Zeit interagieren, z. b. einer Scrollleiste. In Media Foundation bedeutet Bereinigungs, eine Datei zu suchen und einen aktualisierten Frame zu erhalten.

Informationen zum Bereinigen finden Sie unter Informationen [zur Raten Kontrolle](about-rate-control.md).

## <a name="to-perform-scrubbing"></a>So führen Sie Bereinigungs aus

1.  Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) zum Abrufen der [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstelle aus der [Medien Sitzung](media-session.md).
    > [!Note]  
    > Die [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstelle kann nicht aus der Medienquelle abgerufen werden. Die Schnittstelle immer aus der Medien Sitzung erhalten.

     

2.  Greifen Sie [**imfratecontrol:: setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) an, um die Wiedergabe Rate auf NULL festzulegen. Weitere Informationen zum Aufrufen dieser Methode finden Sie unter [Festlegen der Wiedergabe Rate für die Medien Sitzung](how-to-set-the-playback-rate-on-the-media-session.md).
3.  Erstellen Sie eine Suchposition in einer **PROPVARIANT** , indem Sie die Darstellungs Zeit in einem **mftime** -Typ angeben.
4.  Geben Sie [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) mit der Suchposition an, um die Wiedergabe zu starten.
5.  Wenn der Bereinigungsvorgang beendet ist, sendet die Medien Sitzung ein [mesessionscrubsamplecomplete](mesessionscrubsamplecomplete.md) -Ereignis. Warten Sie auf dieses Ereignis, bevor Sie erneut [**starten**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) , um einen weiteren Bereinigungs Vorgang auszuführen.

## <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird gezeigt, wie ein Scrubbing durchgeführt wird.


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



Bei einem erfolgreichen Bereinigungs Vorgang wird das Ereignis [mesessionscrubsamplecomplete](mesessionscrubsamplecomplete.md) generiert, nachdem alle streamsenken mit dem neuen Frame aktualisiert wurden und der Bereinigungs Vorgang erfolgreich abgeschlossen wurde. Beim Bereinigen einer Videodatei wird der Frame angezeigt, zu dem das Seeding erfolgt ist, aber es wird keine Audioausgabe generiert.

Die Anwendung kann Frame-Stepping durchführen, indem die Wiedergabe Rate auf NULL festgelegt wird und dann eine **PROPVARIANT** , die auf **VT \_ empty** festgelegt ist, im [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)-Befehl übergeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Sitzung](media-session.md)
</dt> <dt>

[Raten Steuerung](rate-control.md)
</dt> </dl>

 

 



