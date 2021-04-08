---
title: So implementieren Sie readernachrichten im OnStatus-Rückruf
description: So implementieren Sie readernachrichten im OnStatus-Rückruf
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- Advanced Systems Format (ASF), Implementieren von Reader-Nachrichten
- ASF (Advanced Systems Format), Implementieren von Reader-Nachrichten
- Advanced Systems Format (ASF), OnStatus-Rückruf
- ASF (Advanced Systems Format), OnStatus-Rückruf
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- asynchrone Leser, Implementieren von Reader-Nachrichten
- OnStatus-Rückruf Methode, Implementieren von Reader-Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038544"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a>So implementieren Sie readernachrichten im OnStatus-Rückruf

Um den asynchronen Reader zum Übermitteln von Inhalten aus einer ASF-Datei zu verwenden, müssen Sie mindestens zwei Rückruf Methoden ( [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) und [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample)) implementieren. In diesem Abschnitt wird beschrieben, wie Sie **iwmstatuscallback:: OnStatus** implementieren, um vom Reader gesendete Statusmeldungen zu empfangen und darauf zu reagieren. **OnStatus** wird von anderen Objekten im Windows Media-Format-SDK verwendet. Allgemeine Informationen zu **OnStatus** finden Sie unter [Verwenden des OnStatus-Rückrufs](using-the-onstatus-callback.md).

Wenn Sie den asynchronen Reader verwenden, müssen Sie die folgenden Meldungen in **iwmstatuscallback:: OnStatus** abfangen.



| Statusmeldung | BESCHREIBUNG                                     |
|----------------|-------------------------------------------------|
| WMT \_ geöffnet    | Wird gesendet, wenn Datei öffnende Vorgänge beendet sind. |
| WMT \_ geschlossen    | Wird gesendet, wenn Datei schließende Vorgänge abgeschlossen sind. |



 

Verwenden Sie die oben aufgeführten Statusmeldungen, um die Ausführung der Leseanwendung zu steuern. Beispielsweise müssen Sie warten, bis die **\_ geöffnete WMT** -Nachricht empfangen wird, um den Reader zu starten oder andere Methoden aufzurufen, die erfordern, dass der Reader eine Datei bereit hat. Häufig verwenden Anwendungen, die mit dem asynchronen Reader erstellt wurden, ein Ereignis, um den Abschluss von asynchronen Aufrufen zu signalisieren und die Verarbeitung fortzusetzen. Weitere Informationen zur Verwendung von Ereignissen, um den Abschluss von Vorgängen zu signalisieren, finden Sie unter [Verwenden von Ereignissen mit asynchronen Aufrufen](using-events-with-asynchronous-calls.md).

Viele andere Nachrichten werden vom Reader-Objekt an **OnStatus** gesendet, damit die Anwendung auf den Status von Lesevorgängen reagieren kann. Die möglichen Status Meldungs Werte werden im Enumerationstyp " [**WMT- \_ Status**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) " definiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Verwenden des OnStatus-Rückrufs**](using-the-onstatus-callback.md)
</dt> </dl>

 

 




