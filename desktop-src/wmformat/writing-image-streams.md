---
title: Schreiben von Streams
description: Schreiben von Streams
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- Advanced Systems Format (ASF), Schreiben von Bildstreams
- ASF (Advanced Systems Format), Schreiben von Bildstreams
- Advanced Systems Format (ASF), Imagestreams
- ASF (Advanced Systems Format), Imagestreams
- Bildstreams,Schreiben
- Streams,Schreiben von Bildstreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6061af2ff43cbeb3fe688b6533eee044036df029bdb7f7305af305c8d45084
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006300"
---
# <a name="writing-image-streams"></a>Schreiben von Streams

Die Eingaben für einen Bildstream müssen RGB-formatierte Bitmapbilder sein. Der Writer koordiniert die Komprimierung von Eingabebildbeispielen im JPEG-Format. Bevor Sie mit dem Schreiben einer Datei beginnen, die einen Bildstream enthält, müssen Sie mithilfe der Einstellung g \_ wszJPEGCompressionQuality eine Bildqualität für die Eingabe festlegen. Verwenden Sie [**IWMWriterAdvanced2::SetInputSetting,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) um die Qualität auf einen **DWORD-Wert** im Bereich von 1 bis 100 festzulegen. Niedrige Werte stellen ein hohes Komprimierungsverhältnis auf Kosten der Qualität dar, während hohe Werte qualitativ hochwertige Bilder erzeugen, die mehr Platz erfordern.

Bildstreams erfordern häufig größere Pufferfenster als normale Videostreams. Die genaue erforderliche Größe hängt unter anderem von der Art des Bilds und der Imagequalität ab. Verwenden Sie Testversion und Fehler, um die geeignete Größe für die Bilder zu bestimmen, die Sie verarbeiten möchten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Image Streams**](image-streams.md)
</dt> <dt>

[**So legen Sie eingabe Einstellungen fest**](to-set-input-settings.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




