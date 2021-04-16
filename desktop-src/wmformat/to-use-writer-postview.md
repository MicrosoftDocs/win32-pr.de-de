---
title: So verwenden Sie die Writer-Postview
description: So verwenden Sie die Writer-Postview
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Advanced Systems Format (ASF), Writer-Postview
- ASF (Advanced Systems Format), Writer-Postview
- Advanced Systems Format (ASF), nach Anzeige
- ASF (Advanced Systems Format), Post View
- Writer-Postview
- nach Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104516670"
---
# <a name="to-use-writer-postview"></a>So verwenden Sie die Writer-Postview

Das Writer-Objekt bietet Funktionen für die Post Anzeige, sodass Sie geschriebene Inhalte überprüfen können, ohne das Reader-Objekt einrichten zu müssen. Das Writer-Objekt unterstützt keine Postview für Audioinhalte.

Der Writer-postviewer funktioniert auf die gleiche Weise wie das asynchrone Reader-Objekt, nur mit weniger Features. Ausführliche Informationen zum Lesen digitaler Medien finden Sie unter [Lesen von ASF-Dateien](reading-asf-files.md).

Führen Sie die folgenden Schritte aus, um den postviewer zu implementieren.

1.  Implementieren Sie den-Rückruf [**iwmschreiterpostviewcallback:: onpostviewsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) . Diese Methode ist im Grunde mit [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) identisch, mit der Ausnahme, dass Sie streamnummern anstelle von Ausgaben angibt.
2.  Richten Sie wie gewohnt zum Schreiben ein.
3.  Abrufen eines Zeigers auf die [**iwmschreiterpostview**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) -Schnittstelle des Writer-Objekts durch Aufrufen von **iwmwriter:: QueryInterface**.
4.  Legen Sie den Rückruf für den postviewer fest, der durch Aufrufen von [**iwmschreiterpostview:: setpostviewcallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback)verwendet werden soll.
5.  Für jeden Datenstrom, für den Sie Postview-Beispiele erhalten möchten, nennen Sie [**iwmschreiterpostview:: setreceivepostviewsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples). Sie können überprüfen, ob ein Stream zum Empfangen von Postview-Beispielen festgelegt ist, indem Sie [**iwmschreiterpostview:: getreceivepostviewsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples)aufrufen.
6.  Sie können die Beispiel Formate genau wie die Ausgabeformate im Reader-Objekt oder im synchronen Reader-Objekt bearbeiten.
7.  Wenn Sie mit dem Schreiben der Datei beginnen, beginnen Sie mit dem Empfang von Beispielen in der Implementierung der **onpostviewsample** -Rückruf Methode.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmschreiterpostviewcallback-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




