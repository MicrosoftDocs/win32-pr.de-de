---
title: Behandeln von Fehlern mit MIDI-Funktionen
description: Behandeln von Fehlern mit MIDI-Funktionen
ms.assetid: 7ea5db5e-34d7-4506-8157-c24adf5bcdda
keywords:
- Digital Instrumentation Digital Interface (MIDI), Fehler
- MIDI (Digital Interface Digital Interface), Fehler
- MIDI-Dienste, Fehler
- MIDI-Fehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9689fe30b9c4f598cfc9bea892ff3d4fe15d3a9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340270"
---
# <a name="handling-errors-with-midi-functions"></a>Behandeln von Fehlern mit MIDI-Funktionen

Die Funktionen von MIDI-Audiofunktionen geben einen Fehlercode ungleich NULL zurück. Bei Fehlern, die mit einem Fehler in einem Zusammenhang mit einem Fehler in einem Fehlercode auftreten, rufen die Funktionen [**midiingeterrortext**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext) und [**midioutgeterrortext**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext) die Textbeschreibungen Die Anwendung muss weiterhin den Fehlerwert selbst überprüfen, um zu bestimmen, wie der Vorgang fortgesetzt werden kann. Sie kann jedoch die Fehlerbeschreibungen in Dialogfeldern verwenden, um Benutzer über die Fehlerbedingungen zu informieren.

Die einzigen MIDI-Funktionen, die keine Fehlercodes zurückgeben, sind die Funktionen [**midiingetnumdevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs) und [**midioutgetnumdevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) . Diese Funktionen geben den Wert 0 (null) zurück, wenn keine Geräte in einem System vorhanden sind oder wenn von der Funktion Fehler auftreten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MIDI-Dienste](midi-services.md)
</dt> </dl>

 

 