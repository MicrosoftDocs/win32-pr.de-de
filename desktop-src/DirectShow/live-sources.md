---
description: Livequellen
ms.assetid: 571fe5e5-9616-463b-837c-f8dbb8adf1be
title: Livequellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8872cc5489ae61f3b7b9629e97303ad033630346094f8f1faa013f5da81d9142
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153198"
---
# <a name="live-sources"></a>Livequellen

Eine Livequelle, auch push *source* genannt, empfängt Daten in Echtzeit. Beispiele hierfür sind Videoaufnahmen und Netzwerkübertragungen. Im Allgemeinen kann eine Livequelle nicht steuern, mit welcher Rate Daten eintreffen.

Ein Filter wird als Livequelle betrachtet, wenn einer der folgenden Punkte zutrifft:

-   Der Filter gibt das \_ AM FILTER \_ MISC \_ FLAGS IS \_ \_ SOURCE-Flag von der [**IAMFilterMiscFlags::GetMiscFlags-Methode**](/windows/desktop/api/Strmif/nf-strmif-iamfiltermiscflags-getmiscflags) zurück, und mindestens einer seiner Ausgabepins macht die [**IAMPushSource-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) verfügbar.
-   Der Filter macht die [**IKsPropertySet-Schnittstelle**](ikspropertyset.md) verfügbar und verfügt über einen Erfassungspin (PIN \_ CATEGORY \_ CAPTURE). Weitere Informationen finden Sie unter [Anheften](pin-property-set.md) von Eigenschaften.

Wenn ein Livequellfilter eine Uhr bereitstellt, bevorzugt der Filter Graph Manager diese Uhr, wenn er die Graphverweisuhr ausgibt. Weitere Informationen finden Sie unter [Referenzuhren.](reference-clocks.md)

**Latenz**

Die Latenz eines Filters ist die Zeitspanne, die der Filter benötigt, um ein Beispiel zu verarbeiten. Bei Livequellen wird die Latenz durch die Größe des Puffers bestimmt, der zum Speichern von Stichproben verwendet wird. Angenommen, das Filterdiagramm verfügt über eine Videoquelle mit einer Latenz von 33 Millisekunden (ms) und eine Audioquelle mit einer Latenz von 500 ms. Jeder Videoframe erreicht den Videorenderer etwa 470 ms, bevor das entsprechende Audiobeispiel den Audiorenderer erreicht. Sofern der Unterschied nicht durch das Diagramm kompensiert wird, werden audio und video nicht synchronisiert.

Livequellen können über die [**IAMPushSource-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) synchronisiert werden. Der Filter Graph Manager synchronisiert keine Livequellen, es sei denn, die Anwendung aktiviert die Synchronisierung durch Aufrufen der [**IAMGraphStreams::SyncUsingStreamOffset-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iamgraphstreams-syncusingstreamoffset) Wenn die Synchronisierung aktiviert ist, fragt der Filter Graph Manager jeden Quellfilter nach **IAMPushSource** ab. Wenn der Filter **IAMPushSource** unterstützt, ruft der Filter Graph Manager [**IAMLatency::GetLatency**](/windows/desktop/api/Strmif/nf-strmif-iamlatency-getlatency) auf, um die erwartete Latenz des Filters abzurufen. (Die **IAMPushSource-Schnittstelle** erbt [**IAMLatency**](/windows/desktop/api/Strmif/nn-strmif-iamlatency).) Anhand der kombinierten Latenzwerte bestimmt der Filter Graph Manager die maximale erwartete Latenz im Diagramm. Anschließend ruft sie [**IAMPushSource::SetStreamOffset**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-setstreamoffset) auf, um jedem Quellfilter einen Streamoffset zuzuweisen, den dieser Filter den von ihm generierten Zeitstempeln hinzufügt.

Diese Methode ist in erster Linie für die Livevorschau vorgesehen. Beachten Sie jedoch, dass ein Vorschaustecker auf einem Liveaufnahmegerät (z. B. einer Kamera) keine Zeitstempel für die von ihm übermittelten Stichproben angibt. Um diese Methode mit einem Liveerfassungsgerät verwenden zu können, müssen Sie daher über den Erfassungspin eine Vorschau anzeigen. Weitere Informationen finden Sie unter [DirectShow Video Capture Filters](directshow-video-capture-filters.md).

Derzeit wird die [**IAMPushSource-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) vom [VFW Capture-Filter](vfw-capture-filter.md) und dem [Audio Capture-Filter](audio-capture-filter.md) unterstützt.

**Ratenübereinstimmung**

Wenn ein Rendererfilter Stichproben mit einer Verweisuhr plant, der Quellfilter sie jedoch mit einer anderen Uhr erzeugt, können bei der Wiedergabe Störungen auftreten. Der Renderer kann schneller als die Quelle ausgeführt werden, wodurch Lücken in den Daten entstehen. Oder es kann langsamer als die Quelle ausgeführt werden, was dazu führt, dass die Stichproben "zusammengehäuft" werden, bis das Diagramm zu einem bestimmten Zeitpunkt stichprobenweise abfällt. In der Regel kann eine Livequelle ihre Produktionsrate nicht steuern, sodass der Renderer stattdessen die Raten mit der Quelle abgleichen sollte.

Derzeit führt nur der Audiorenderer einen Ratenabgleich durch, da Störungen bei der Audiowiedergabe deutlicher sind als Störungen im Video. Um eine Ratenübereinstimmung durchzuführen, muss der Audiorenderer etwas auswählen, mit dem die Raten übereinstimmen. Dabei wird der folgende Algorithmus verwendet:

-   Wenn das Diagramm keine Referenzuhr verwendet, versucht der Audiorenderer nicht, die Raten abzugleichen. (Wenn das Diagramm über keine Referenzuhr verfügt, werden Stichproben immer sofort gerendert, sobald sie eintreffen.)
-   Andernfalls überprüft der Audiorenderer bei Verwendung einer Referenzuhr für den Graphen anhand der zuvor beschriebenen Kriterien, ob ein Livequell-Upstream vorhanden ist. Falls nicht, stimmt der Audiorenderer nicht mit den Raten überein.
-   Wenn eine Livequelle upstream vorhanden ist und diese Quelle die [**IAMPushSource-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) auf dem Ausgabepin verfügbar macht, ruft der Audiorenderer [**IAMPushSource::GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags)auf. Es sucht nach einem der folgenden Flags:
    -   AM \_ \_ INTERNEN \_ PUSHSOURCECAPS-RM. Dieses Flag bedeutet, dass der Quellfilter über einen eigenen Ratenübereinstimmungsmechanismus verfügt, sodass der Audiorenderer nicht mit Raten übereinstimmt.
    -   AM \_ PUSHSOURCECAPS \_ NICHT \_ LIVE. Dieses Flag bedeutet, dass der Quellfilter nicht wirklich eine Livequelle ist, obwohl er die [**IAMPushSource-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iampushsource) verfügbar macht. Daher stimmt der Audiorenderer nicht mit raten überein.
    -   AM \_ PRIVATEN PUSHSOURCECAPS-UHR. \_ \_ Dieses Flag bedeutet, dass der Quellfilter eine private Uhr verwendet, um Zeitstempel zu generieren. In diesem Fall gleicht der Audiorenderer die Raten mit den Zeitstempeln ab. (Wenn die Beispiele jedoch keine Zeitstempel aufweisen, ignoriert der Renderer dieses Flag.)
-   Wenn [**GetPushSourceFlags**](/windows/desktop/api/Strmif/nf-strmif-iampushsource-getpushsourceflags) keine Flags (null) zurückgibt, hängt das Verhalten des Audiorenderers von der Graphuhr und davon ab, ob die Stichproben Zeitstempel aufweisen:
    -   Wenn der Audiorenderer nicht die Graphuhr ist und die Beispiele Zeitstempel aufweisen, gleicht der Audiorenderer die Raten mit den Zeitstempeln ab.
    -   Wenn die Beispiele keine Zeitstempel aufweisen, versucht der Audiorenderer, die Rate der eingehenden Audiodaten abzugleichen.
    -   Wenn der Audiorenderer die Graphuhr ist, versucht er, die eingehende Datenrate abzugleichen.

Der Grund für den letzten Fall ist der folgende: Wenn der Audiorenderer die Referenzuhr ist und der Quellfilter die gleiche Uhr verwendet, um Zeitstempel zu generieren, kann der Audiorenderer keine Raten mit den Zeitstempeln abgleichen. In diesem Falle würde er versuchen, die Raten mit sich selbst abzugleichen, was dazu führen könnte, dass die Uhr abdriftet. Daher stimmt der Renderer in diesem Fall mit der Rate der eingehenden Audiodaten überein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



