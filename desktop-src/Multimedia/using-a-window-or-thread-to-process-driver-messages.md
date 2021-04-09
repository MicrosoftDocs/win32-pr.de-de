---
title: Verwenden eines Fensters oder Threads zum Verarbeiten von Treiber Nachrichten
description: Verwenden eines Fensters oder Threads zum Verarbeiten von Treiber Nachrichten
ms.assetid: 7a9eaaa1-d3b0-400e-8fbf-ee5fe59efc32
keywords:
- Wellenform-Audiodatei, Fenster Rückruf
- Audiodatenblöcke, Fenster Rückruf
- Wellenform-Audiodatei, Thread Rückruf
- Audiodatenblöcke, Thread Rückruf
- Wellenform-Audiodatei, Verarbeitung von Treiber Meldungen
- Audiodatenblöcke, Verarbeiten von Treiber Meldungen
- Verarbeiten von Treiber Meldungen
- Wavin Open-Funktion
- WaveOutOpen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a147bd86b3c8045456ef9961039f645fd4023f13
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948735"
---
# <a name="using-a-window-or-thread-to-process-driver-messages"></a>Verwenden eines Fensters oder Threads zum Verarbeiten von Treiber Nachrichten

Um eine Fenster Rückruffunktion zu verwenden, geben Sie das Rückruf \_ Fenster-Flag im *fdwopen* -Parameter und ein Fenster Handle im nieder wertigen Wort des *dwcallback* -Parameters der [**waveinopen**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion oder der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion an. Treiber Meldungen werden an die Fenster Prozedur für das Fenster gesendet, das durch das Handle in *dwcallback* identifiziert wird.

Um einen Thread Rückruf zu verwenden, geben Sie auch \_ den Rückruf Thread und ein Thread Handle im Aufrufs von **waveinopen** oder **WaveOutOpen** an. In diesem Fall werden Nachrichten anstelle eines Fensters an den angegebenen Thread gesendet.

Nachrichten, die an den Fenster-oder Thread Rückruf gesendet werden, sind spezifisch für den verwendeten audiogerätetyp. Weitere Informationen zu diesen Meldungen finden Sie unter wieder [Gabe Waveform-Audio Dateien](playing-waveform-audio-files.md).

 

 