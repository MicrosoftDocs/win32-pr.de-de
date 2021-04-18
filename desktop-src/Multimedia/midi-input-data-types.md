---
title: Datentypen der MIDI-Eingabe
description: Datentypen der MIDI-Eingabe
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- Digital Instrumentation Digital Interface (MIDI), Eingabe Datentypen
- MIDI (Digital Instrumentation Digital Interface), Eingabe Datentypen
- Aufzeichnen von MIDI-Audiodaten, Eingabe Datentypen
- Datentypen der MIDI-Eingabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8f0738827cce4cfd8cb4a237dcd2031c2fe71a7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340264"
---
# <a name="midi-input-data-types"></a>Datentypen der MIDI-Eingabe

Windows definiert die folgenden Datentypen für die MIDI-Eingabefunktionen.



| Wert                            | Bedeutung                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Hmidiin**                      | Handle eines MIDI-Eingabe Geräts.                                                                                                                                                              |
| [**Midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | Header für einen Streampuffer oder einen Block von System exklusiven systemeigenen Systemdaten. Bei Eingabe Anwendungen zeichnet diese Struktur nur System exklusive Daten auf (das Streaming wird für eine MIDI-Eingabe nicht unterstützt). |
| [**Midiincaps**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | Struktur, die verwendet wird, um die Funktionen eines MIDI-Eingabe Geräts zu Fragen.                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von MIDI-Audiodateien](recording-midi-audio.md)
</dt> </dl>

 

 