---
title: Abfragen vonENDE-Geräten
description: Abfragen vonENDE-Geräten
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- InstrumentIeren der digitalen Schnittstelle (KEYBOARD), Abfragen von Geräten
- ENDE (Keyboard Instrument Digital Interface), Abfragen von Geräten
- ENDE-Dienste,Abfragen von Geräten
- Abfragen vonENDE-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3546971a17a5a8002f0e6d4205ceee5ca796babeb2b27df911cfca5a5911371c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372315"
---
# <a name="querying-midi-devices"></a>Abfragen vonENDE-Geräten

Bevor Sie DIE-Daten wiedergeben oder aufzeichnen, müssen Sie die Funktionen der IM SYSTEM-Hardware bestimmen. DIE-Funktion kann von Multimediacomputer zu Multimediacomputer variieren. -Anwendungen sollten keine Annahmen über die Hardware treffen, die in einem bestimmten System vorhanden ist.

Windows stellt die folgenden Funktionen bereit, um zu bestimmen, wie viele DER Geräte in einem bestimmten System für die Eingabe oder Ausgabe verfügbar sind.



| Wert                                          | Bedeutung                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [**beiinGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | Ruft die Anzahl der IMT-Eingabegeräte ab, die im System vorhanden sind.  |
| [**ohneGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | Ruft die Anzahl der IMT-Ausgabegeräte ab, die im System vorhanden sind. |



 

Wie andere Audiogeräte werden AUCH-Geräte durch eine Geräte-ID identifiziert, die implizit anhand der Anzahl der geräte in einem bestimmten System bestimmt wird. Gerätebezeichner reichen von null bis zur Anzahl der geräte vorhanden, minus eins. Wenn z. B. zwei OUTPUT-Geräte in einem System enthalten sind, sind die gültigen Gerätebezeichner 0 und 1.

Nachdem Sie ermittelt haben, wie viele EINGABE- oder Ausgabegeräte in einem System vorhanden sind, können Sie sich über die Funktionen der einzelnen Geräte informieren. Windows stellt die folgenden Funktionen bereit, um die Funktionen von Audiogeräten zu bestimmen.



| Wert                                          | Bedeutung                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**mussinGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | Ruft die Funktionen eines angegebenen EINGABEGERÄTs ab und platziert diese Informationen in der [**FORMATINCAPS-Struktur.**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)    |
| [**ohneGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | Ruft die Funktionen eines angegebenen OUTPUT-Ausgabegeräts ab und platziert diese Informationen in der [**STRUKTUR DES AUSDRUCKOUTCAPS.**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) |



 

Jede dieser Funktionen verfügt über einen Parameter, der die Adresse einer -Struktur angibt, die die Funktion mit Informationen zu den Funktionen eines angegebenen Geräts auffüllt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[KEYBOARD-Dienste](midi-services.md)
</dt> </dl>

 

 