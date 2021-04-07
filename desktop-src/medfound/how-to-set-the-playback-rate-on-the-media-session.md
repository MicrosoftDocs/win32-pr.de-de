---
description: Festlegen der Wiedergabe Rate für die Medien Sitzung
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Festlegen der Wiedergabe Rate für die Medien Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761370"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a>Festlegen der Wiedergabe Rate für die Medien Sitzung

Zum Implementieren von Wiedergabe Funktionen wie "schnelles vorwärts" und "Zurückspulen" müssen Anwendungen möglicherweise die Wiedergabe Rate für einen Mediendaten Strom ändern. Media Foundation stellt den Raten Steuerungs Dienst bereit, den die Anwendungen verwenden müssen, um die Wiedergabe Rate dynamisch festzulegen.

Vor dem Festlegen der Wiedergabe Rate sollte eine Anwendung überprüfen, ob die Rate von der Medienquelle unterstützt wird. Weitere Informationen zum Abfragen unterstützter Tarife finden Sie unter [bestimmen der unterstützten Tarife](how-to-determine-supported-rates.md).

Informationen zu den Wiedergabe Raten finden Sie unter Informationen [zur Raten Kontrolle](about-rate-control.md).

## <a name="to-set-the-playback-rate"></a>So legen Sie die Wiedergabe Rate fest

1.  Aufrufen von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) zum Abrufen des Raten Steuerungs Objekts aus der Medien Sitzung.

    Anwendungen, die " [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) " aufrufen, müssen Folgendes sicherstellen:

    -   Der *punkObject* -Parameter enthält einen initialisierten [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstellen Zeiger.
    -   Das in den Parameter *ppvobject* empfangene Raten Steuerungsobjekt wird freigegeben, um Speicher Verluste zu vermeiden.

2.  Ruft die [**imfratecontrol:: setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) -Methode auf, um die Wiedergabe Rate festzulegen. Nachdem **setRate** asynchron abgeschlossen wurde, empfängt die Anwendung das Ereignis [mesessionratechanged](mesessionratechanged.md) .

## <a name="example"></a>Beispiel

Der folgende Code zeigt, wie die Wiedergabe Rate durch Aufrufen der [**setRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) -Methode festgelegt wird.


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



Die Anwendung muss beendet oder angehalten werden, bevor Sie einen Übergang von einer negativen oder NULL-Rate zu einem positiven Satz durchführen kann. Weitere Informationen zu diesen Zuständen finden [Sie unter How to Control Presentation States](how-to-control-presentation-states.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Sitzung](media-session.md)
</dt> <dt>

[Raten Steuerung](rate-control.md)
</dt> <dt>

[Suchen, schnelles vorwärts und umgekehrtes spielen](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



