---
description: Die cvideotransformfilter-Klasse ist hauptsächlich als Basisklasse für AVI-dedaemon-Filter konzipiert.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: Cvideotransformfilter-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter
api_type:
- COM
api_location: ''
ms.openlocfilehash: 360f46eb7242de01d5e734c5efa17399f23adf7d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860515"
---
# <a name="cvideotransformfilter-class"></a>Cvideotransformfilter-Klasse

![cvideotransformfilter-Klassenhierarchie](images/vtsip01.png)

Die- `CVideoTransformFilter` Klasse ist hauptsächlich als Basisklasse für AVI-Dekompressor-Filter konzipiert. Diese Klasse fügt der [**ctransformfilter**](ctransformfilter.md) -Klasse Unterstützung für die Qualitätskontrolle hinzu. Die **Receive** -Methode des Filters kann festlegen, ob Frames auf der Grundlage von Qualitäts Meldungen vom Renderer und Leistungsmessungen, die der Filter beim Streaming sammelt, gelöscht werden sollen.

Wenn der Filter einen Frame löscht, werden die Frames so lange gelöscht, bis der nächste Keyframe erreicht wird. Bei MPEG-Streams unterscheidet der Filter nicht zwischen B-Frames und P-Frames.



| Geschützte Member-Variablen                                                      | BESCHREIBUNG                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ bqualitychanged**](cvideotransformfilter-m-bqualitychanged.md)           | Gibt an, ob der Filter Frames gelöscht hat.                                               |
| [**m \_ bskipping**](cvideotransformfilter-m-bskipping.md)                       | Gibt an, ob der Filter derzeit Frames löscht.                                     |
| [**m \_ itravgdecode**](cvideotransformfilter-m-itravgdecode.md)                 | Die durchschnittliche Zeitspanne, die zum Decodieren eines Frames benötigt wurde.                                         |
| [**m \_ itrlate**](cvideotransformfilter-m-itrlate.md)                           | Gibt an, wie spät die Stichproben am Renderer eintreffen.                                   |
| [**m \_ nframessincekeyframe**](cvideotransformfilter-m-nframessincekeyframe.md) | Die Anzahl der Frames, die der Filter seit dem letzten Keyframe empfangen hat.                    |
| [**m \_ nkeyframeperiod**](cvideotransformfilter-m-nkeyframeperiod.md)           | Das größte beobachtete Intervall zwischen Keyframes.                                              |
| [**m \_ nwaitforkey**](cvideotransformfilter-m-nwaitforkey.md)                   | Die aktuelle maximale Anzahl der zu löschenden Delta Frames.                                            |
| [**m \_ tdecodestart**](cvideotransformfilter-m-tdecodestart.md)                 | Die Zeitspanne, die zum Decodieren des neuesten Beispiels benötigt wurde.                                  |
| Geschützte Methoden                                                               | BESCHREIBUNG                                                                                    |
| [**Abbruch Wiedergabe**](cvideotransformfilter-abortplayback.md)                    | Wird verwendet, um einen Streamingfehler zu signalisieren.                                                              |
| [**Alterquality**](cvideotransformfilter-alterquality.md)                      | Benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird.                                        |
| [**Medizinisch**](cvideotransformfilter-receive.md)                                | Empfängt ein Medien Beispiel, verarbeitet es und stellt ein Ausgabe Beispiel für den downstreamfilter bereit. |
| [**Schuldskipframe**](cvideotransformfilter-shouldskipframe.md)                | Bestimmt, ob der Filter eine angegebene Stichprobe löschen soll.                                  |
| [**Startstreaming**](cvideotransformfilter-startstreaming.md)                  | Wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt.                                           |
| Öffentliche Methoden                                                                  | BESCHREIBUNG                                                                                    |
| [**Cvideotransformfilter**](cvideotransformfilter-cvideotransformfilter.md)    | Konstruktormethode.                                                                            |
| [**Endflush**](cvideotransformfilter-endflush.md)                              | Beendet einen Löschvorgang.                                                                        |



 

 

 



