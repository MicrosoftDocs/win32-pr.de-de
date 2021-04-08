---
title: Verwenden eines Ereignis Rückrufs zum Verarbeiten von Treiber Nachrichten
description: Verwenden eines Ereignis Rückrufs zum Verarbeiten von Treiber Nachrichten
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- Wellenform-Audiodatei, Ereignis Rückruf
- Audiodatenblöcke, Ereignis Rückruf
- Wellenform-Audiodatei, Verarbeitung von Treiber Meldungen
- Audiodatenblöcke, Verarbeiten von Treiber Meldungen
- Verarbeiten von Treiber Meldungen
- Funktion "kreateevent"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbfeb95fcf0e5d83f9a54fc0cf3cd223ac6ce19
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725416"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>Verwenden eines Ereignis Rückrufs zum Verarbeiten von Treiber Nachrichten

Um einen Ereignis Rückruf zu verwenden, verwenden [**Sie die Funktion**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) "Funktion", um ein manuelles Zurücksetzungs Ereignis zu erstellen. Geben Sie im Aufrufen der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion das **Rückruf \_ Ereignis** für den *fdwopen* -Parameter an. Nachdem Sie die [**waveoutprepareheader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) -Funktion aufgerufen haben, aber bevor Sie Waveform-Audiodaten an das Gerät gesendet haben, setzen Sie das Ereignis in einen nicht signalisierten Zustand, indem Sie die [**resettevent**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) -Funktion aufrufen. Anschließend wird in einer Schleife, die überprüft, ob das **whdr \_ done** -Flag im **dwFlags** -Member der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur festgelegt ist, die [WaitForSingleObject](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) -Funktion aufgerufen und als Parameter für das Ereignis Handle und einen Timeout Wert angegeben.

Da Ereignis Rückrufe keine bestimmten Close-, done-oder Open-Benachrichtigungen empfangen, muss eine Anwendung möglicherweise den Status des Prozesses überprüfen, auf den Sie wartet, nachdem das Ereignis aufgetreten ist. Es ist möglich, dass eine Reihe von Aufgaben durch die Rückgabe von [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) abgeschlossen wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiodatenblöcke](audio-data-blocks.md)
</dt> </dl>

 

 