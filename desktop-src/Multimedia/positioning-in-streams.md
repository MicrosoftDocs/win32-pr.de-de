---
title: Positionieren in Streams
description: Positionieren in Streams
ms.assetid: 97ab491d-1a58-4b4b-a13a-215be24dac1c
keywords:
- AVIStreamStart-Funktion
- Avistreamfindsample-Funktion
- Avistreamsampleto Time-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252aa938d32c323da9fcf7ae106d11db0ff2fb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709864"
---
# <a name="positioning-in-streams"></a>Positionieren in Streams

Avifile bietet mehrere Möglichkeiten, um eine Position in einem Datenstrom zu suchen und zu verschieben. Die Funktionen und Makros in diesem Abschnitt ermöglichen der Anwendung die Suche nach der Anfangsposition, der Länge und den Keyframes (mit einem kompletten Bild im Beispiel) innerhalb eines Streams. Die Funktionen und Makros ordnen auch Zeit mit Positionen in einem Stream zu, indem Sie die verstrichene Zeit berechnen, die benötigt wird, um einen Stream von Anfang an an einem beliebigen Punkt in einem Stream wiederzugeben.

## <a name="finding-the-starting-position"></a>Ermitteln der Anfangs Position

Sie können die Beispiel Nummer des ersten Frames in einem Videostream mit der [**AVIStreamStart**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart) -Funktion abrufen. (Abhängig von der Einstellung des Autors können die Rahmen eines Films mit dem Beispiel 0 oder 1 beginnen.) Sie können diese Informationen auch mit der [**AVISTREAMINFO**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) -Funktion abrufen. Diese Funktion speichert die Beispiel Zahl im **dwstart** -Member der [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) -Struktur. Sie können die Startzeit für das erste Beispiel eines Streams mit dem [**avistreamstarttime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime) -Makro abrufen.

Sie können die Streamlänge mit der [**avistreamlength**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength) -Funktion abrufen. Diese Funktion gibt die Anzahl der Stichproben im Stream zurück. Sie können diese Informationen auch mit der **AVISTREAMINFO** -Funktion abrufen. Diese Funktion speichert die Länge des Streams im **dwLength** -Member der **AVISTREAMINFO** -Struktur. Um die Länge eines Streams in Millisekunden abzurufen, verwenden Sie das [**avistreamverläntime**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime) -Makro.

In einem Videostream entspricht jedes Beispiel in der Regel einem Video Video. Es können jedoch auch Beispiele vorhanden sein, für die keine Videodaten vorhanden sind. Wenn Sie die [**avistreamread**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) -Funktion aufrufen, die eine dieser Positionen angibt, wird eine Daten Länge von 0 Bytes zurückgegeben. Sie finden Beispiele, die Daten enthalten, mithilfe der [**avistreamfindsample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) -Funktion und der Angabe \_ eines Flags suchen.

In einem Audiostream entspricht jedes Beispiel einem Datenblock von Audiodaten. Wenn die Audiodaten z. b. das ADPCM-Format 22 kHz (Adaptive Differential Pulse Code Modulation) aufweisen, entspricht jedes Beispiel für **avistreamlength** einem Block von 256 Byte komprimierter Audiodaten. Dieser Block von Audiodaten enthält ungefähr 500 Audiobeispiele, wenn die Komprimierung nicht komprimiert ist. Die Funktionen und Makros von avifile behandeln jedoch jeden 256-Byte-Block als ein einzelnes Beispiel.

> [!Note]  
> Gültige Positionen innerhalb eines streambereichs zwischen dem Anfang und dem Ende des Streams, d. h. der Summe des Anfangs Punkts des Streams und seiner Länge. Die durch die Summe der Anfangsposition dargestellte Position und die Länge entsprechen einer Zeit, nachdem die letzten Daten gerendert wurden. Sie enthält keine Daten. Sie können die Beispiel Nummer, die das Ende des Streams darstellt, mit dem [**avistreamend**](/windows/desktop/api/Vfw/nf-vfw-avistreamend) -Makro abrufen. Sie können den Uhrzeitwert in Millisekunden abrufen, der das Ende des Streams darstellt, indem Sie das [**avistreamendtime**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime) -Makro verwenden.

 

## <a name="finding-sample-and-key-frames"></a>Suchen von Beispiel-und Keyframes

Mithilfe der [**avistreamfindsample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) -Funktion können Sie verschiedene Typen von Beispielen in einem Datenstrom suchen. Diese Funktion sucht rückwärts oder vorwärts durch einen Stream, um ein Beispiel des entsprechenden Typs zu erhalten, beginnend mit der angegebenen Stichproben Nummer. Sie können in einem Stream nach verschiedenen Typen von Beispielen suchen, indem Sie in der **avistreamfindsample** -Aufruf Sequenz ein Flag angeben. Geben Sie das \_ Flag suchen an, um nicht leere Beispiele zu suchen oder um Beispiele zu überspringen, bei denen Daten fehlen. Geben Sie das \_ schlüsselflag suchen an, um nach Keyframes zu suchen, die die Daten zum Rendering eines kompletten Bilds enthalten, ohne auf vorherige Frames verweisen zu müssen. Geben Sie das \_ Flag zum Suchen nach Format an, um nach Änderungen im Format zu suchen. **Avistreamfindsample** wird hauptsächlich mit Videostreams verwendet.

Mehrere Makros, die avifile-Funktionen verwenden, ergänzen die streamsuchfunktionen. Die folgende Liste enthält eine kurze Beschreibung der einzelnen Makros. Die Makros, die nach einer bestimmten Position oder einem Datentyp suchen, erfordern, dass ein Start Speicherort im Stream angegeben wird.



| Makro                                                                | Beschreibung                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**Avistreamiskeyframe**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)                   | Gibt an, ob ein Beispiel in einem angegebenen Stream ein Keyframe ist.                                                            |
| [**Avistreamnearestkeyframe**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)         | Gibt den Keyframe an der angegebenen Position in einem Stream an oder vor der angegebenen Position.                                                     |
| [**Avistreamnearestkeyframetime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime) | Bestimmt die Zeit, die dem Anfang des Keyframes entspricht, der einem angegebenen Zeitpunkt in einem Stream am nächsten liegt (oder vorher vorangestellt). |
| [**Avistreamnearestsample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)             | Die nächstgelegene, nicht leere Stichprobe wird an einer angegebenen Position in einem Stream platziert.                                       |
| [**Avistreamnearestsampletime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)     | Bestimmt die Zeit, die dem Anfang eines Beispiels entspricht, der einem bestimmten Zeitpunkt in einem Stream am nächsten liegt.             |
| [**Avistreamnextkeyframe**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)               | Gibt den nächsten Keyframe nach einer angegebenen Position in einem Stream an.                                                      |
| [**Avistreamnextkeyframetime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)       | Gibt die Zeit des nächsten Keyframes in einem Stream ab einem bestimmten Zeitpunkt zurück.                                               |
| [**Avistreamnextsample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)                   | Gibt das nächste nicht leere Beispiel von einer angegebenen Position in einem Stream an.                                                     |
| [**Avistreamnextsampletime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)           | Gibt die Uhrzeit zurück, zu der ein Beispiel für das nächste Beispiel im Stream geändert wird.                                                    |
| [**Avistreamprevkeyframe**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)               | Gibt den Keyframe an, der einer angegebenen Position in einem Stream vorangestellt ist.                                                       |
| [**Avistreamprevkeyframetime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)       | Gibt die Zeit des vorherigen Keyframes im Stream zurück, beginnend zu einem bestimmten Zeitpunkt.                                         |
| [**Avistreamprevsample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)                   | Gibt das nicht leere Beispiel an, das einer angegebenen Position in einem Stream vorangestellt ist.                                                 |
| [**Avistreamprevsampletime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)           | Bestimmt die Zeit, zu der das vorherige Beispiel seinen Vorgänger im Stream ersetzt.                                    |
| [**Avistreamsampleprosample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)           | Gibt das Beispiel in einem Stream zurück, der zur gleichen Zeit wie ein Beispiel in einem zweiten Stream auftritt.                     |



 

## <a name="switching-between-samples-and-time"></a>Wechseln zwischen Beispielen und Zeit

Mithilfe der [**avistreamsampledetime**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime) -Funktion können Sie die verstrichene Zeit zwischen dem Anfang eines Datenstroms und einem Beispiel ermitteln. Diese Funktion konvertiert die Stichproben Nummer in einen Zeitwert, der in Millisekunden ausgedrückt wird. Bei einem Videorahmen (der mehrere Millisekunden umfasst) ist dieser Wert die Zeit, zu der die Stichprobe beginnt, seit der Wiedergabe begonnen wurde, und es wird davon ausgegangen, dass der Videoclip bei normaler Geschwindigkeit abgespielt wird Bei einem Audiobeispiel (das mehrere Beispiele in einer Millisekunde enthält) entspricht der Zeitwert dem Zeitpunkt, an dem die Stichprobe beginnt, und geht davon aus, dass der Audiostream bei normaler Geschwindigkeit abgespielt wird.

Umgekehrt können Sie die mit einem Uhrzeitwert verknüpfte Beispiel Nummer mithilfe der [**avistreamtimeto Sample**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample) -Funktion suchen. Diese Funktion konvertiert den Millisekundenwert in eine Stichproben Nummer und geht davon aus, dass der Videoclip bei normaler Geschwindigkeit abgespielt wird.

Da **avistreamsampleumtime** die Zeit zurückgibt, zu der ein Frame abgespielt wird, ist die Beziehung zwischen **avistreamsampleumtime** und **avistreamtimeto Sample** nicht wirklich umgekehrt. Sie bestimmen die Position in einer Datei mehr, als Sie die Zeit bestimmen. Beispielsweise können zwei aufeinander folgende Audiobeispiele in der gleichen Millisekunde abgespielt werden. Die Verwendung von **avistreamsampleumtime** zum Konvertieren der Beispiel Zahlen würde zu identischen Uhrzeitwerten führen. Wenn Sie den Uhrzeitwert mithilfe von **avistreamtimeumsample** wieder in eine Beispiel Zahl konvertieren, wird auf ein einzelnes Beispiel verwiesen.

 

 




