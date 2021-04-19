---
title: Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten
description: Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten
ms.assetid: 7fef400f-5040-4d33-9a2f-bb12aa9369e0
keywords:
- Wellenform-Audiodaten, Rückruf Funktionen
- Audiodatenblöcke, Rückruf Funktionen
- Wellenform-Audiodatei, Verarbeitung von Treiber Meldungen
- Audiodatenblöcke, Verarbeiten von Treiber Meldungen
- Verarbeiten von Treiber Meldungen
- Wavin Open-Funktion
- WaveOutOpen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3e7541a00b43b5fb2267a17d4de8bb017823c3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341300"
---
# <a name="using-a-callback-function-to-process-driver-messages"></a>Verwenden einer Rückruffunktion zum Verarbeiten von Treiber Nachrichten

Sie können eine eigene Rückruffunktion schreiben, um Nachrichten zu verarbeiten, die vom Gerätetreiber gesendet werden. Um eine Rückruffunktion zu verwenden, geben Sie das Rückruf \_ funktionsflag im Parameter *fdwopen* und die Adresse des Rückrufs im *dwcallback* -Parameter der [**Wavin Open**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen) -Funktion oder der [**WaveOutOpen**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen) -Funktion an.

An eine Rückruffunktion gesendete Nachrichten ähneln Nachrichten, die an ein Fenster gesendet werden, mit dem Unterschied, dass Sie anstelle eines **uint** -und **DWORD** -Parameters zwei **DWORD** -Parameter aufweisen. Ausführliche Informationen zu diesen Meldungen finden Sie unter wieder [Gabe Waveform-Audio Dateien](playing-waveform-audio-files.md).

Verwenden Sie eine der folgenden Verfahren, um Instanzdaten von einer Anwendung an eine Rückruffunktion zu übergeben:

-   Übergeben Sie die Instanzdaten mit dem *dwinstance* -Parameter der Funktion, die den Gerätetreiber öffnet.
-   Übergeben Sie die Instanzdaten mit dem **DWUser** -Member der [**wavehdr**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) -Struktur, die einen audiodatenblock identifiziert, der an einen Gerätetreiber gesendet wird.

Wenn Sie mehr als 32 Bits von Instanzdaten benötigen, übergeben Sie einen Zeiger auf eine-Struktur, die die zusätzlichen Informationen enthält.

 

 