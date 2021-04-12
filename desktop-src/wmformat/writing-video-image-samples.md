---
title: Schreiben von Video Bildbeispielen
description: Schreiben von Video Bildbeispielen
ms.assetid: 1d375186-230a-4a18-a995-b331c72a76e7
keywords:
- Advanced Systems Format (ASF), Schreiben von Video Bildbeispielen
- ASF (Advanced Systems Format), Schreiben von Video Bildbeispielen
- Videobilder, Schreiben von Beispielen
- Streams, Schreiben von Video Bildbeispielen
- Codecs, Schreiben von Video Bildbeispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fbac644d7938477ba3d2e8b21ebb6e631a47708
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314249"
---
# <a name="writing-video-image-samples"></a>Schreiben von Video Bildbeispielen

Ein Video Bild Datenstrom ist ein Video, das eine Reihe von Bildern enthält. Die Bilder können innerhalb des Frames verschoben werden, und jedes Bild kann in das nächste Bild integriert werden. Videobildstreams werden mit dem Windows Media Video 9-Abbild v2-Codec codiert. Das Ausgabevideo ähnelt dem, das vom Windows Media Video 9-Codec erstellt wurde.

Um ein Profil zu erstellen, das einen Video Bild Datenstrom enthält, können Sie zunächst die Video Codecs auflisten, wie unter [Informationen zum Streamen von streamkonfigurations Informationen von Codecs](getting-stream-configuration-information-from-codecs.md)beschrieben. Suchen Sie nach dem Codec, der den Untertyp "wmmediasubtype WVP2" unterstützt \_ .

Nachdem Sie das Profil für das Writer-Objekt festgelegt haben, können Sie [**iwmwriter:: getinputproperties**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops) aufrufen, um die Medien Eigenschaften für den Eingabestream des Video Bilds abzurufen. Rufen Sie den Medientyp aus dem Media Properties-Objekt ab, indem Sie [**iwmmediaproperties:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)aufrufen, und ändern Sie den Untertyp in wmmediasubtype \_ Videoimage. Legen Sie die Breite und Höhe des Videos auf die maximale Größe fest, die zum Einschließen der Bilder erforderlich ist, die Sie dem Stream hinzufügen werden. Nennen Sie anschließend [**iwmmedia-Eigenschaften:: setmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype) mit dem geänderten Eingabetyp. Nun können Sie mit dem Senden von Beispielen an das Writer-Objekt beginnen.

Jede Stichprobe muss mit einer **WMT \_ Videoimage \_ SAMPLE2** -Struktur beginnen. Außerdem enthalten Beispiele möglicherweise Bitmap-Bilder. Ein Bild wird nur an eine Stichprobe für den ersten Frame angefügt, in dem er angezeigt wird. Alle zusätzlichen Frames, die dieses Bild verwenden, benötigen nur Informationen in der Struktur. Eingabe Bitmaps müssen als RGB, 24 Bits pro Pixel formatiert werden.

Bitmapdateien speichern die Bilddaten, sodass die Daten für jede Zeile des Bilds eine Anzahl von Bytes haben, die von vier angezeigt werden. (Dies wird als Schritt der Bitmap bezeichnet.) Dadurch wird der Anfang jeder Zeile des Videos zu einer **DWORD** -Grenze erzwungen, wodurch das Kopieren effizienter wird. Wenn die Bildzeilen nicht gleichmäßig durch vier angezeigt werden, wird die Zeile mit dem nächsthöchsten Vielfachen von vier Bytes aufgefüllt. Wenn Sie Bilddaten anfügen, müssen Sie alle Auffüll Zeichen entfernen, die am Ende der Daten für jede Zeile vorhanden sind.

Der Windows Media Video 9-Abbild v2-Codec verwaltet bis zu zwei Bilder gleichzeitig im Arbeitsspeicher. Diese Images werden als Vorheriges Bild und das aktuelle Image bezeichnet. Jedes Image verfügt über eine Reihe von Membern in der **WMT \_ Videoimage \_ SAMPLE2** -Struktur, die die Darstellung des Bilds im Frame vorschreiben. Sie können ein Bild hinzufügen, indem Sie den dwcontrolflags-Member von **WMT \_ Videoimage \_ SAMPLE2** auf WMT \_ Videoimage \_ Sample \_ input \_ Frame festlegen. Wenn Sie einen Eingabe Rahmen an den Codec übergeben, wird dieses Bild zum aktuellen Bild. Das Bild, das das aktuelle Bild im vorherigen Beispiel war, wird in der Regel zum vorherigen Bild, und das Bild, das das vorherige Bild im vorherigen Beispiel war, wird verworfen. Sie können den Codec so konfigurieren, dass das alte vorherige Image beibehalten wird, indem Sie das **bkeepprevimage** -Element auf " **true**" festlegen. In diesem Fall wird das Bild, das das aktuelle Bild im vorherigen Beispiel war, verworfen.

Die grundlegende Komposition eines Video Bilds wird durch zwei Faktoren für jedes Bild bestimmt: Interessenbereich und Blend-Koeffizienten. Der relevante Bereich eines Bilds wird durch einen Ursprungs Punkt, eine Breite und eine Höhe definiert. Der Teil eines Bilds, der durch den Interessenbereich beschrieben wird, füllt den Ausgabe Rahmen aus. Wenn der relevante Bereich eine andere Größe als der Ausgabe Rahmen hat, ändert der Codec seine Größe. Der Blend-Koeffizient des Bilds bestimmt die Mischung der beiden Bilder. Die Blend-Koeffizienten für die aktuellen und vorherigen Bilder müssen insgesamt 1,0 sein. Wenn z. b. **fcurrblendcoef** auf 0,5 und **fprevblendcoef** auf 0,5 festgelegt ist, besteht der Ausgabe Frame aus einer gleichwertigen Mischung der relevanten Bereiche beider Bilder.

Wenn Sie den Interessenbereich eines Bilds verändern, können Sie schwenken und Zoom Effekte erstellen. Die Blend-Koeffizienten ermöglichen das Kreuz ausblenden (auflösen) zwischen Bildern. Zusätzlich zu diesen Auswirkungen können Sie einen der vordefinierten Übergänge verwenden, um komplexere Frames zu erstellen. Die verfügbaren Übergänge werden im Abschnitt [Video Bild Übergänge](video-image-transitions.md) in dieser Dokumentation beschrieben. Wenn Sie einen Übergang verwenden, müssen Sie jeden Frame konfigurieren. Die einfachste Möglichkeit hierfür ist, eine Funktion zu erstellen, die Elemente der **WMT \_ Videoimage \_ SAMPLE2** -Struktur inkrementell ändert, um einen vollen Effekt zu erzielen.

Weitere Informationen zu den Werten, die für Deformationen festgelegt werden sollen, finden Sie unter [**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2).

**Hinweis** Wenn Sie Audiodaten in eine Datei mit einem Video Bild Datenstrom einschließen möchten, müssen Sie unkomprimierte Audioeingaben verwenden. Um einen videobildstream mit einem vorhandenen komprimierten Audiostream zu kombinieren, müssen Sie die Audiodatei Dekomprimieren und die Beispiele in unkomprimierter Form übergeben. Wenn Sie beim Schreiben eines videobildstreams komprimierte Beispiele an den Writer übergeben, tritt ein Fehler auf, der dazu führt, dass Beispiele aus dem Video gelöscht werden.

Außerdem können komprimierte Video Bilddateien ohne Audiodatenströme mehrere sehr kleine, stark komprimierte Video Frames in einem einzelnen ASF-Paket enthalten. Dies kann zu einem schlechten Wiedergabe Erlebnis in früheren Versionen von Windows Media Player führen. Um dieses Problem zu vermeiden, besteht die beste Lösung darin, einen automatischen Audiostream in die Datei einzufügen, obwohl dadurch auch die Dateigröße erhöht wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Videobild**](video-image.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




