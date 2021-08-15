---
title: Abfragen von ABFRAGEGERÄTEN
description: Abfragen von ABFRAGEGERÄTEN
ms.assetid: 0c9882a7-b5cb-41d1-a52e-003112225035
keywords:
- Instrumentieren der digitalen Schnittstelle (INSTRUMENT Digital Interface, INSTRUMENT), Abfragen von Geräten
- INSTRUMENTS (Music Instrument Digital Interface),Abfragen von Geräten
- DIENSTEN,Abfragen von Geräten
- Abfragen von MESSGERÄTE-Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3546971a17a5a8002f0e6d4205ceee5ca796babeb2b27df911cfca5a5911371c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372315"
---
# <a name="querying-midi-devices"></a>Abfragen von ABFRAGEGERÄTEN

Vor dem Wiedergeben oder Aufzeichnen von CSV-Daten müssen Sie die Funktionen der IM System vorhandenen HARDWARE bestimmen. DIE FUNKTION VON CAN kann von einem Multimediacomputer zum nächsten variieren. -Anwendungen sollten keine Annahmen über die Hardware treffen, die in einem bestimmten System vorhanden ist.

Windows stellt die folgenden Funktionen bereit, um zu bestimmen, wie viele DER GERÄTE für die Ein- oder Ausgabe in einem bestimmten System verfügbar sind.



| Wert                                          | Bedeutung                                                            |
|------------------------------------------------|--------------------------------------------------------------------|
| [**partsInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)   | Ruft die Anzahl der im System vorhandenen INPUT-Geräte ab.  |
| [**partsOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs) | Ruft die Anzahl der im System vorhandenen OUTPUT-Geräte ab. |



 

Wie andere Audiogeräte werden AUCH-Geräte durch einen Gerätebezeichner identifiziert, der implizit anhand der Anzahl der in einem bestimmten System vorhandenen Geräte bestimmt wird. Gerätebezeichner reichen von 0 (null) bis zur Anzahl der vorhandenen Geräte minus 1. Wenn ein System z. B. zwei OUTPUT-Geräte enthält, sind die gültigen Gerätebezeichner 0 und 1.

Nachdem Sie ermittelt haben, wie viele EIN- oder Ausgabegeräte in einem System vorhanden sind, können Sie sich über die Funktionen der einzelnen Geräte informieren. Windows stellt die folgenden Funktionen bereit, um die Funktionen von Audiogeräten zu bestimmen.



| Wert                                          | Bedeutung                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**partsInGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)   | Ruft die Funktionen eines angegebenen CAB-Eingabegeräts ab und platziert diese Informationen in der [**STRUKTUR VON CABINCAPS.**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)    |
| [**partsOutGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps) | Ruft die Funktionen eines bestimmten CAB-Ausgabegeräts ab und platziert diese Informationen in der [**STRUKTUR VON CABOUTCAPS.**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps) |



 

Jede dieser Funktionen verfügt über einen Parameter, der die Adresse einer Struktur angibt, die die Funktion mit Informationen zu den Funktionen eines angegebenen Geräts ausfüllt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PARTS-Dienste](midi-services.md)
</dt> </dl>

 

 