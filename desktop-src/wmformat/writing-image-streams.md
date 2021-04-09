---
title: Schreiben von bildstreams
description: Schreiben von bildstreams
ms.assetid: 3a017bdd-9723-4b7f-b5e1-22838c0ba4ff
keywords:
- Advanced Systems Format (ASF), Schreiben von bildstreams
- ASF (Advanced Systems Format), Schreiben von bildstreams
- Advanced Systems Format (ASF), bildstreams
- ASF (Advanced Systems Format), bildstreams
- bildstreams, schreiben
- Streams, Schreiben von bildstreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60daa9b62701c172d127c4cff1fb6c301edf7d86
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948436"
---
# <a name="writing-image-streams"></a>Schreiben von bildstreams

Die Eingaben für einen Bildstream müssen RGB-formatierte Bitmap-Bilder sein. Der Writer koordiniert die Komprimierung von Eingabebild Beispielen mit dem JPEG-Format. Bevor Sie mit dem Schreiben einer Datei beginnen, die einen Bildstream enthält, müssen Sie eine Bildqualität für die Eingabe mithilfe der \_ Einstellung g wszjpgcompressionquality festlegen. Verwenden Sie [**IWMWriterAdvanced2:: setinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) , um die Qualität auf einen **DWORD** -Wert im Bereich von 1 bis 100 festzulegen. Niedrige Werte stellen ein hohes Komprimierungs Verhältnis auf Kosten der Qualität dar, während hohe Werte hochwertige Bilder liefern, die mehr Platz benötigen.

Bildstreams erfordern häufig größere Puffer Fenster als normale Videostreams. Die genaue Größe hängt von der Art des Bilds und der Bildqualität ab, und zwar neben anderen Faktoren. Verwenden Sie Testversion und Fehler, um die geeignete Größe für die Abbilder zu ermitteln, die Sie verarbeiten möchten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Bildstreams**](image-streams.md)
</dt> <dt>

[**So legen Sie Eingabeeinstellungen fest**](to-set-input-settings.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




