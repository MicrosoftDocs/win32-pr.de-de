---
description: Steuern von Präsentationszuständen
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Steuern von Präsentationszuständen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2148410527ecf966b10e605bbe4d6beb0ac3d515acd6895e4fc03e73564a72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942420"
---
# <a name="how-to-control-presentation-states"></a>Steuern von Präsentationszuständen

Die Mediensitzung bietet Transportsteuerelement, z. B. das Ändern von Präsentationszuständen (Wiedergabe, Pause und Beenden in einem Wiedergabeszenario im Wiedergabestil der Wiedergabeliste). In diesem Thema werden Mediensitzungsmethoden beschrieben, die eine Anwendung aufrufen sollte, um den Wiedergabezustand zu ändern.

Die folgende Tabelle zeigt die gültigen Präsentationszustandsübergänge.



| Zustandsübergang | BESCHREIBUNG                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| Play -> Pause | Die Präsentationsuhr friert ein.                                                            |
| Play -> Stop  | Die Präsentationsuhr wird zurückgesetzt.                                                           |
| Anhalten –> Wiedergeben | Die Präsentationsuhr wird ab dem Zeitpunkt fortgesetzt, zu dem sie während des Übergangs Wiedergabe bis Pause einfriert. |
| Anhalten –> Beenden | Die Präsentationsuhr wird zurückgesetzt.                                                           |
| Beenden von -> Play  | Die Präsentationsuhr beginnt am Anfang der Präsentation.                      |
| Beenden –> Anhalten | Nicht zulässig.                                                                               |



 

## <a name="to-change-presentation-states"></a>So ändern Sie präsentationszustände

-   Rufen Sie die [**METHODE UNTERMEDIASESSION::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) auf, um die Wiedergabe anzuhalten.

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    Vor dem Aufrufen dieser Methode muss die Anwendung die [**METHODE VONMEDIASESSION::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) aufrufen, um zu ermitteln, ob die Medienquelle den Pause-Zustand unterstützt. In diesem Falle gibt diese Methode **MFSESSIONCAP \_ PAUSE** im *pdwCaps-Parameter* zurück.

    Anhalten beendet vorübergehend die Mediensitzung, die Präsentationsuhr und die Streamsenke für die aktuelle Präsentation. Nachdem der Aufruf erfolgreich abgeschlossen wurde, empfängt die Anwendung ein [MESessionPaused-Ereignis.](mesessionpaused.md)

-   Rufen Sie die [**METHODE ÜBERMEDIASESSION::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) auf, um die Wiedergabe zu beenden.

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    Diese Methode beendet die Mediensitzung, indem die Medienquelle, die entsprechenden Uhren und Die Streamsenken beendet werden. Wenn die Mediensitzung die [Sequencerquelle](sequencer-source.md)steuert, werden die zugrunde liegenden nativen Quellen von der Sequencerquelle beendet. Nachdem die Mediensitzung beendet wurde, empfängt die Anwendung ein [MESessionStopped-Ereignis.](mesessionstopped.md)

-   Rufen Sie die [**METHODE SEEKMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) auf, um die Wiedergabe zu starten oder eine neue Position zu suchen.

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    Diese Methode startet die Mediensitzung aus den Zuständen Anhalten und Beenden. Die Mediensitzung ist für die Einrichtung des Datenflusses in der Pipeline verantwortlich. Diese Methode weist die Mediensitzung an, die Präsentationsuhr zu starten. Nach diesem Aufruf sendet Media Session ein [MESessionStarted-Ereignis](mesessionstarted.md) an die Anwendung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mediensitzung](media-session.md)
</dt> </dl>

 

 



