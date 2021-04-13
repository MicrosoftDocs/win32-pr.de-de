---
title: Zurücksetzen der MIDI-Ausgabe
description: Zurücksetzen der MIDI-Ausgabe
ms.assetid: 281a7cfa-f274-4c7a-b63a-c0573b9f1169
keywords:
- Digital Instrumentation Digital Interface (MIDI), Ausgabegeräte zurücksetzen
- MIDI (Digital Instrumentation Digital Interface), Zurücksetzen von Ausgabegeräten
- Abspielen von MIDI-Dateien, Zurücksetzen von Ausgabegeräten
- Zurücksetzen von Ausgabegeräten
- Digital Instrumentation Digital Interface (MIDI), Ausgabegeräte
- MIDI (Digital Instrumentation Digital Interface), Ausgabegeräte
- Abspielen von MIDI-Dateien, Ausgabe von Geräten
- MIDI-Ausgabegeräte
- EOX (Ende der exklusiven)
- Ende der exklusiven (EOX)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15778fc8a1a48c34b69915aafb7e3139153b5882
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314685"
---
# <a name="resetting-midi-output"></a>Zurücksetzen der MIDI-Ausgabe

Die [**midiversiset**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset) -Funktion deaktiviert alle Notizen für alle MIDI-Kanäle für ein bestimmtes MIDI-Gerät. Anschließend werden alle ausstehenden System exklusiven Puffer als abgeschlossen markiert und an die Anwendung zurückgegeben. Diese Funktion kann in einer Anwendung nützlich sein, die die Verwendung von MIDI verwendet, um dem Benutzer die Möglichkeit zu geben, die MIDI-Ausgabe zurückzusetzen.

> [!Note]  
> Das Beenden einer System exklusiven Nachricht, ohne ein EOX-Byte zu senden, kann Probleme für das empfangende Gerät verursachen. Die **midibereichset** -Funktion sendet kein EOX-Byte, wenn Sie eine System exklusive Nachricht beendet, da Anwendungen dafür verantwortlich sind.

 

 

 