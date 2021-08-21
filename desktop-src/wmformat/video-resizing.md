---
title: Ändern der Video-Größe
description: Ändern der Video-Größe
ms.assetid: 38ecb729-68eb-4452-8389-cabe987fb8b6
keywords:
- Windows Medienformat-SDK, Ändern der Video-Größe
- Windows Medienformat-SDK, Ändern der Größe des Videos
- Advanced Systems Format (ASF), Ändern der Video-Größe
- ASF (Advanced Systems Format), Ändern der Größe von Videos
- Advanced Systems Format (ASF), Video zum Ändern der Größe
- ASF (Advanced Systems Format), Video zum Ändern der Größe
- Ändern der Video-Größe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7a3261b5b78b386a0589e2e5554b52793d478f052765cb9caa63cf7e399d90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027188"
---
# <a name="video-resizing"></a>Ändern der Video-Größe

Wenn Sie die Einstellungen für einen Videostream definieren, müssen Sie eine Breite und Höhe für die Videoframes angeben. Diese Videogröße bestimmt die Größe der Videoframes, die im Datenabschnitt der Datei codiert sind. Die Videogröße in einem Profil bestimmt jedoch nicht die Größe der Eingabemedien, die Sie an den Writer liefern, oder die Größe der Ausgabemedien, die Sie vom Reader erhalten, oder schränkt sie ein. Der Writer kann die Größe der Videoframes an die Anforderungen Ihrer Anwendung anpassen.

Die Größe des Videobilds kann als drei Phasen angenommen werden: Größe des Eingabevideos, Videogröße des Streams und Größe des Ausgabevideos.

Die Größe des Eingabevideos ist die Größe der Frames, die Sie als Beispiele an das Writer-Objekt übergeben. Sie definieren diese Größe als eine der erforderlichen Videoeingabeeigenschaften. Weitere Informationen zu Eingabeeigenschaften finden Sie unter [So enumerieren Sie Eingabeformate](to-enumerate-input-formats.md).

Die Größe des Streamvideos ist die Größe der Frames im Datenabschnitt der ASF-Datei. Sie definieren diese Größe als eine der erforderlichen Streamkonfigurationseinstellungen im Profil. Wenn Sie eine Datei schreiben und die Größe des Eingabevideos von der Größe des Streamvideos abspricht, wird die Größe der Frames beim Codieren vom Writer geändert. Weitere Informationen zu Videostreameigenschaften finden Sie unter [Configuring Video Streams](configuring-video-streams.md).

Die Größe des Ausgabevideos ist die Größe der Frames, die vom Reader oder synchronen Reader bereitgestellt werden. Sie definieren diese Größe als eine der erforderlichen Videoausgabeeigenschaften. Wenn Sie eine Datei lesen und sich die Größe des Ausgabevideos von der Größe des Streamvideos unterscheiden, wird die Größe der Frames beim Decodieren vom Reader geändert.

Sie können die Größe eines Streamvideos nicht auf eine ungerade Anzahl von Pixeln festlegen. Wenn Sie die Breite eines Videostreams auf einen ungeraden Wert festlegen, wird das Profil vom Writer entweder nicht akzeptiert, oder das resultierende Video wird mit einer schwarzen Linie nach unten um eine Seite codiert, um den Unterschied zu machen.

Gehen Sie beim Ändern der Video-Größe mit Vorsicht vor. Bilder sehen in der Regel ihre ursprüngliche Auflösung am besten aus. Das Ändern der Größe von Bildern kann häufig zu Verzerrung führen und Text unlesbar machen. Wenn Sie Videos mit einer niedrigen Bitrate komprimieren, werden Sie auch feststellen, dass größenverzerrende Komprimierungsartefakte zu schwerwiegenden Komprimierungsartefakten führen können.

Der Windows Media Video 9 Screen-Codec unterstützt keine Größenvergrößerung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Schreiben von Dateien**](file-writing-features.md)
</dt> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> <dt>

[**Arbeiten mit Ausgaben**](working-with-outputs.md)
</dt> </dl>

 

 




