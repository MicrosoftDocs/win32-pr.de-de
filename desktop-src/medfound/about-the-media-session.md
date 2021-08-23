---
description: Informationen zur Mediensitzung
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: Informationen zur Mediensitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68816f4c9b9468de2e687a7d00087c5232cc5d24509c9166c5f04c7c0370f6f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035638"
---
# <a name="about-the-media-session"></a>Informationen zur Mediensitzung

Die Mediensitzung macht die [**INTERFACESMediaSession-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) verfügbar. Es gibt zwei Möglichkeiten, die Mediensitzung zu erstellen, je nachdem, ob Ihre Anwendung geschützte Inhalte unterstützt:

-   Wenn Ihre Anwendung keine geschützten Inhalte unterstützt, können Sie die Mediensitzung erstellen, indem Sie [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)aufrufen. Diese Funktion erstellt die Mediensitzung innerhalb des Anwendungsprozesses.
-   Um geschützte Inhalte zu unterstützen, erstellen Sie die Mediensitzung, indem [**Sie MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)aufrufen. Diese Funktion erstellt die Mediensitzung innerhalb des PMP-Prozesses (Protected Media Path). Die Anwendung empfängt einen Zeiger auf ein Proxyobjekt, das Methodenaufrufe über die Prozessgrenze marshallt. Beachten Sie, dass die PMP-Mediensitzung verwendet werden kann, um sowohl klare Inhalte als auch geschützte Inhalte wiederzuspielen.

Jede Anwendung, die die Mediensitzung verwendet, führt die folgenden allgemeinen Schritte aus:

1.  Erstellen Sie eine Topologie.
2.  Stellen Sie die Topologie in der Mediensitzung in die Warteschlange, indem Sie [**DEN AUFRUF VONMEDIASESSION::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)aufrufen.
3.  Steuern Sie den Datenfluss, indem [**Sie ÜBERMEDIASESSION::Start,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) [**ÜBERMEDIASESSION::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)oder [**ÜBERMEDIASESSION::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop)aufrufen.
4.  Rufen Sie VOR dem Beenden der Anwendung [**DIE DATEI "WFMediaSession::Close"**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) auf, um die Mediensitzung zu schließen.
5.  Fahren Sie alle Medienquellen herunter, die von der Anwendung erstellt wurden, indem Sie [**DEN AUFRUF VONMEDIASOURCE::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)aufrufen.
6.  Fahren Sie die Mediensitzung herunter, indem Sie [**DEN AUFRUF VONMEDIASESSION::Shutdown aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)

Bei Verwendung der Mediensitzung sollte die Anwendung die Medienquelle nicht direkt starten, anhalten oder beenden. Alle Zustandsänderungen müssen durch aufrufende [**METHODEN VONMEDIASESSION**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) initiiert werden. Zustandsänderungen in der Medienquelle werden von der Mediensitzung behandelt.

Viele weitere Details hängen von der spezifischen Funktionalität Ihrer Anwendung ab.

## <a name="protected-content"></a>Geschützter Inhalt

Um geschützten Inhalt wiederzugeben, müssen Sie die Mediensitzung innerhalb des Pfads für geschützte Medien (PMP) erstellen, indem Sie [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)aufrufen. Diese Funktion erstellt eine Instanz der Mediensitzung innerhalb des PMP und gibt einen Zeiger auf ein Proxyobjekt zurück, das Schnittstellen über die Prozessgrenze marshallt.

In den meisten Punkten ist die Verwendung der Mediensitzung innerhalb des PMP für die Anwendung transparent. Möglicherweise muss die Anwendung jedoch bestimmte Aktionen aufrufen, die es dem Benutzer ermöglichen, den Inhalt wiederzuspielen. Beispielsweise muss der Benutzer möglicherweise eine DRM-Lizenz erwerben. Media Foundation definiert einen generischen Mechanismus für diese Aktionen mithilfe der [**INTERFACESContentEnabler-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)

Weitere Informationen finden Sie in den folgenden Themen:

-   [Pfad zu geschützten Medien](protected-media-path.md)
-   [Wiedergeben geschützter Mediendateien](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a>Präsentationsuhr

Die Mediensitzung verwaltet alle Aspekte der Präsentationsuhr:

-   Erstellen der Präsentationsuhr.

-   Auswählen der Zeitquelle.

-   Benachrichtigen der Mediensenken über die Uhr

-   Starten, Beenden und Anhalten der Uhr nach Bedarf.

-   Herunterfahren der Uhr.

Rufen Sie ZUM Abrufen eines Zeigers auf die Präsentationsuhr IN DER MEDIENSITZUNG [**DEN AUFRUF VONMEDIASESSION::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) auf. Die Präsentationsuhr gibt keine gültige Zeit zurück, bis die Mediensitzung das [MESessionTopologyStatus-Ereignis](mesessiontopologystatus.md) mit dem \_ MF TOPOSTATUS \_ READY-Flag sendet. Bis dahin gibt **GetClock** MF \_ E CLOCK NO TIME SOURCE \_ \_ \_ \_ zurück.

Eine Anwendung, die die Mediensitzung verwendet, sollte die Präsentationsuhr nie starten, beenden oder anhalten. ändern Sie die Taktrate. oder die Uhr herunterfahren.

Wenn die Anwendung [**DANNMEDIASession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)aufruft, startet die Mediensitzung die Präsentationsuhr mit einer Startzeit, die der in der **Startmethode** angegebenen Startposition entspricht. Weitere Informationen zur Mediensitzung finden Sie unter [Mediensitzung.](media-session.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mediensitzung](media-session.md)
</dt> </dl>

 

 



