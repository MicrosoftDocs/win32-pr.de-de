---
title: Abfragen von EINGABEGERÄTEN
description: Abfragen von EINGABEGERÄTEN
ms.assetid: 2da88418-f9cf-49da-b17f-8a26d357b5ab
keywords:
- Instrument Digital Interface (INSTRUMENTS), Eingabegeräte
- INSTRUMENTS (Music Instrument Digital Interface), Eingabegeräte
- Aufzeichnen von AUDIO, Eingabegeräten
- INPUT-Eingabegeräte
- Instrumentieren der digitalen Schnittstelle (INSTRUMENT Digital Interface, INSTRUMENT), Abfragen von Eingabegeräten
- INSTRUMENTS (Music Instrument Digital Interface),Abfragen von Eingabegeräten
- Aufzeichnen von SOUND-Audio, Abfragen von Eingabegeräten
- Abfragen von EINGABEGERÄTEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81340f767c1ef3acf3105f78d2cef000f7548361b387e6887ecc4136437dbe6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371932"
---
# <a name="querying-midi-input-devices"></a>Abfragen von EINGABEGERÄTEN

Vor der Aufzeichnung von AUDIOdaten sollten Sie die [**Funktion "inputsInGetDevCaps"**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps) verwenden, um die Funktionen des IM System vorhandenen EINGABEGERÄTs zu bestimmen. Diese Funktion verwendet eine Adresse einer [**CABINCAPS-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) die sie mit Informationen über die Funktionen des angegebenen Geräts auffüllt. Diese Informationen umfassen die Hersteller- und Produktbezeichner, einen Produktnamen für das Gerät und die Versionsnummer des Gerätetreibers.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Recording RECORDING Audio (Aufzeichnen von AUDIO)](recording-midi-audio.md)
</dt> </dl>

 

 