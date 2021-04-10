---
description: Standardmäßige Qualitätskontrolle
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: Standardmäßige Qualitätskontrolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 864cd187df71c56441edcfd00fcd6785d96afe84
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041125"
---
# <a name="default-quality-control"></a>Standardmäßige Qualitätskontrolle

Die [DirectShow-Basisklassen](directshow-base-classes.md) implementieren einige Standardverhalten für die Video Qualitäts Steuerung.

Qualitäts Meldungen beginnen beim Renderer. Die Basisklasse für Videorenderer ist [**cbasevideorenderer**](cbasevideorenderer.md), die folgendes Verhalten aufweist:

1.  Wenn der Videorenderer ein Beispiel erhält, vergleicht es den Zeitstempel des Beispiels mit der aktuellen Verweis Zeit.
2.  Der Videorenderer generiert eine Qualitäts Meldung. In der Basisklasse ist der **Anteils** Wert der Qualitäts Nachricht auf einen Bereich von 500 (50%) beschränkt. auf 2000 (200%). Werte außerhalb dieses Bereichs können zu abrupten Qualitätsänderungen führen.
3.  Standardmäßig sendet der Videorenderer die Qualitäts Meldung an die upstreamausgabepin (die PIN, die mit der eingabepin verbunden ist). Anwendungen können dieses Verhalten überschreiben, indem Sie die **setsink** -Methode aufrufen.

Was als nächstes passiert, hängt vom upstreamfilter ab. In der Regel handelt es sich hierbei um einen Transformations Filter. Die Basisklasse für Transformations Filter ist [**ctransformfilter**](ctransformfilter.md), bei dem die Klassen [**ctransforminputpin**](ctransforminputpin.md) und [**ctransformoutputpin**](ctransformoutputpin.md) zum Implementieren von Eingabe-und Ausgabe Pins verwendet werden. Diese Klassen haben das folgende Verhalten:

1.  Die [**ctransformoutputpin:: notify**](ctransformoutputpin-notify.md) -Methode ruft [**ctransformfilter:: alterquality**](ctransformfilter-alterquality.md)auf, eine private Methode für die Filter Basisklasse.
2.  Abgeleitete Filter können **alterquality** überschreiben, um die Qualitäts Meldung zu verarbeiten. Standardmäßig ignoriert **alterquality** die Qualitäts Meldung.
3.  Wenn **alterquality** die Qualitäts Meldung nicht verarbeitet, ruft die Ausgabe-PIN [**cbaseinputpin::P assnotify**](cbaseinputpin-passnotify.md)auf, eine private Methode für die Eingabe-PIN des Filters.
4.  **Passnotify** übergibt die Qualitäts Nachricht an die entsprechende Stelle – die nächste upstreamausgabepin oder ein benutzerdefinierter Quality Manager.

Vorausgesetzt, dass kein Transformations Filter die Qualitäts Meldung behandelt, erreicht die Nachricht schließlich die Ausgabe-PIN für den Quell Filter. In den Basisklassen gibt [**cbasepin:: notify**](cbasepin-notify.md) E \_ notimpl zurück. Die Art und Weise, in der ein bestimmter Quell Filter Qualitäts Meldungen verarbeitet, hängt von der Art der Quelle ab. Einige Quellen, z. b. die Live Video Erfassung, können keine sinnvolle Qualitätskontrolle ausführen. Andere Quellen können die Rate anpassen, mit der Sie Stichproben bereitstellen.

Das folgende Diagramm veranschaulicht das Standardverhalten.

![Qualitätskontrolle in den Basisklassen](images/quality-control.png)

Der basisvideorenderer implementiert **iqualitycontrol:: notify**. Dies bedeutet, dass Sie Qualitäts Meldungen an den Renderer selbst übergeben können. Wenn Sie für das **proportional** Element einen Wert kleiner als 1000 festlegen, fügt der Videorenderer eine Wartezeit zwischen den einzelnen Frames ein, die er rendert, wodurch der Renderer verlangsamt wird. (Beispielsweise können Sie dies tun, um die System Auslastung zu reduzieren.) Weitere Informationen finden Sie unter [**cbasevideorenderer:: throttlewait**](cbasevideorenderer-throttlewait.md). Das Festlegen des **proportionalmembers** auf einen Wert größer als 1000 hat keine Auswirkungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Qualitäts Steuerungs Verwaltung](quality-control-management.md)
</dt> </dl>

 

 



