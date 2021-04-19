---
description: Steuern von Präsentations Zuständen
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Steuern von Präsentations Zuständen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a82fe0363a27b9c6f5c054b73ca409835a3dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350516"
---
# <a name="how-to-control-presentation-states"></a>Steuern von Präsentations Zuständen

Die Medien Sitzung bietet Transport Steuerelemente, z. b. das Ändern von Präsentations Zuständen (wiedergeben, anhalten und stoppen in einem Wiedergabe Szenario mit Wiedergabelisten). In diesem Thema werden die Methoden der Medien Sitzungen beschrieben, die eine Anwendung zum Ändern des Wiedergabe Zustands aufruft.

In der folgenden Tabelle sind die gültigen Präsentations Zustandsübergänge aufgeführt.



| Zustandsübergang | BESCHREIBUNG                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| Wiedergabe > Pause | Die Präsentations Uhr friert.                                                            |
| Wiedergabe > Beendigung  | Die Präsentations Uhr wird zurückgesetzt.                                                           |
| Pause > Wiedergabe | Die Präsentations Uhr wird von der Zeit wieder aufgenommen, die während der Wiedergabe zum Anhalten des Übergangs gewechselt ist. |
| Anhalten-> anhalten | Die Präsentations Uhr wird zurückgesetzt.                                                           |
| Wiedergabe >  | Die Präsentations Uhr beginnt am Anfang der Präsentation.                      |
| Anhalten-> anhalten | Nicht zulässig.                                                                               |



 

## <a name="to-change-presentation-states"></a>So ändern Sie Darstellungs Zustände

-   Wenden Sie die [**imfmediasession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) -Methode an, um die Wiedergabe anzuhalten.

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    Vor dem Aufrufen dieser Methode muss die Anwendung die [**imfmediasession:: gezessionfunktionalitäten**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) -Methode aufrufen, um zu ermitteln, ob die Medienquelle den anhaltezustand unterstützt. Wenn dies der Fall ist, gibt diese Methode " **mfsessioncap \_ Pause** " im *pdwcaps* -Parameter zurück.

    Anhalten beendet vorübergehend die Medien Sitzung, die Präsentations Uhr und die streamsenke für die aktuelle Präsentation. Nachdem der-Vorgang erfolgreich abgeschlossen wurde, empfängt die Anwendung ein [mesessionangeh Ed](mesessionpaused.md) -Ereignis.

-   Wenden Sie die [**imfmediasession:: stopmethode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) an, um die Wiedergabe zu verhindern.

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    Diese Methode beendet die Medien Sitzung durch Beenden der Medienquelle, der entsprechenden Uhren und der streamsenken. Wenn die Medien Sitzung die [Sequencer-Quelle](sequencer-source.md)steuert, werden die zugrunde liegenden systemeigenen Quellen von der Sequencer-Quelle beendet. Nachdem die Medien Sitzung beendet wurde, empfängt die Anwendung ein [mesessionbeendete](mesessionstopped.md) -Ereignis.

-   Wenden Sie die [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) -Methode an, um die Wiedergabe zu starten oder eine neue Position zu suchen.

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    Diese Methode startet die Medien Sitzung über den Status anhalten und anhalten. Die Medien Sitzung ist für das Einrichten des Datenflusses in der Pipeline zuständig. Diese Methode weist die Medien Sitzung an, die Präsentations Uhr zu starten. Nach diesem-Befehl sendet die Medien Sitzung ein [mesessionstarted](mesessionstarted.md) -Ereignis an die Anwendung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Sitzung](media-session.md)
</dt> </dl>

 

 



