---
description: In diesem Thema wird beschrieben, wie ein benutzerdefinierter DirectShow-Erfassungsfilter Ausgabedaten generieren soll.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Erstellen von Daten in einem Erfassungsfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbc604c94953239b8be70ced28c9c0d6cf43eefa308c9d624db9a33d62152ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748180"
---
# <a name="producing-data-in-a-capture-filter"></a>Erstellen von Daten in einem Erfassungsfilter

In diesem Thema wird beschrieben, wie ein benutzerdefinierter DirectShow-Erfassungsfilter Ausgabedaten generieren soll.

## <a name="filter-state-changes"></a>Ändern des Filterzustands

Ein Erfassungsfilter sollte nur dann Daten erzeugen, wenn der Filter ausgeführt wird. Senden Sie keine Daten von Ihren Pins, wenn der Filter angehalten wird. Geben Sie **außerdem VFW \_ S \_ CANT \_ CUE** von der [**CBaseFilter::GetState-Methode**](cbasefilter-getstate.md) zurück, wenn der Filter angehalten wird. Dieser Rückgabewert informiert den Filter Graph Manager darüber, dass er nicht auf Daten aus dem Filter warten soll, während der Filter angehalten wird. Weitere Informationen finden Sie unter [Filtern von Zuständen.](filter-states.md)

Der folgende Code zeigt, wie die [**IMediaFilter::GetState-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) implementiert wird:


```C++
CMyVidcapFilter::GetState(DWORD dw, FILTER_STATE *pState)
{
    CheckPointer(pState, E_POINTER);
    *pState = m_State;
    if (m_State == State_Paused)
    {
        return VFW_S_CANT_CUE;
    }
    else
    {
        return S_OK;
    }
}
```



## <a name="controlling-individual-streams"></a>Steuern einzelner Streams

Die Ausgabepins eines Erfassungsfilters sollten die [**IAMStreamControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) unterstützen, damit eine Anwendung jeden Pin einzeln aktivieren oder deaktivieren kann. Beispielsweise kann eine Anwendung eine Vorschau ohne Erfassung anzeigen und dann in den Erfassungsmodus wechseln, ohne das Filterdiagramm neu zu erstellen. Sie können die [**CBaseStreamControl-Klasse**](cbasestreamcontrol.md) verwenden, um diese Schnittstelle zu implementieren.

## <a name="time-stamps"></a>Zeitstempel

Wenn der Filter eine Stichprobe erfasst, wird der Zeitstempel des Beispiels mit der aktuellen Streamzeit versehen. Die Endzeit ist die Startzeit plus die Dauer. Wenn der Filter beispielsweise zehn Stichproben pro Sekunde erfasst und die Streamzeit 200.000.000 Einheiten beträgt, wenn der Filter die Stichprobe erfasst, sollten die Zeitstempel 200000000 und 2010000000 sein. (Es gibt 10.000.000 Einheiten pro Sekunde.)

Rufen Sie zum Berechnen der Streamzeit die [**IReferenceClock::GetTime-Methode**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) auf, um die aktuelle Verweiszeit abzurufen, und subtrahieren Sie dann die ursprüngliche Startzeit. Alternativ können Sie die [**CBaseFilter::StreamTime-Methode**](cbasefilter-streamtime.md) aufrufen, die dieselbe Berechnung ausführt. Um den Zeitstempel für ein Beispiel festzulegen, rufen Sie die [**IMediaSample::SetTime-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) auf.

Wenn der Filter jedoch über einen Vorschaupin verfügt, sollten die Beispiele aus dem Vorschaupin keine Zeitstempel aufweisen. Der Grund dafür ist, dass Stichproben den Renderer nach dem Zeitpunkt der Erfassung immer leicht erreichen. Wenn die Stichproben mit einem Zeitstempel versehen sind, behandelt der Renderer sie als spät und versucht möglicherweise, den Rückstand durch Verwerfen von Stichproben aufzuholen. (Weitere Informationen finden Sie unter [DirectShow Video Capture Filters](directshow-video-capture-filters.md).) Beachten Sie, dass die [**IAMStreamControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) die Stecknadel benötigt, um die Beispielzeiten nachzuverfolgen. Für einen Vorschaupin müssen Sie möglicherweise die Implementierung ändern, sodass sie nicht auf Zeitstempeln angewiesen ist.

Zeitstempel müssen sich immer von einer Stichprobe zur nächsten erhöhen. Dies gilt auch, wenn der Filter angehalten wird. Wenn der Filter ausgeführt, angehalten und dann erneut ausgeführt wird, muss das erste Beispiel nach der Pause einen größeren Zeitstempel aufweisen als das letzte Beispiel vor der Pause.

Abhängig von den erfassten Daten kann es sinnvoll sein, die Medienzeit für die Stichproben festzulegen.

Weitere Informationen finden Sie unter [Uhrzeit und Uhren in DirectShow.](time-and-clocks-in-directshow.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Videoaufnahmefilter](directshow-video-capture-filters.md)
</dt> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Schreiben von Erfassungsfiltern](writing-capture-filters.md)
</dt> </dl>

 

 



