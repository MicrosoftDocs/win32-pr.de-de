---
title: Abfragen von MIDI-Ausgabegeräten
description: Abfragen von MIDI-Ausgabegeräten
ms.assetid: c6a33a4e-c61a-4e06-805e-5128a97f5199
keywords:
- Digital Instrumentation Digital Interface (MIDI), Ausgabegeräte
- MIDI (Digital Instrumentation Digital Interface), Ausgabegeräte
- Abspielen von MIDI-Dateien, Ausgabe von Geräten
- MIDI-Ausgabegeräte
- Digital Instrumentation Digital Interface (MIDI), Abfragen von Ausgabegeräten
- MIDI (Digital Instrumentation Digital Interface), Abfragen von Ausgabegeräten
- Abspielen von MIDI-Dateien, Abfragen von Ausgabegeräten
- Abfragen von MIDI-Ausgabegeräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292fbacbb4acf182d566e8c98832dfb0f993ea2b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106342126"
---
# <a name="querying-midi-output-devices"></a>Abfragen von MIDI-Ausgabegeräten

Vor der Wiedergabe einer MIDI-Datei sollten Sie die Funktion " [**midioutgetdevcaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) " verwenden, um die Funktionen des im System vorhandenen Ausgabegeräts von MIDI zu ermitteln. Diese Funktion verwendet eine Adresse einer [**midioutcaps**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) -Struktur, die Informationen zu den Funktionen des jeweiligen Geräts füllt. Diese Informationen umfassen die Hersteller-und Produkt-IDs, einen Produktnamen für das Gerät und die Versionsnummer des Gerätetreibers (angegeben in den Membern **wmid**, **wpid**, **szpname** und **vdriverversion** ).

Bei der Ausgabe von MIDI-Geräten kann es sich entweder um interne oder externe, von der Ausgabe Ports von MIDI Der **wtechnology** -Member der **midioutcaps** -Struktur gibt die Technologie des Geräts an.

Wenn es sich bei dem Gerät um einen internen Synthesizer handelt, sind zusätzliche Geräteinformationen in den Elementen **wvoices**, **wnotes** und **wchannelmask** verfügbar. Das **wvoices** -Element gibt die Anzahl der Stimmen an, die das Gerät unterstützt. Jede Stimme kann einen anderen Sound oder ein anderes Timbre aufweisen. Stimmen sind in den MIDI-Kanälen organisiert. Der **wnotes** -Member gibt die *Polyphonie* des Geräts an, d. –. die maximale Anzahl von Notizen, die gleichzeitig wiedergegeben werden können. Der **wchannelmask** -Member ist eine Bitdarstellung der MIDI-Kanäle, auf die das Gerät antwortet. Wenn das Gerät z. b. auf die ersten acht MIDI-Kanäle antwortet, ist **wchannelmask** 0x00FF. Wenn das Gerät ein externer Ausgabeport ist, werden **wstimmen** und **wnotes** nicht verwendet, und **wchannelmask** wird auf 0xFFFF festgelegt.

Der **dwsupport** -Member der **midioutcaps** -Struktur gibt an, ob der Gerätetreiber volumeänderungen, patchcaching und Streaming unterstützt. Volumeänderungen werden nur von internen Synthesizer-Geräten unterstützt. Externe MIDI-Ausgabeports unterstützen keine volumeänderungen. Weitere Informationen zum Ändern des Volumes finden Sie unter [Ändern des internen MIDI-synthesizervolumes](changing-internal-midi-synthesizer-volume.md).

 

 