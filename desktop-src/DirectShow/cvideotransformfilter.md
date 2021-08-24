---
description: Die CVideoTransformFilter-Klasse ist in erster Linie als Basisklasse für AVI-Dekomprimierungsfilter konzipiert.
ms.assetid: 8eb87f9f-24b3-4dbe-a390-54db993d2724
title: CVideoTransformFilter-Klasse
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
ms.openlocfilehash: a1e1a1b717aeb2814b469fc34a9e038052abb6720dde0ed75982f27716978de5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907005"
---
# <a name="cvideotransformfilter-class"></a>CVideoTransformFilter-Klasse

![cvideotransformfilter-Klassenhierarchie](images/vtsip01.png)

Die `CVideoTransformFilter` -Klasse ist in erster Linie als Basisklasse für AVI-Dekomprimierungsfilter konzipiert. Diese Klasse fügt der [**CTransformFilter-Klasse**](ctransformfilter.md) Unterstützung für die Qualitätskontrolle hinzu. Die **Receive-Methode** des Filters kann basierend auf Qualitätsmeldungen des Renderers und Leistungsmessungen, die der Filter während des Streamings sammelt, Frames löschen.

Wenn der Filter einen Frame löscht, werden Frames so lange abfällt, bis er den nächsten Keyframe erreicht. Bei MPEG-Streams unterscheidet der Filter nicht zwischen B-Frames und P-Frames.



| Geschützte Membervariablen                                                      | BESCHREIBUNG                                                                                    |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**m \_ bQualityChanged**](cvideotransformfilter-m-bqualitychanged.md)           | Gibt an, ob der Filter Frames gelöscht hat.                                               |
| [**m \_ bSkipping**](cvideotransformfilter-m-bskipping.md)                       | Gibt an, ob der Filter derzeit Frames ausgibt.                                     |
| [**m \_ itrAvgDecode**](cvideotransformfilter-m-itravgdecode.md)                 | Durchschnittliche Zeitdauer, die zum Decodieren eines Frames gedauert hat.                                         |
| [**m \_ itrLate**](cvideotransformfilter-m-itrlate.md)                           | Gibt an, wie spät die Beispiele beim Renderer eintreffen.                                   |
| [**m \_ nFramesSinceKeyFrame**](cvideotransformfilter-m-nframessincekeyframe.md) | Die Anzahl der Frames, die der Filter seit dem letzten Keyframe empfangen hat.                    |
| [**m \_ nKeyFramePeriod**](cvideotransformfilter-m-nkeyframeperiod.md)           | Das größte beobachtete Intervall zwischen Keyframes.                                              |
| [**m \_ nWaitForKey**](cvideotransformfilter-m-nwaitforkey.md)                   | Die aktuelle maximale Anzahl der zu verdringten Deltaframes.                                            |
| [**m \_ tDecodeStart**](cvideotransformfilter-m-tdecodestart.md)                 | Die Zeitdauer, die zum Decodieren des letzten Beispiels gedauert hat.                                  |
| Geschützte Methoden                                                               | BESCHREIBUNG                                                                                    |
| [**AbortPlayback**](cvideotransformfilter-abortplayback.md)                    | Wird verwendet, um einen Streamingfehler zu signalisieren.                                                              |
| [**AlterQuality**](cvideotransformfilter-alterquality.md)                      | Benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird.                                        |
| [**Erhalten**](cvideotransformfilter-receive.md)                                | Empfängt ein Medienbeispiel, verarbeitet es und übergibt ein Ausgabebeispiel an den Downstreamfilter. |
| [**ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md)                | Bestimmt, ob der Filter ein angegebenes Beispiel ablegen soll.                                  |
| [**StartStreaming**](cvideotransformfilter-startstreaming.md)                  | Wird aufgerufen, wenn der Filter in den angehaltenen Zustand wechselt.                                           |
| Öffentliche Methoden                                                                  | BESCHREIBUNG                                                                                    |
| [**CVideoTransformFilter**](cvideotransformfilter-cvideotransformfilter.md)    | Konstruktormethode.                                                                            |
| [**EndFlush**](cvideotransformfilter-endflush.md)                              | Beendet einen Leerungsvorgang.                                                                        |



 

 

 



