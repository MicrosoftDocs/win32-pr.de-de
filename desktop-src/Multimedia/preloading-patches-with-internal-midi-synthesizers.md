---
title: Vorab Laden von Patches mit internen MIDI-Synthesizern
description: Vorab Laden von Patches mit internen MIDI-Synthesizern
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- Digital Instrumentation Digital Interface (MIDI), interne Synthesizer
- MIDI (Digital Instrumentation Digital Interface), interne Synthesizer
- Abspielen von MIDI-Dateien, internen Synthesizern
- Interne MIDI-Synthesizer
- Digital Instrumentation Digital Interface (MIDI), vorab Laden von Patches
- MIDI (Digital Instrumentation Digital Interface), vorab Laden von Patches
- Abspielen von MIDI-Dateien, vorab Laden von Patches
- vorab Laden von MIDI-Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc54eccdaa0a0c9aa16f206e7e036f322b615d96
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948651"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a>Vorab Laden von Patches mit internen MIDI-Synthesizern

Bei einigen internen Geräten mit einem MIDI-Synthesizer können nicht alle Patches gleichzeitig geladen werden. Diese Geräte müssen die Patchdaten vorab laden.

Windows stellt die folgenden Funktionen bereit, um anzufordern, dass ein Synthesizer bestimmte Patches vorab lädt und zwischenspeichert.



| Wert                                                      | Bedeutung                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**midioutcachepatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | Fordert an, dass ein internes MIDI-Synthesizer-Gerät vorab geladen und zwischen angegebene melodische Patches zwischenspeichert.              |
| [**midioutcachedrumpatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | Fordert an, dass ein internes MIDI-Synthesizer-Gerät bestimmte Schlüssel basierte Percussion-Patches vorab lädt und zwischenspeichert. |



 

Informationen dazu, wie Sie bestimmen können, ob ein bestimmtes Gerät das vorab Laden von Patches unterstützt, finden Sie unter [Abfragen von MIDI-Ausgabegeräten](querying-midi-output-devices.md).

 

 