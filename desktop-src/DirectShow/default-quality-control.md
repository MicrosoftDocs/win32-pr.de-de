---
description: Standardqualitätssteuerung
ms.assetid: 91c4b8cf-3d24-4a11-b19c-b0297734e52b
title: Standardqualitätssteuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9df737855376db52a35476c0f01da4b850e3678ec20595ee82720b7b928237ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953133"
---
# <a name="default-quality-control"></a>Standardqualitätssteuerung

Die [DirectShow-Basisklassen](directshow-base-classes.md) implementieren einige Standardverhalten für die Videoqualitätssteuerung.

Qualitätsmeldungen beginnen beim Renderer. Die Basisklasse für Videorenderer ist [**CBaseVideoRenderer**](cbasevideorenderer.md)mit folgendem Verhalten:

1.  Wenn der Videorenderer ein Beispiel empfängt, vergleicht er den Zeitstempel des Beispiels mit der aktuellen Referenzzeit.
2.  Der Videorenderer generiert eine Qualitätsmeldung. In der Basisklasse ist das **Proportion-Member** der Qualitätsnachricht auf einen Bereich von 500 (50 %) bis 2000 (200 %) beschränkt. Werte außerhalb dieses Bereichs können zu plötzlichen Qualitätsänderungen führen.
3.  Standardmäßig sendet der Videorenderer die Qualitätsnachricht an den Upstreamausgabepin (der Pin ist mit seinem Eingabepin verbunden). Anwendungen können dieses Verhalten überschreiben, indem sie die **SetSink-Methode** aufrufen.

Was als Nächstes geschieht, hängt vom Upstreamfilter ab. In der Regel ist dies ein Transformationsfilter. Die Basisklasse für Transformationsfilter ist [**CTransformFilter,**](ctransformfilter.md)die die [**Klassen CTransformInputPin**](ctransforminputpin.md) und [**CTransformOutputPin**](ctransformoutputpin.md) verwendet, um Eingabe- und Ausgabepins zu implementieren. Zusammen haben diese Klassen das folgende Verhalten:

1.  Die [**CTransformOutputPin::Notify-Methode**](ctransformoutputpin-notify.md) ruft [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md)auf, eine private Methode für die Filterbasisklasse.
2.  Abgeleitete Filter können **AlterQuality überschreiben,** um die Qualitätsmeldung zu verarbeiten. Standardmäßig ignoriert **AlterQuality** die Qualitätsmeldung.
3.  Wenn **AlterQuality die** Qualitätsnachricht nicht verarbeitet, ruft der Ausgabepin [**CBaseInputPin::P assNotify**](cbaseinputpin-passnotify.md)auf, eine private Methode auf dem Eingabepin des Filters.
4.  **PassNotify übergibt** die Qualitätsmeldung an den entsprechenden Ort – den nächsten Upstreamausgabepin oder einen benutzerdefinierten Qualitäts-Manager.

Wenn kein Transformationsfilter die Qualitätsmeldung verarbeitet, erreicht die Nachricht schließlich den Ausgabepin des Quellfilters. In den Basisklassen gibt [**CBasePin::Notify**](cbasepin-notify.md) E \_ NOTIMPL zurück. Wie ein bestimmter Quellfilter Qualitätsnachrichten verarbeitet, hängt von der Art der Quelle ab. Einige Quellen, z. B. Livevideoaufnahmen, können keine sinnvolle Qualitätskontrolle durchführen. Andere Quellen können die Rate anpassen, mit der sie Stichproben liefern.

Das folgende Diagramm veranschaulicht das Standardverhalten.

![Qualitätskontrolle in den Basisklassen](images/quality-control.png)

Der Basisvideorenderer implementiert **IQualityControl::Notify.** Dies bedeutet, dass Sie Qualitätsmeldungen an den Renderer selbst übergeben können. Wenn Sie das **Proportion-Member** auf einen Wert kleiner als 1000 festlegen, fügt der Videorenderer eine Wartezeit zwischen jedem gerenderten Frame ein, was den Renderer verlangsamt. (Sie können dies beispielsweise tun, um die Systemauslastung zu reduzieren.) Weitere Informationen finden Sie unter [**CBaseVideoRenderer::ThrottleWait**](cbasevideorenderer-throttlewait.md). Das Festlegen **des Proportion-Mitglieds** auf einen Wert größer als 1000 hat keine Auswirkungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Qualitätskontrollverwaltung](quality-control-management.md)
</dt> </dl>

 

 



