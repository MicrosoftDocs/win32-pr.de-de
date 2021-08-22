---
title: Schreiben von Videobildbeispielen
description: Schreiben von Videobildbeispielen
ms.assetid: 1d375186-230a-4a18-a995-b331c72a76e7
keywords:
- Advanced Systems Format (ASF), Schreiben von Videobildbeispielen
- ASF (Advanced Systems Format), Schreiben von Videobildbeispielen
- Videobilder, Schreiben von Beispielen
- Streams,Schreiben von Videobildbeispielen
- Codecs, Schreiben von Videobildbeispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c05bbcc9239eede97f4ea7ca0df34004b1fb7facc0c36c8f38098c42e86fce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704820"
---
# <a name="writing-video-image-samples"></a>Schreiben von Videobildbeispielen

Ein Videobildstream ist ein Video, das eine Reihe von Standbildern enthält. Die Bilder können innerhalb des Rahmens verschoben werden, und jedes Bild kann sich in das nächste einfügen. Videobildstreams werden mit dem codec Windows Media Video 9 Image v2 codiert. Das Ausgabevideo ähnelt dem, das vom Windows Media Video 9-Codec erstellt wurde.

Um ein Profil zu erstellen, das einen Videobildstream enthält, beginnen Sie mit dem Auflisten der Videocodecs, wie unter [Abrufen von Streamkonfigurationsinformationen von Codecs](getting-stream-configuration-information-from-codecs.md)beschrieben. Suchen Sie nach dem Codec, der den WVP2-Untertyp WMMEDIASUBTYPE \_ unterstützt.

Nachdem Sie das Profil für das Writer-Objekt festgelegt haben, rufen Sie [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops) auf, um die Medieneigenschaften für den Videobild-Eingabestream abzurufen. Rufen Sie den Medientyp aus dem Medieneigenschaftenobjekt ab, indem [**Sie IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)aufrufen, und ändern Sie den Untertyp in WMMEDIASUBTYPE \_ VIDEOIMAGE. Sie sollten die Videobreite und -höhe auf die maximalen Abmessungen festlegen, die für die Bilder erforderlich sind, die Sie dem Stream hinzufügen. Rufen Sie dann [**IWMMediaProps::SetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype) mit dem geänderten Eingabetyp auf. Nun können Sie mit dem Senden von Beispielen an das Writer-Objekt beginnen.

Jedes Beispiel muss mit einer **WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur** beginnen. Darüber hinaus können Beispiele Bitmapbilder enthalten. Ein Bild ist nur an ein Beispiel für den ersten Frame angefügt, in dem es angezeigt wird. Alle zusätzlichen Frames, die dieses Bild verwenden, benötigen nur Informationen in der -Struktur. Eingabebitmaps müssen als RGB formatiert werden, 24 Bits pro Pixel.

Bitmapdateien speichern die Bilddaten, sodass die Daten für jede Zeile des Bilds eine Anzahl von Bytes enthalten, die durch vier teilbar sind. (Dies wird als Schritt der Bitmap bezeichnet.) Dadurch wird der Anfang jeder Videozeile zu einer **DWORD-Grenze** gezwungen, wodurch das Kopieren effizienter wird. Wenn die Bildzeilen nicht gleichmäßig durch vier teilbar sind, wird die Zeile auf das nächst höchster Vielfache von vier Bytes aufgefüllt. Wenn Sie Bilddaten anfügen, müssen Sie alle Auffüllungen entfernen, die am Ende der Daten für jede Zeile vorhanden sind.

Der Codec Windows Media Video 9 Image v2 behält bis zu zwei Bilder gleichzeitig im Arbeitsspeicher bei. Diese Bilder werden als vorheriges Und aktuelles Bild bezeichnet. Jedes Bild verfügt über einen Satz von Membern in der **WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur,** die vorgeben, wie das Bild im Rahmen dargestellt wird. Sie können ein Bild hinzufügen, indem Sie den dwControlFlags-Member von **WMT \_ VIDEOIMAGE \_ SAMPLE2** auf WMT \_ VIDEOIMAGE \_ SAMPLE INPUT FRAME \_ \_ festlegen. Wenn Sie einen Eingaberahmen an den Codec übergeben, wird dieses Bild zum aktuellen Bild. Das Bild, das das aktuelle Bild im vorherigen Beispiel war, wird in der Regel zum vorherigen Bild, und das Bild, das das vorherige Bild im vorherigen Beispiel war, wird verworfen. Sie können den Codec so konfigurieren, dass das alte vorherige Bild beibehalten wird, indem Sie den **Member bKeepPrevImage** auf **TRUE** festlegen. In diesem Fall wird das Image, das das aktuelle Image im vorherigen Beispiel war, verworfen.

Die grundlegende Zusammensetzung eines Videobildrahmens wird durch zwei Faktoren für jedes Bild bestimmt: bereich of interest und blend coefficient. Der für ein Bild interessante Bereich wird durch einen Ursprungspunkt, eine Breite und eine Höhe definiert. Der Teil eines Bilds, der durch den interessanten Bereich beschrieben wird, füllt den Ausgaberahmen. Wenn der interessante Bereich eine andere Größe als der Ausgaberahmen hat, wird die Größe des Codecs geändert. Der Mischungskoeffizient des Bilds bestimmt die Mischung der beiden Bilder. Die Blendkoeffizienten für die aktuellen und vorherigen Bilder müssen insgesamt 1,0 betragen. Wenn **fCurrBlendCoef** beispielsweise auf 0,5 und **fPrevBlendCoef** auf 0,5 festgelegt ist, besteht der Ausgaberahmen aus einer gleichen Mischung aus den interessanten Bereichen beider Bilder.

Durch Bearbeiten des gewünschten Bereichs für ein Bild können Sie Schwenk- und Zoomeffekte erstellen. Die Mischungskoeffizienten ermöglichen es Ihnen, zwischen Bildern zu überblenden (zu überblenden). Zusätzlich zu diesen Effekten können Sie einen der vordefinierten Übergänge verwenden, um komplexere Frames zu erstellen. Die verfügbaren Übergänge werden im Abschnitt [Videobildübergänge](video-image-transitions.md) dieser Dokumentation beschrieben. Wenn Sie einen Übergang verwenden, müssen Sie jeden Frame konfigurieren. Die einfachste Möglichkeit besteht darin, eine Funktion zu erstellen, die Elemente der **WMT \_ VIDEOIMAGE \_ SAMPLE2-Struktur** inkrementell ändert, um einen vollständigen Effekt zu erzielen.

Weitere Informationen zu den Werten, die für Dies festgelegt werden sollen, finden Sie unter [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2).

**Hinweis** Wenn Sie Audiodaten in eine Datei mit einem Videobildstream einschließen möchten, müssen Sie unkomprimierte Audioeingaben verwenden. Um einen Videobildstream mit einem vorhandenen komprimierten Audiostream zu kombinieren, müssen Sie die Audiodaten dekomprimieren und die Beispiele unkomprimiert übergeben. Wenn Sie beim Schreiben eines Videobildstreams komprimierte Beispiele an den Writer übergeben, tritt ein Fehler auf, der dazu führt, dass Beispiele aus dem Video gelöscht werden.

Außerdem können komprimierte Videobilddateien ohne Audiostreams mehrere sehr kleine, stark komprimierte Videoframes in einem einzelnen ASF-Paket enthalten, was zu einer schlechten Wiedergabeerfahrung bei früheren Versionen von Windows Media Player führen kann. Um dieses Problem zu vermeiden, besteht die beste Lösung darin, einen automatischen Audiodatenstrom in die Datei einzufügen, obwohl dadurch auch die Dateigröße erhöht wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Videobild**](video-image.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




