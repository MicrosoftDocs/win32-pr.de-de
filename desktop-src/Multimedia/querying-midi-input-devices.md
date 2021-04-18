---
title: Abfragen von MIDI-Eingabegeräten
description: Abfragen von MIDI-Eingabegeräten
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- Digital Instrumentation Digital Interface (MIDI), Eingabegeräte
- MIDI (Digital Instrumentation Digital Interface), Eingabegeräte
- Aufzeichnen von MIDI-Audiodaten, Eingabegeräte
- MIDI-Eingabegeräte
- Digital Instrumentation Digital Interface (MIDI), Abfragen von Eingabegeräten
- MIDI (Digital Instrumentation Digital Interface), Abfragen von Eingabegeräten
- Aufzeichnen von MIDI-Audiodaten, Abfragen von Eingabegeräten
- Abfragen von MIDI-Eingabegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a92bec8733887e20c25f37d1de3dd493e555c8a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337221"
---
# <a name="querying-midi-input-devices"></a>Abfragen von MIDI-Eingabegeräten

Vor dem Aufzeichnen von MIDI-Audiodaten sollten Sie die Funktion " [**midiingetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) " verwenden, um die Funktionen des im System vorhandenen MIDI-Eingabe Geräts zu ermitteln. Diese Funktion verwendet eine Adresse einer [**midiincaps**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) -Struktur, die Informationen zu den Funktionen des jeweiligen Geräts füllt. Diese Informationen umfassen die Hersteller-und Produkt-IDs, einen Produktnamen für das Gerät und die Versionsnummer des Gerätetreibers.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von MIDI-Audiodateien](recording-midi-audio.md)
</dt> </dl>

 

 