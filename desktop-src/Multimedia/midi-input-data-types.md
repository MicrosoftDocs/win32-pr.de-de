---
title: EINGABE-Datentypen
description: EINGABE-Datentypen
ms.assetid: c67f149e-60b8-4f9e-8e3c-a88cd579d29f
keywords:
- Instrument Digital Interface (KEYBOARD), Eingabedatentypen
- SIGNATURE (Keyboard Instrument Digital Interface), Eingabedatentypen
- Aufzeichnung von audio,input data types
- EINGABEDATENTYPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3cb45c321cdac95c09274f25293f4635d5a715638367c8f9e06cf5c45777af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525220"
---
# <a name="midi-input-data-types"></a>EINGABE-Datentypen

Windows definiert die folgenden Datentypen für die EINGABEFUNKTIONEN des -Eingabetyps.



| Wert                            | Bedeutung                                                                                                                                                                                     |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **HMIDIIN**                      | Handle eines EINGABE-Eingabegeräts.                                                                                                                                                              |
| [**KEYBOARDHDR**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)       | Header für einen Streampuffer oder einen Block mit system-exklusiven SYSTEM-Daten. Bei Eingabeanwendungen zeichnet diese Struktur nur system exklusive Daten auf (Streaming wird für die EINGABE-Eingabe nicht unterstützt). |
| [**KEYBOARDINCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps) | Struktur, die verwendet wird, um die Funktionen eines EINGABE-Eingabegeräts zu untersuchen.                                                                                                                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von TONS-Audio](recording-midi-audio.md)
</dt> </dl>

 

 