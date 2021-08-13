---
description: Festlegen der Wiedergaberate für die Mediensitzung
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Festlegen der Wiedergaberate für die Mediensitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 696932d0da0147ba87e49cbc22d7ad53a525bc52c9bc2b3518c0f3e956a650aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465990"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a>Festlegen der Wiedergaberate für die Mediensitzung

Um Wiedergabefunktionen wie schnelles Vorwärts- und Zurückspulen zu implementieren, müssen Anwendungen möglicherweise die Wiedergaberate für einen Medienstream ändern. Media Foundation stellt den Ratenkontrolldienst bereit, den die Anwendungen verwenden müssen, um die Wiedergaberate dynamisch festzulegen.

Vor dem Festlegen der Wiedergaberate sollte eine Anwendung überprüfen, ob die Rate von der Medienquelle unterstützt wird. Informationen zum Abfragen unterstützter Raten finden Sie unter [Ermitteln unterstützter Raten.](how-to-determine-supported-rates.md)

Informationen zu Wiedergaberaten finden Sie unter [Informationen zur Ratensteuerung.](about-rate-control.md)

## <a name="to-set-the-playback-rate"></a>So legen Sie die Wiedergaberate fest

1.  Rufen Sie [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) auf, um das Ratensteuerungsobjekt aus der Mediensitzung abzurufen.

    Anwendungen, die [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufrufen, müssen Folgendes sicherstellen:

    -   Der *parameterobject* enthält einen initialisierten [**POINTERMediaSession-Schnittstellenzeiger.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
    -   Das im *ppvObject-Parameter* empfangene Ratenkontrollobjekt wird freigegeben, um Speicherverluste zu vermeiden.

2.  Rufen Sie die [**METHODE ÜBERRATEControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) auf, um die Wiedergaberate festzulegen. Nachdem **SetRate** asynchron abgeschlossen wurde, empfängt die Anwendung das [MESessionRateChanged-Ereignis.](mesessionratechanged.md)

## <a name="example"></a>Beispiel

Der folgende Code zeigt, wie die Wiedergaberate durch Aufrufen der [**SetRate-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) festgelegt wird.


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



Die Anwendung muss beendet oder angehalten werden, bevor sie einen Übergang von einer negativen oder Nullrate zu einer positiven Rate vornehmen kann. Informationen zu diesen Zuständen finden Sie unter [Steuern von Präsentationszuständen.](how-to-control-presentation-states.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mediensitzung](media-session.md)
</dt> <dt>

[Ratensteuerung](rate-control.md)
</dt> <dt>

[Suchen, Vorlauf und ReversePlay](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



