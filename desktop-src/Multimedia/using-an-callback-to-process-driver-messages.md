---
title: Verwenden eines Ereignisrückrufs zum Verarbeiten von Treibermeldungen
description: Verwenden eines Ereignisrückrufs zum Verarbeiten von Treibermeldungen
ms.assetid: 5b17ff93-ed00-46ee-828c-baf716c9257c
keywords:
- Waveform-Audio, Ereignisrückruf
- Audiodatenblöcke,Ereignisrückruf
- Waveform-Audio, Verarbeiten von Treibermeldungen
- Audiodatenblöcke,Verarbeiten von Treibermeldungen
- Verarbeiten von Treibermeldungen
- CreateEvent-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c5bdbfe46fed9fa9124a031e90af3bfefb983caf6743415d90c645afc42c6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801200"
---
# <a name="using-an-event-callback-to-process-driver-messages"></a>Verwenden eines Ereignisrückrufs zum Verarbeiten von Treibermeldungen

Um einen Ereignisrückruf zu verwenden, verwenden Sie die [**CreateEvent-Funktion,**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) um ein Ereignis für die manuelle Zurücksetzung zu erstellen. Geben Sie im Aufruf der [**waveOutOpen-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) **CALLBACK \_ EVENT** für den *fdwOpen-Parameter* an. Nachdem Sie die [**waveOutPrepareHeader-Funktion**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader) aufgerufen haben, aber bevor Sie Waveform-Audiodaten an das Gerät senden, setzen Sie das Ereignis in einen nicht signalierten Zustand, indem Sie die [**ResetEvent-Funktion**](/windows/desktop/api/synchapi/nf-synchapi-resetevent) aufrufen. Rufen Sie dann in einer Schleife, die überprüft, ob das **Flag WHDR \_ DONE** im **dwFlags-Member** der [**WAVEHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) festgelegt ist, die [WaitForSingleObject-Funktion](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) auf, und geben Sie dabei als Parameter das Ereignishandle und einen Time out-Wert an.

Da Ereignisrückrufe keine spezifischen Benachrichtigungen zum Schließen, Fertig- oder Öffnen empfangen, muss eine Anwendung möglicherweise den Status des Prozesses überprüfen, auf den sie nach dem Auftreten des Ereignisses wartet. Es ist möglich, dass eine Reihe von Aufgaben bis zur Rückgabe von [**WaitForSingleObject abgeschlossen**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) worden wäre.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiodatenblöcke](audio-data-blocks.md)
</dt> </dl>

 

 