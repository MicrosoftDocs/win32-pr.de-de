---
title: Vorabladen von Patches mit internen SYNTHESIZER-Synthesizern
description: Vorabladen von Patches mit internen SYNTHESIZER-Synthesizern
ms.assetid: c200aa91-ab91-48e8-b3b5-8e7f36e511be
keywords:
- Instrument Digital Interface (INSTRUMENTS), interne Synthesizer
- INSTRUMENTS (Music Instrument Digital Interface), interne Synthesizer
- Wiedergabe von DATEIEN, interne Synthesizer
- interne SYNTHESIZER
- Music Instrument Digital Interface (OPC), Vorabladen von Patches
- INSTRUMENTS (Music Instrument Digital Interface),Vorabladen von Patches
- WIEDERGEBEN VON DATEIEN, Vorabladen von Patches
- Vorabladen von PATCH-Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de389e058c015c38d05fb8ff2a960ca3ef75a662faa6a1ce519c26afe14f09b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372497"
---
# <a name="preloading-patches-with-internal-midi-synthesizers"></a>Vorabladen von Patches mit internen SYNTHESIZER-Synthesizern

Einige interne SYNTHESIZER-Geräte können nicht alle patches gleichzeitig laden. Diese Geräte müssen ihre Patchdaten vorab laden.

Windows stellt die folgenden Funktionen bereit, um anzufordern, dass ein Synthesizer angegebene Patches vorab lädt und zwischenspeichert.



| Wert                                                      | Bedeutung                                                                                                     |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**cacheOutCachePatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)         | Fordert an, dass ein internes SYNTHESIZER-Gerät angegebene dic-Patches vorab lädt und zwischenspeichert.              |
| [**partsOutCacheDrumPatches**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches) | Fordert an, dass ein internes SYNTHESIZER-Gerät angegebene schlüsselbasierte Patches vorab lädt und zwischenspeichert. |



 

Informationen zum Bestimmen, ob ein bestimmtes Gerät das Vorabladen von Patches unterstützt, finden Sie unter [Abfragen von AUSGABEGERÄTEN.](querying-midi-output-devices.md)

 

 