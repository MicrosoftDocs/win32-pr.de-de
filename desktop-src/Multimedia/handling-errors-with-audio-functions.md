---
title: Behandeln von Fehlern mit Audiofunktionen
description: Behandeln von Fehlern mit Audiofunktionen
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- Multimedia-Audiodaten, Waveform-Audiofehler
- Audiofehler, Waveform-Audiofehler
- Multimedia-Audiodaten, zusätzliche Audiofehler
- Audiofehler, zusätzliche Audiofehler
- Wellenform-Audiodaten, Fehler
- zusätzliches Audiomaterial, Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314786"
---
# <a name="handling-errors-with-audio-functions"></a>Behandeln von Fehlern mit Audiofunktionen

Die Waveform-Audiofunktionen und hilfsaudiofunktionen geben einen Wert ungleich 0 (null) zurück, wenn ein Fehler auftritt. Windows stellt Funktionen bereit, die diese Fehler Werte in Textbeschreibungen der Fehler konvertieren. Die Anwendung muss die Fehler Werte weiterhin überprüfen, um zu bestimmen, wie der Vorgang fortgesetzt werden kann. Textbeschreibungen von Fehlern können jedoch in Dialogfeldern verwendet werden, in denen Benutzerfehler beschrieben werden.

Mit den folgenden Funktionen können Sie Textbeschreibungen von audiofehlerwerten abrufen:



| Funktion                                           | BESCHREIBUNG                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveingeterrortext**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | Ruft eine Textbeschreibung eines angegebenen Waveform-audioeingabefehlers ab.  |
| [**waveoutgeterrortext**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | Ruft eine Textbeschreibung eines angegebenen Waveform-audioausgabefehlers ab. |



 

Die einzigen Audiofunktionen, die keine Fehler Werte zurückgeben [**, sind "**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)" "" [](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)"" "" "" "" "" "" "" "" "" "" "" "" [**".**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs) Diese Funktionen geben 0 (null) zurück, wenn keine Geräte in einem System vorhanden sind oder wenn Fehler auftreten.

 

 