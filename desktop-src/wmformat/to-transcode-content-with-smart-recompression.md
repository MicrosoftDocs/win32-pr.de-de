---
title: So transcodieren Sie Inhalte mit intelligenter Neukomprimierung
description: So transcodieren Sie Inhalte mit intelligenter Neukomprimierung
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows Media-Format-SDK, Transcodierung von Inhalten
- Windows Media-Format-SDK, intelligente Neukomprimierung
- SDK für Windows Media-Format, Neukomprimierung
- Windows Media-Format-SDK, Windows Media Audio Codecs
- Advanced Systems Format (ASF), Transcodierung von Inhalten
- ASF (Advanced Systems Format), Transcodierung von Inhalten
- Advanced Systems Format (ASF), intelligente Neukomprimierung
- ASF (Advanced Systems Format), intelligente Neukomprimierung
- Advanced Systems Format (ASF), Neukomprimierung
- ASF (Advanced Systems Format), erneute Komprimierung
- Advanced Systems Format (ASF), Windows Media Audio Codecs
- ASF (Advanced Systems Format), Windows Media Audio Codecs
- Transcodieren von Inhalten
- intelligente Neukomprimierung
- Neukomprimierung
- Windows Media Audio Codecs, Transcodierung von Inhalten
- Codecs, Windows Media Audio Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314291"
---
# <a name="to-transcode-content-with-smart-recompression"></a>So transcodieren Sie Inhalte mit intelligenter Neukomprimierung

Mithilfe des SDK für den Windows Media-Format können Sie Inhalte von einer Bitrate in eine andere transcodieren. Normalerweise besteht dies darin, den Inhalt einfach zu decodieren und erneut in die gewünschte Bitrate zu codieren. Der Windows Media Audio 9-Codec unterstützt die intelligente Neukomprimierung, die eine bessere Qualität als normale ermöglicht.

Bei der intelligenten Neukomprimierung muss der ursprüngliche Audiostream mit dem Windows Media Audio Codec codiert werden. Alle Codec-Versionen werden unterstützt, aber die spezialisierten audiovercodecs (Windows Media Audio 9 Professional und Windows Media Audio 9 Voice) nicht. Wenn die ursprüngliche Audiodatei mit dem Windows Media Audio 9-Codec ohne Verlust verwendet wurde, ist die Verwendung intelligenter Neukomprimierung nicht erforderlich, da keine Informationen in der ursprünglichen Codierung verloren gegangen sind.

Führen Sie die folgenden Schritte aus, um die intelligente Neukomprimierung zu verwenden.

1.  Richten Sie ein Reader-Objekt mit der Quelldatei zum Lesen ein. Weitere Informationen finden Sie unter [Lesen von ASF-Dateien](reading-asf-files.md).
2.  Richten Sie ein Writer-Objekt ein, das zum transcodieren der Datei verwendet werden soll. Legen Sie den Dateinamen für die neue Datei fest. Wählen Sie ein Profil aus, das für die neue Datei verwendet werden soll. Legen Sie das ausgewählte Profil im Writer-Objekt fest. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).
3.  Abrufen eines Zeigers auf die [**iwmprofile**](iwmprofile.md) -Schnittstelle des Reader-Objekts durch Aufrufen von **iwmreader:: QueryInterface**.
4.  Rufen Sie die [**iwmstreamconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) -Schnittstelle für den Audiostream ab, der durch Aufrufen von [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)transcodiert werden soll.
5.  Rufen Sie die [**iwmmediarequicenschnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) für das Datenstrom-Konfigurationsobjekt ab, indem Sie **iwmstreamconfig:: QueryInterface** aufrufen.
6.  Rufen Sie die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur für den Stream ab, indem Sie zwei Aufrufe an [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)durchführen. Abrufen der Größe der Struktur beim ersten-Befehl und Zuweisen von Arbeitsspeicher für einen Puffer, der beim zweiten-Befehl übergeben werden soll.
7.  Rufen Sie einen Zeiger auf die [**iwminputmedia-**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) Oberfläche für die Eingabe im Writer auf, indem Sie [**iwmwriter:: GetInput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)Eigenschaften aufrufen.
8.  Rufen Sie die [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle für das Eingabemedien Eigenschaften-Objekt durch Aufrufen von **iwminputmediaproperties:: QueryInterface** ab.
9.  Verwenden Sie die [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) -Methode, um die \_ Eigenschaft g wszoriginalwaveformat festzulegen. Verwenden Sie die in Schritt 6 erhaltene **WaveFormatEx** -Struktur als Wert der-Eigenschaft.
10. Schließen Sie die an den Eingabemedien Eigenschaften vorgenommenen Änderungen ein, indem Sie [**iwmwriter:: mentinputtial**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) aufrufen und einen Zeiger auf die **iwminputmediaproperties** -Schnittstelle übergeben.
11. Beginnen Sie mit dem Lesen von Beispielen aus der ursprünglichen Datei, und übergeben Sie Sie mit Aufrufen von [**iwmwriter:: Write-ample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)an den Writer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erweiterte Themen**](advanced-topics.md)
</dt> <dt>

[**Iwminputmediarequiterschnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[**Iwmmedia-Eigenschaften Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**Iwmprofile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**Iwmpropertyvault-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[**Iwmstreamconfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




