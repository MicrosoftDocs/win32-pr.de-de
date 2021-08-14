---
title: So verwenden Sie writer postview
description: So verwenden Sie writer postview
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Advanced Systems Format (ASF), Writer-Postview
- ASF (Advanced Systems Format), Writer-Postview
- Advanced Systems Format (ASF), Postviewing
- ASF (Advanced Systems Format), Postviewing
- Writer-Postview
- Postviewing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7800f3ba50f9f1d61793a0d2ada2db0c03d6b88551ac1147e17872aa8e428c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118196404"
---
# <a name="to-use-writer-postview"></a>So verwenden Sie writer postview

Das Writer-Objekt bietet Postviewingfunktionen, sodass Sie geschriebene Inhalte überprüfen können, ohne das Readerobjekt einrichten zu müssen. Das Writer-Objekt unterstützt keine Postviewing für Audioinhalte.

Der Writer-Postviewer funktioniert auf die gleiche Weise wie das asynchrone Readerobjekt, nur mit weniger Features. Ausführliche Informationen zum Lesen digitaler Medien finden Sie unter [Lesen von ASF-Dateien.](reading-asf-files.md)

Führen Sie die folgenden Schritte aus, um den Postviewer zu implementieren.

1.  Implementieren Sie [**den IWMWriterPostViewCallback::OnPostViewSample-Rückruf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) Diese Methode ist im Wesentlichen identisch mit [**IWMReaderCallback::OnSample,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) außer dass sie Datenstromnummern anstelle von Ausgaben angibt.
2.  Richten Sie wie gewohnt für das Schreiben ein.
3.  Rufen Sie einen Zeiger auf die [**IWMWriterPostView-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) des Writerobjekts ab, indem **Sie IWMWriter::QueryInterface aufrufen.**
4.  Legen Sie den Rückruf für die Verwendung durch den Postviewer fest, indem [**Sie IWMWriterPostView::SetPostViewCallback aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback)
5.  Rufen Sie für jeden Stream, für den Sie Postview-Beispiele erhalten möchten, [**IWMWriterPostView::SetReceivePostViewSamples auf.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples) Sie können überprüfen, ob ein Stream für den Empfang von Postview-Beispielen festgelegt ist, indem Sie [**IWMWriterPostView::GetReceivePostViewSamples aufrufen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples)
6.  Sie können die Beispielformate genau wie die Ausgabeformate im Readerobjekt oder synchronen Readerobjekt bearbeiten.
7.  Wenn Sie mit dem Schreiben der Datei beginnen, erhalten Sie Beispiele in Ihrer Implementierung der **OnPostViewSample-Rückrufmethode.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMWriterPostViewCallback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




