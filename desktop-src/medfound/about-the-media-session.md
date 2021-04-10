---
description: Informationen zur Medien Sitzung
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: Informationen zur Medien Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961094"
---
# <a name="about-the-media-session"></a>Informationen zur Medien Sitzung

Die Medien Sitzung macht die [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Schnittstelle verfügbar. Es gibt zwei Möglichkeiten, die Medien Sitzung zu erstellen, je nachdem, ob Ihre Anwendung geschützte Inhalte unterstützt:

-   Wenn Ihre Anwendung geschützte Inhalte nicht unterstützt, können Sie die Medien Sitzung erstellen, indem Sie die [**mfcreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession)aufrufen. Diese Funktion erstellt die Medien Sitzung innerhalb des Anwendungsprozesses.
-   Um geschützte Inhalte zu unterstützen, erstellen Sie die Medien Sitzung, indem Sie [**mfcreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)aufrufen. Diese Funktion erstellt die Medien Sitzung innerhalb des PMP-Prozesses (Protected Media Path). Die Anwendung empfängt einen Zeiger auf ein Proxy Objekt, das Methodenaufrufe über die Prozess Grenze hinweg marshallen. Beachten Sie, dass die PMP-Medien Sitzung verwendet werden kann, um Klartext und geschützte Inhalte wiederzugeben.

Jede Anwendung, die die Medien Sitzung verwendet, führt die folgenden allgemeinen Schritte aus:

1.  Erstellen Sie eine Topologie.
2.  Stellen Sie die Topologie in der Medien Sitzung durch Aufrufen von [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology)in die Warteschlange.
3.  Steuern Sie den Datenfluss durch Aufrufen von [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**imfmediasession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)oder [**imfmediasession:: Beendigung**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).
4.  Bevor die Anwendung beendet wird, wird [**imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) aufgerufen, um die Medien Sitzung zu schließen.
5.  Beenden Sie alle Medienquellen, die von der Anwendung erstellt wurden, durch Aufrufen von [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).
6.  Beenden Sie die Medien Sitzung, indem Sie [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)aufrufen.

Wenn Sie die Medien Sitzung verwenden, sollte die Anwendung die Medienquelle nicht direkt starten, anhalten oder beenden. Alle Zustandsänderungen müssen durch Aufrufen von [**imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) -Methoden initiiert werden. Zustandsänderungen in der Medienquelle werden von der Medien Sitzung behandelt.

Viele weitere Details hängen von der spezifischen Funktionalität Ihrer Anwendung ab.

## <a name="protected-content"></a>Geschützter Inhalt

Um geschützte Inhalte wiederzugeben, müssen Sie die Medien Sitzung im geschützten Medien Pfad (PMP) erstellen, indem Sie [**mfcreatepmpmediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession)aufrufen. Diese Funktion erstellt eine Instanz der Medien Sitzung innerhalb des PMP und gibt einen Zeiger auf ein Proxy Objekt zurück, das Schnittstellen über die Prozess Grenze hinweg marshunkt.

In den meisten Fällen ist die Verwendung der Medien Sitzung innerhalb des PMP für die Anwendung transparent. Allerdings muss die Anwendung möglicherweise bestimmte Aktionen aufrufen, die dem Benutzer die Wiedergabe des Inhalts ermöglichen. Beispielsweise muss der Benutzer möglicherweise eine DRM-Lizenz erwerben. Media Foundation definiert einen generischen Mechanismus für diese Aktionen mithilfe der [**IMF contentenabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) -Schnittstelle.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Geschützter Medien Pfad](protected-media-path.md)
-   [Wiedergeben geschützter Mediendateien](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a>Präsentations Uhr

In der Medien Sitzung werden alle Aspekte der Präsentations Uhr verwaltet:

-   Erstellen der Präsentations Uhr.

-   Die Zeit Quelle wird ausgewählt.

-   Benachrichtigen der Medien senken über die Uhr

-   Starten, beenden und Anhalten der Uhr nach Bedarf.

-   Die Uhr wird heruntergefahren.

Um einen Zeiger auf die Präsentations Uhr zu erhalten, nennen Sie [**imfmediasession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) für die Medien Sitzung. Die Präsentations Uhr gibt keine gültige Zeit zurück, bis die Medien Sitzung das [mesessiontopologystatus](mesessiontopologystatus.md) -Ereignis mit dem MF- \_ Flag "topostatusready" sendet \_ . Bis zu diesem Zeitpunkt gibt **getclock** die "MF \_ E \_ Clock \_ No Time"- \_ Quelle zurück \_ .

Eine Anwendung, die die Medien Sitzung verwendet, sollte die Präsentations Uhr nie starten, beenden oder anhalten. Ändern Sie die Taktrate. oder beenden Sie die Uhr.

Wenn die Anwendung [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)aufruft, startet die Medien Sitzung die Präsentations Uhr mit einer Startzeit, die der Anfangsposition entspricht, die in der **Start** -Methode angegeben ist. Weitere Informationen zur Medien Sitzung finden Sie unter [Medien Sitzung](media-session.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Sitzung](media-session.md)
</dt> </dl>

 

 



