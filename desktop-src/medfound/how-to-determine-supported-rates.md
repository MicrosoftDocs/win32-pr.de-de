---
description: Bestimmen der unterstützten Tarife
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Bestimmen der unterstützten Tarife
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214964"
---
# <a name="how-to-determine-supported-rates"></a>Bestimmen der unterstützten Tarife

Vor dem Ändern der Wiedergabe Rate sollte eine Anwendung überprüfen, ob die Wiedergabe Rate von den Objekten in der Pipeline unterstützt wird. Die [**imfresupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) -Schnittstelle stellt Methoden zum erzielen der maximalen Forward-und Reverse-Raten, die unterstützte Rate, die der angeforderten Rate am nächsten liegt, und die langsamste Rate bereit. Jede dieser Raten Abfragen kann die Wiedergabe Richtung angeben und angeben, ob die Verdünnung verwendet werden soll. Die genaue Wiedergabe Rate wird mithilfe der [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstelle abgefragt.

Weitere Informationen zum Ändern der Wiedergabe Raten finden [Sie unter Festlegen der Wiedergabe Rate für die Medien Sitzung](how-to-set-the-playback-rate-on-the-media-session.md).

Allgemeine Informationen zu den Wiedergabe Raten finden Sie unter [Informationen zur Raten Kontrolle](about-rate-control.md).

## <a name="to-determine-the-current-playback-rate"></a>So bestimmen Sie die aktuelle Wiedergabe Rate

1.  Holen Sie sich den Raten Steuerungs Dienst aus der Medien Sitzung.

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    Übergeben Sie einen initialisierten [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstellen Zeiger im *punkObject* -Parameter von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

    Die Anwendung muss den Raten Steuerungs Dienst über die Medien Sitzung Abfragen. Intern fragt die Medien Sitzung die Objekte in der Topologie ab.

2.  Ruft die [**imfratecontrol:: getrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) -Methode auf, um die aktuelle Wiedergabe Rate zu erhalten.

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    Der *pfthin* -Parameter von [**getrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) empfängt einen **booleschen** Wert, der angibt, ob der Stream gerade schlank ist. Die Anwendung muss **null** übergeben, wenn Sie keine Unterstützung für die Unterstützung des Datenstroms Abfragen möchte. Der *pflrate* -Parameter empfängt die aktuelle Wiedergabe Rate.

## <a name="to-determine-the-nearest-supported-rate"></a>So bestimmen Sie die nächstgelegene unterstützte Rate

1.  Holen Sie sich den Dienst zur Gebühren Unterstützung aus der Medien Sitzung.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Übergeben Sie einen initialisierten [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstellen Zeiger im *punkObject* -Parameter von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Rufen Sie die [**imfratesupport:: isratesupportiert**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) -Methode auf, um die unterstützte Rate abzurufen, die der angeforderten Wiedergabe Rate am nächsten liegt.

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    Im Beispiel wird abgefragt, ob eine Wiedergabe Rate von 4,0 bei der Verdünnung unterstützt wird. Dies wird durch Übergeben von " **true** " im Parameter " *f* " von [**isratesupportiert**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported)angegeben. Wenn diese Rate unterstützt wird, enthält *actualrate* die Wiedergabe Rate 4,0, und der-Befehl wird mit dem Rückgabewert S \_ OK erfolgreich ausgeführt. Wenn die genaue Wiedergabe Rate nicht unterstützt wird, wird die nächste unterstützte Rate in *actualrate* empfangen. Wenn die Rate nicht unterstützt wird und keine verfügbare nächste Wiedergabe Rate verfügbar ist, gibt der-Rückruf einen entsprechenden Fehlercode zurück.

    Diese Werte können sich abhängig davon ändern, welche Pipeline Komponenten geladen werden. Daher sollten Sie die Werte erneut Abfragen, wenn Sie eine neue topolgy laden.

    Wenn die gewünschte Wiedergabe Rate nicht unterstützt wird, besteht eine Möglichkeit darin, jedes Objekt in der Topologie einzeln abzufragen, um herauszufinden, ob eine bestimmte Komponente die Rate nicht unterstützt. Möglicherweise sind Sie in der Lage, die Topologie ohne diese Komponente neu zu erstellen und dann die gewünschte Rate zu spielen. Wenn z. b. jede Komponente außer dem audiorenderer eine bestimmte Rate unterstützt, können Sie die Topologie ohne den audiobranch neu erstellen und ohne Audiodaten mit der gewünschten Geschwindigkeit wiedergeben.

## <a name="to-determine-the-slowest-supported-rate"></a>So bestimmen Sie die langsamste unterstützte Rate

1.  Holen Sie sich den Dienst zur Gebühren Unterstützung aus der Medien Sitzung.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Übergeben Sie einen initialisierten [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstellen Zeiger im *punkObject* -Parameter von [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Rufen Sie die [**imfratesupport:: gezlowestrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) -Methode auf, um die langsamste unterstützte Rate abzurufen.

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    Im Beispiel wird die langsamste umgekehrte Wiedergabe Rate bei der Verdünnung abgefragt. Die untere Grenze wird im *slowestrate* -Parameter von [**gesorlowestrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)empfangen.

    Wenn die umgekehrte Wiedergabe oder die Verdünnung nicht unterstützt wird, gibt der-Rückruf einen entsprechenden Fehlercode zurück.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Sitzung](media-session.md)
</dt> <dt>

[Raten Steuerung](rate-control.md)
</dt> <dt>

[Suchen, schnelles vorwärts und umgekehrtes spielen](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



