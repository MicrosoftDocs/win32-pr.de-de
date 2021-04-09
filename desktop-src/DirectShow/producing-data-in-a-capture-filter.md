---
description: In diesem Thema wird beschrieben, wie ein benutzerdefinierter DirectShow-Erfassungs Filter Ausgabedaten generieren soll.
ms.assetid: e407e9ed-f1f7-43c4-a048-c27476c910ea
title: Erstellen von Daten in einem Erfassungs Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9c9e5bed6fc7e01aa89bf6f495c1bbdf6e42a0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957969"
---
# <a name="producing-data-in-a-capture-filter"></a>Erstellen von Daten in einem Erfassungs Filter

In diesem Thema wird beschrieben, wie ein benutzerdefinierter DirectShow-Erfassungs Filter Ausgabedaten generieren soll.

## <a name="filter-state-changes"></a>Filter Zustandsänderungen

Ein Erfassungs Filter sollte nur dann Daten erstellen, wenn der Filter ausgeführt wird. Senden Sie keine Daten von ihren Pins, wenn der Filter angehalten wird. Geben Sie außerdem einen **VFW \_ S \_ \_** -Fehler von der [**cbasefilter:: GetState**](cbasefilter-getstate.md) -Methode zurück, wenn der Filter angehalten wird. Mit diesem Rückgabewert wird dem Filter Diagramm-Manager mitgeteilt, dass er nicht auf Daten aus dem Filter warten soll, während der Filter angehalten wird. Weitere Informationen finden Sie unter [Filter Zustände](filter-states.md).

Der folgende Code zeigt, wie die [**imediafilter:: GetState**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getstate) -Methode implementiert wird:


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

Die Ausgabe Pins eines Erfassungs Filters sollten die [**iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) -Schnittstelle unterstützen, sodass eine Anwendung jede Pin einzeln aktivieren oder deaktivieren kann. Beispielsweise kann eine Anwendung ohne Erfassung eine Vorschau anzeigen und dann in den Aufzeichnungsmodus wechseln, ohne das Filter Diagramm neu zu erstellen. Sie können die [**cbasestreamcontrol**](cbasestreamcontrol.md) -Klasse verwenden, um diese Schnittstelle zu implementieren.

## <a name="time-stamps"></a>Zeitstempel

Wenn der Filter eine Stichprobe erfasst, wird das Beispiel mit der aktuellen streamzeit versehen. Die Endzeit ist die Startzeit und die Dauer. Wenn der Filter beispielsweise bei zehn Samplings pro Sekunde erfasst und die streamzeit 200 Millionen Einheiten beträgt, wenn der Filter das Beispiel erfasst, sollten die Zeitstempel 200 Millionen und 201 Millionen lauten. (Es sind 10 Millionen Einheiten pro Sekunde vorhanden.)

Um die streamzeit zu berechnen, müssen Sie die [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) -Methode aufrufen, um die aktuelle Verweis Zeit abzurufen. Anschließend wird die ursprüngliche Startzeit subtrahit. Rufen Sie alternativ die [**cbasefilter:: streamtime**](cbasefilter-streamtime.md) -Methode auf, die dieselbe Berechnung ausführt. Um den Zeitstempel für ein Beispiel festzulegen, müssen Sie die [**imediasample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) -Methode aufrufen.

Wenn der Filter jedoch über eine Vorschau-Pin verfügt, sollten Beispiele aus der Vorschau-Pin keine Zeitstempel enthalten. Der Grund hierfür ist, dass die Beispiele den Renderer nach dem Zeitpunkt der Erfassung immer etwas erreichen. Wenn die Beispiele Zeitstempel sind, behandelt der Renderer Sie als spät, und es kann versucht werden, Beispiele zu verwerfen. (Weitere Informationen finden Sie unter [DirectShow-Video Erfassungs Filter](directshow-video-capture-filters.md).) Beachten Sie, dass die [**iamstreamcontrol**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) -Schnittstelle erfordert, dass die PIN die Stichproben Zeiten nachverfolgt. Für eine Vorschau-PIN müssen Sie möglicherweise die Implementierung ändern, damit Sie nicht auf Zeitstempel angewiesen ist.

Zeitstempel müssen immer von einem Beispiel auf das nächste erhöht werden. Dies gilt auch, wenn der Filter angehalten wird. Wenn der Filter ausgeführt wird, angehalten und dann erneut ausgeführt wird, muss das erste Beispiel nach der Pause einen größeren Zeitstempel aufweisen als das letzte Beispiel vor der Pause.

Abhängig von den Daten, die Sie erfassen, kann es sinnvoll sein, die Medien Zeit für die Beispiele festzulegen.

Weitere Informationen finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Video Erfassungs Filter](directshow-video-capture-filters.md)
</dt> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> <dt>

[Schreiben von Erfassungs Filtern](writing-capture-filters.md)
</dt> </dl>

 

 



