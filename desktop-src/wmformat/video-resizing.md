---
title: Ändern der Größe von Videos
description: Ändern der Größe von Videos
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows Media-Format-SDK, Videogröße ändern
- Windows Media-Format-SDK, Ändern der Größe von Videos
- Advanced Systems Format (ASF), Video-Größe ändern
- ASF (Advanced Systems Format), Video-Größe ändern
- Advanced Systems Format (ASF), Ändern der Größe von Videos
- ASF (Advanced Systems Format), Ändern der Größe von Videos
- Ändern der Größe von Videos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b200496b1dead3abacfbfad7674519e0cf7ce4f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206537"
---
# <a name="video-resizing"></a>Ändern der Größe von Videos

Wenn Sie die Einstellungen für einen Videostream definieren, müssen Sie eine Breite und Höhe für die Videorahmen angeben. Diese Videogröße bestimmt die Größe der Video Frames, die im Daten Abschnitt der Datei codiert sind. Die Videogröße in einem Profil bestimmt jedoch weder die Größe des Eingabe Mediums, das Sie an den Writer übermitteln, noch die Größe des Ausgabe Mediums, das Sie vom Reader erhalten. Der Writer kann die Größe der Video Frames an die Anforderungen Ihrer Anwendung anpassen.

Die Video Bildgröße kann sich als dreistufige Vorgehensweise vorstellen: Eingabe Videogröße, streamvideo Größe und Ausgabevideo Größe.

Die Eingabe Videogröße ist die Größe der Frames, die Sie als Stichproben an das Writer-Objekt übergeben. Diese Größe wird als eine der erforderlichen Videoeingabe Eigenschaften definiert. Weitere Informationen zu Eingabe Eigenschaften finden [Sie unter Auflisten von Eingabe Formaten](to-enumerate-input-formats.md).

Stream Video size ist die Größe der Frames im Daten Abschnitt der ASF-Datei. Sie definieren diese Größe als eine der erforderlichen Datenstrom-Konfigurationseinstellungen im Profil. Wenn Sie eine Datei schreiben und die Eingabe Videogröße von der Größe des Stream-Videos abweicht, ändert der Writer die Rahmen der Codierung. Weitere Informationen zu den Eigenschaften von Videostreams finden Sie unter [Konfigurieren von Videostreams](configuring-video-streams.md).

Die Größe des Ausgabevideos ist die Größe der Frames, die vom Reader oder dem synchronen Reader bereitgestellt werden. Diese Größe wird als eine der erforderlichen Videoausgabe Eigenschaften definiert. Wenn Sie eine Datei lesen und sich die Ausgabevideo Größe von der Größe des Stream-Videos unterscheidet, ändert der Reader die Rahmen beim Decodieren.

Sie können die Größe eines streamvideos nicht auf eine ungerade Anzahl von Pixel Breite festlegen. Wenn Sie die Breite eines Videostreams auf einen ungeraden Wert festlegen, wird das Profil entweder nicht vom Writer akzeptiert, oder das resultierende Video wird mit einer schwarzen Zeile nach unten codiert, um den Unterschied zu bilden.

Beim Ändern der Größe des Videos sollten Sie sorgfältig vorgehen. Images werden bei ihrer ursprünglichen Auflösung tendenziell am besten aussehen. Das Ändern der Größe von Bildern kann häufig zu einer Verzerrung und zum Durchführen von Text führen. Wenn Sie Video auf eine niedrige Bitrate komprimieren, werden Sie auch feststellen, dass die Änderung der Größe der Größe zu schwerwiegenden Komprimierungs Artefakten führen kann.

Der Windows Media Video 9-Bildschirm Codec unterstützt das Ändern der Größe nicht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Schreiben von Dateien**](file-writing-features.md)
</dt> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> <dt>

[**Arbeiten mit Ausgaben**](working-with-outputs.md)
</dt> </dl>

 

 




