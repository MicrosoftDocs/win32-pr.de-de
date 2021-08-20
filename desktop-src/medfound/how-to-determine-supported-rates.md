---
description: Ermitteln der unterstützten Raten
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Ermitteln der unterstützten Raten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aadbf0f9a0ce9608b58019d64ddb18a2227bbeb2941540086a6f998e40ebc3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878942"
---
# <a name="how-to-determine-supported-rates"></a>Ermitteln der unterstützten Raten

Vor dem Ändern der Wiedergaberate sollte eine Anwendung überprüfen, ob die Wiedergaberate von den Objekten in der Pipeline unterstützt wird. Die [**BERATERateSupport-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) stellt Methoden bereit, um die maximalen Vorwärts- und Umgekehrt-Raten, die unterstützte Rate, die einer angeforderten Rate am nächsten ist, und die langsamste Rate zu erhalten. Jede dieser Rate-Abfragen kann die Wiedergaberichtung angeben und angeben, ob thinning verwendet werden soll. Die genaue Wiedergaberate wird mithilfe der [**BERRATEControl-Schnittstelle abgefragt.**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)

Informationen zum Ändern der Wiedergaberaten finden Sie unter Festlegen der [Wiedergaberate für die Mediensitzung.](how-to-set-the-playback-rate-on-the-media-session.md)

Allgemeine Informationen zu Wiedergaberaten finden Sie unter [Informationen zur Ratensteuerung.](about-rate-control.md)

## <a name="to-determine-the-current-playback-rate"></a>So bestimmen Sie die aktuelle Wiedergaberate

1.  Sie können den Rate Control-Dienst aus der Mediensitzung erhalten.

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    Übergeben Sie einen initialisierten [**INTERFACEMediaSession-Schnittstellenzeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) im *eigenschaftObject-Parameter* von [**MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)

    Die Anwendung muss den Rate Control-Dienst über die Mediensitzung abfragen. Intern fragt die Mediensitzung die Objekte in der Topologie ab.

2.  Rufen Sie [**die METHODE VERRATEControl::GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) auf, um die aktuelle Wiedergaberate zu erhalten.

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    Der *pfThin-Parameter* von [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) empfängt einen **BOOL-Wert,** der angibt, ob der Stream gerade ausgefälsiert wird. Die Anwendung muss NULL **übergeben,** wenn sie keine Unterstützung für die Verankerung des Streams abfragen möchte. Der *parameter pflRate* empfängt die aktuelle Wiedergaberate.

## <a name="to-determine-the-nearest-supported-rate"></a>So bestimmen Sie die nächste unterstützte Rate

1.  Den Supportdienst für die Rate erhalten Sie über die Mediensitzung.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Übergeben Sie einen initialisierten [**INTERFACEMediaSession-Schnittstellenzeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) im *eigenschaftObject-Parameter* von [**MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)

2.  Rufen Sie [**die METHODE VERRATESupport::IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) auf, um die unterstützte Rate abzurufen, die einer angeforderten Wiedergaberate am nächsten liegt.

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    Im Beispiel wird abgefragt, ob eine Wiedergaberate von 4,0 mit Thinning unterstützt wird. Dies wird durch Übergeben **von TRUE** im *fThin-Parameter* von [**IsRateSupported angegeben.**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) Wenn diese Rate unterstützt wird, *enthält actualRate* die Wiedergaberate von 4,0, und der Aufruf ist mit dem Rückgabewert S \_ OK erfolgreich. Wenn die genaue Wiedergaberate nicht unterstützt wird, wird die nächste unterstützte Rate in *actualRate empfangen.* Wenn die Rate nicht unterstützt wird und keine nächste Wiedergaberate verfügbar ist, gibt der Aufruf einen entsprechenden Fehlercode zurück.

    Diese Werte können sich abhängig davon ändern, welche Pipelinekomponenten geladen werden. Daher sollten Sie die Werte erneut abfragen, wenn Sie eine neue topololgy laden.

    Wenn die gewünschte Wiedergaberate nicht unterstützt wird, besteht eine Möglichkeit in der individuellen Abfrage jedes Objekts in der Topologie, um herauszufinden, ob eine bestimmte Komponente die Rate nicht unterstützt. Möglicherweise können Sie die Topologie ohne diese Komponente neu erstellen und dann mit der gewünschten Rate wieder verwenden. Wenn beispielsweise jede Komponente mit Ausnahme des Audiorenderers eine bestimmte Rate unterstützt, können Sie die Topologie ohne den Audiozweig neu erstellen und mit der gewünschten Rate ohne Audio wieder geben.

## <a name="to-determine-the-slowest-supported-rate"></a>So bestimmen Sie die langsamste unterstützte Rate

1.  Den Supportdienst für die Rate erhalten Sie über die Mediensitzung.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Übergeben Sie einen initialisierten [**INTERFACEMediaSession-Schnittstellenzeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) im *eigenschaftObject-Parameter* von [**MFGetService.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice)

2.  Rufen Sie [**die METHODE MARSHRateSupport::GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) auf, um die langsamste unterstützte Rate abzurufen.

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    Im Beispiel wird die langsamste Umgekehrt-Wiedergaberate mit Verlangsamung abgefragt. Die untere Grenze wird im *slowestRate-Parameter* von [**GetSlowestRate empfangen.**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)

    Wenn die umgekehrte Wiedergabe oder Verankerung nicht unterstützt wird, gibt der Aufruf einen entsprechenden Fehlercode zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mediensitzung](media-session.md)
</dt> <dt>

[Rate Control](rate-control.md)
</dt> <dt>

[Suchen, Vorlauf und Umgekehrtes Wiederkehren](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



