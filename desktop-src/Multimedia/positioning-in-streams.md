---
title: Positionierung in Streams
description: Positionierung in Streams
ms.assetid: 97ab491d-1a58-4b4b-a13a-215be24dac1c
keywords:
- AVIStreamStart-Funktion
- AVIStreamFindSample-Funktion
- AVIStreamSampleToTime-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0528fea9ea10e28a418d253bd1abe6c599a952fe95a8c8f6c86807abe0e41159
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805860"
---
# <a name="positioning-in-streams"></a>Positionierung in Streams

AVIFile bietet mehrere Möglichkeiten zum Suchen und Verschieben an eine Position in einem Datenstrom. Mit den Funktionen und Makros in diesem Abschnitt kann Ihre Anwendung die Anfangsposition, Länge und Keyframes (die ein vollständiges Bild im Beispiel enthalten) in einem Stream finden. Die Funktionen und Makros ordnen die Zeit auch Positionen in einem Stream zu, indem sie die verstrichene Zeit berechnen, die benötigt wird, um einen Stream von seinem Anfang bis zu einem beliebigen Punkt in einem Stream wiederzuspielen.

## <a name="finding-the-starting-position"></a>Suchen der Anfangsposition

Sie können die Beispielnummer des ersten Frames in einem Videostream mithilfe der [**AVIStreamStart-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreamstart) abrufen. (Die Frames eines Films können je nach Präferenz des Autors bei Sample 0 oder 1 beginnen.) Sie können diese Informationen auch mithilfe der [**AVIStreamInfo-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreaminfoa) abrufen. Diese Funktion speichert die Beispielnummer im **dwStart-Member** der [**AVISTREAMINFO-Struktur.**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) Sie können die Startzeit des ersten Beispiels eines Streams mithilfe des [**MAKROS AVIStreamStartTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamstarttime) abrufen.

Sie können die Streamlänge mithilfe der [**AVIStreamLength-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreamlength) abrufen. Diese Funktion gibt die Anzahl der Stichproben im Stream zurück. Sie können diese Informationen auch mithilfe der **AVIStreamInfo-Funktion** abrufen. Diese Funktion speichert die Streamlänge im **dwLength-Member** der **AVISTREAMINFO-Struktur.** Verwenden Sie das [**AVIStreamLengthTime-Makro,**](/windows/desktop/api/Vfw/nf-vfw-avistreamlengthtime) um die Länge eines Streams in Millisekunden abzurufen.

In einem Videostream entspricht jedes Beispiel im Allgemeinen einem Videoframe. Es kann jedoch Beispiele geben, für die keine Videodaten vorhanden sind. Wenn Sie die [**AVIStreamRead-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) aufrufen, die eine dieser Positionen angibt, wird eine Datenlänge von 0 Bytes zurückgegeben. Sie finden Beispiele, die Daten enthalten, indem Sie die [**FUNKTION AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) verwenden und das FIND \_ ANY-Flag angeben.

In einem Audiostream entspricht jedes Beispiel einem Datenblock von Audiodaten. Wenn die Audiodaten z. B. ein ADPCM-Format mit 22 kHz (Adaptive Differential Pulse Code Code) aufweisen, entspricht jedes Beispiel für **AVIStreamLength** einem Block mit 256 Bytes komprimierter Audiodaten. Dieser Block von Audiodaten enthält ca. 500 Audiobeispiele, wenn diese nicht komprimiert sind. Die Funktionen und Makros von AVIFile behandeln jedoch jeden 256-Byte-Block als einzelnes Beispiel.

> [!Note]  
> Gültige Positionen innerhalb eines Datenstrombereichs vom Anfang bis zum Ende des Streams, also die Summe des Streamstartpunkts und seiner Länge. Die Position, die durch die Summe der Anfangsposition und der Länge dargestellt wird, entspricht einem Zeitpunkt, nach dem die letzten Daten gerendert wurden. sie enthält keine Daten. Sie können die Beispielnummer, die das Ende des Streams darstellt, mithilfe des [**MAKROS AVIStreamEnd**](/windows/desktop/api/Vfw/nf-vfw-avistreamend) abrufen. Sie können den Zeitwert in Millisekunden abrufen, der das Ende des Streams darstellt, indem Sie das [**AVIStreamEndTime-Makro**](/windows/desktop/api/Vfw/nf-vfw-avistreamendtime) verwenden.

 

## <a name="finding-sample-and-key-frames"></a>Suchen von Beispiel- und Keyframes

Sie können in einem Stream mithilfe der [**FUNKTION AVIStreamFindSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamfindsample) nach verschiedenen Arten von Beispielen suchen. Diese Funktion durchsucht einen Stream rückwärts oder vorwärts nach einem Beispiel des entsprechenden Typs, beginnend mit der von Ihnen angegebenen Beispielnummer. Sie können in einem Stream nach verschiedenen Arten von Beispielen suchen, indem Sie ein Flag in der **AUFRUFsequenz AVIStreamFindSample** angeben. Geben Sie das FLAG FIND \_ ANY an, um nicht genügend Stichproben zu finden oder Beispiele ohne Daten zu überspringen. Geben Sie das FLAG FIND \_ KEY an, um nach Keyframes zu suchen, die die Daten enthalten, um ein vollständiges Bild zu rendern, ohne auf vorherige Frames verweisen zu müssen. Geben Sie das FLAG FIND \_ FORMAT an, um nach Änderungen am Format zu suchen. **AVIStreamFindSample** wird hauptsächlich mit Videostreams verwendet.

Mehrere Makros, die AVIFile-Funktionen verwenden, ergänzen die Funktionen der Streamsuche. Die folgende Liste enthält eine kurze Beschreibung der einzelnen Makros. Die Makros, die nach einer bestimmten Position oder einem bestimmten Datentyp suchen, erfordern eine Startposition, die im Stream angegeben werden muss.



| Makro                                                                | Beschreibung                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [**AVIStreamIsKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamiskeyframe)                   | Gibt an, ob ein Beispiel in einem angegebenen Stream ein Keyframe ist.                                                            |
| [**AVIStreamStreamRestKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframe)         | Sucht den Keyframe an oder vor einer angegebenen Position in einem Stream.                                                     |
| [**AVIStreamStreamRestKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestkeyframetime) | Bestimmt die Zeit, die dem Anfang des Keyframes entspricht, der einer angegebenen Zeit in einem Stream am nächsten (oder vorangehend) ist. |
| [**AVIStreamStreamRestSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsample)             | Sucht die nächste nichtmpty-Stichprobe an oder vor einer angegebenen Position in einem Stream.                                       |
| [**AVIStreamStreamRestSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnearestsampletime)     | Bestimmt die Zeit, die dem Anfang einer Stichprobe entspricht, die einer angegebenen Zeit in einem Stream am nächsten liegt.             |
| [**AVIStreamNextKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframe)               | Sucht den nächsten Keyframe nach einer angegebenen Position in einem Stream.                                                      |
| [**AVIStreamNextKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextkeyframetime)       | Gibt die Zeit des nächsten Keyframes in einem Stream zurück, beginnend zu einem bestimmten Zeitpunkt.                                               |
| [**AVIStreamNextSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsample)                   | Sucht das nächste nichtmpty-Beispiel von einer angegebenen Position in einem Stream.                                                     |
| [**AVIStreamNextSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamnextsampletime)           | Gibt den Zeitpunkt zurück, zu dem ein Beispiel in das nächste Beispiel im Stream geändert wird.                                                    |
| [**AVIStreamPrevKeyFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframe)               | Sucht den Keyframe, der einer angegebenen Position in einem Stream vorangestellt ist.                                                       |
| [**AVIStreamPrevKeyFrameTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevkeyframetime)       | Gibt die Zeit des vorherigen Keyframes im Stream zurück, beginnend zu einem bestimmten Zeitpunkt.                                         |
| [**AVIStreamPrevSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsample)                   | Sucht das nichtmpy-Beispiel, das einer angegebenen Position in einem Stream vorausgeht.                                                 |
| [**AVIStreamPrevSampleTime**](/windows/desktop/api/Vfw/nf-vfw-avistreamprevsampletime)           | Bestimmt den Zeitpunkt, zu dem das vorherige Beispiel seinen Vorgänger im Stream ersetzt.                                    |
| [**AVIStreamSampleToSample**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletosample)           | Gibt das Beispiel in einem Stream zurück, der gleichzeitig mit einem Beispiel auftritt, das in einem zweiten Stream auftritt.                     |



 

## <a name="switching-between-samples-and-time"></a>Wechseln zwischen Stichproben und Zeit

Sie können die verstrichene Zeit vom Anfang eines Streams bis zu einem Beispiel mithilfe der [**AVIStreamSampleToTime-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreamsampletotime) ermitteln. Diese Funktion konvertiert die Stichprobennummer in einen Zeitwert in Millisekunden. Bei einem Videoframe (der mehrere Millisekunden umfasst) stellt dieser Wert die Zeit dar, zu der das Sample seit Beginn der Wiedergabe wiedergegeben wird, und geht davon aus, dass der Videoclip mit normaler Geschwindigkeit wiedergegeben wird. Bei einem Audiobeispiel (mit mehreren Samplings in einer Millisekunde) entspricht der Zeitwert der Zeit, zu der das Sample mit der Wiedergabe beginnt, und geht davon aus, dass der Audiostream mit normaler Geschwindigkeit wiedergegeben wird.

Umgekehrt können Sie die einem Zeitwert zugeordnete Beispielnummer mithilfe der [**AVIStreamTimeToSample-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreamtimetosample) ermitteln. Diese Funktion konvertiert den Millisekundenwert in eine Beispielnummer und geht davon aus, dass der Videoclip mit normaler Geschwindigkeit wiedergegeben wird.

Da **AVIStreamSampleToTime** den Zeitpunkt zurückgibt, zu dem ein Frame wiedergegeben wird, ist die Beziehung zwischen **AVIStreamSampleToTime** und **AVIStreamTimeToSample** nicht wirklich umgekehrt. Sie bestimmen die Position in einer Datei häufiger als die Zeit. Beispielsweise können zwei aufeinander folgende Audiobeispiele in derselben Millisekunde wiedergegeben werden. Die Verwendung von **AVIStreamSampleToTime** zum Konvertieren der Beispielzahlen würde zu identischen Zeitwerten führen. Wenn Sie den Zeitwert mithilfe von **AVIStreamTimeToSample** zurück in eine Beispielnummer konvertieren, wird auf ein einzelnes Beispiel verwiesen.

 

 




