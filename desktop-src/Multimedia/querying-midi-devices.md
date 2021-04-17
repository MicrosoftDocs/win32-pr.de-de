---
title: Abfragen von MIDI-Geräten
description: Abfragen von MIDI-Geräten
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- Digital Instrumentation Digital Interface (MIDI), Abfragen von Geräten
- MIDI (Digital Instrumentation Digital Interface), Abfragen von Geräten
- MIDI-Dienste, Abfragen von Geräten
- Abfragen von MIDI-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066648d6e9ce89e03b26940cb27f3b62b6a03c07
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390183"
---
# <a name="querying-midi-devices"></a>Abfragen von MIDI-Geräten

Vor der Wiedergabe oder Aufzeichnung von MIDI-Daten müssen Sie die Funktionen der im System vorhandenen MIDI-Hardware ermitteln. Die Funktionen von MIDI können von einem Multimedia-Computer bis zum nächsten abweichen. Anwendungen sollten keine Annahmen über die Hardware treffen, die in einem bestimmten System vorhanden ist.

Windows stellt die folgenden Funktionen bereit, um zu bestimmen, wie viele MIDI-Geräte für die Eingabe oder Ausgabe in einem bestimmten System verfügbar sind.



| Wert                                          | Bedeutung                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [**midiingetnumentvs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | Ruft die Anzahl der im System vorhandenen MIDI-Eingabegeräte ab.  |
| [**midioutgetnumentvs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | Ruft die Anzahl der im System vorhandenen Ausgabegeräte im System ab. |



 

Wie bei anderen Audiogeräten werden die MIDI-Geräte durch einen Geräte Bezeichner identifiziert, der implizit von der Anzahl der in einem bestimmten System vorhandenen Geräte bestimmt wird. Geräte Bezeichner reichen von Null bis zur Anzahl der vorhandenen Geräte, minus 1. Wenn z. b. zwei MIDI-Ausgabegeräte in einem System vorhanden sind, sind gültige Geräte Bezeichner 0 und 1.

Nachdem Sie festgelegt haben, wie viele Eingabe-oder Ausgabegeräte in einem System vorhanden sind, können Sie sich über die Funktionen der einzelnen Geräte informieren. Windows stellt die folgenden Funktionen bereit, um die Funktionen von Audiogeräten zu bestimmen.



| Wert                                          | Bedeutung                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**midiingetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | Ruft die Funktionen eines angegebenen MIDI-Eingabe Geräts ab und platziert diese Informationen in der [**midiincaps**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) -Struktur.    |
| [**midioutgetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | Ruft die Funktionen eines angegebenen Ausgabegeräts von MIDI ab und platziert diese Informationen in der [**midioutcaps**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) -Struktur. |



 

Jede dieser Funktionen verfügt über einen Parameter, der die Adresse einer Struktur angibt, die die Funktion mit Informationen zu den Funktionen eines bestimmten Geräts füllt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MIDI-Dienste](midi-services.md)
</dt> </dl>

 

 