---
title: Behandeln von Fehlern mit Audiofunktionen
description: Behandeln von Fehlern mit Audiofunktionen
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- Multimediaaudio, Waveform-Audiofehler
- Audio, Waveform-Audiofehler
- Multimediaaudio, Zusätzliche Audiofehler
- Audio, Zusätzliche Audiofehler
- Waveformaudio, Fehler
- Hilfsaudio, Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbb332ed0be06a829c169bdf333f3f4ce73a6e9dff81b22949174216dd4017d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141083"
---
# <a name="handling-errors-with-audio-functions"></a>Behandeln von Fehlern mit Audiofunktionen

Die Funktionen waveform-audio und auxiliary-audio geben einen Wert ungleich 0 (null) zurück, wenn ein Fehler auftritt. Windows stellt Funktionen bereit, die diese Fehlerwerte in Textbeschreibungen der Fehler konvertieren. Die Anwendung muss weiterhin die Fehlerwerte untersuchen, um zu bestimmen, wie der Vorgang fortgesetzt werden soll. Textbeschreibungen von Fehlern können jedoch in Dialogfeldern verwendet werden, in denen Fehler für Benutzer beschrieben werden.

Sie können die folgenden Funktionen verwenden, um Textbeschreibungen von Audiofehlerwerten abzurufen:



| Funktion                                           | Beschreibung                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | Ruft eine Textbeschreibung eines angegebenen Waveform-Audio-Eingabefehlers ab.  |
| [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | Ruft eine Textbeschreibung eines angegebenen Waveform-Audio-Ausgabefehlers ab. |



 

Die einzigen Audiofunktionen, die keine Fehlerwerte zurückgeben, sind [**auxGetNumDevs,**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)und [**waveOutGetNumDevs.**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) Diese Funktionen geben 0 (null) zurück, wenn in einem System keine Geräte vorhanden sind oder wenn Fehler auftreten.

 

 