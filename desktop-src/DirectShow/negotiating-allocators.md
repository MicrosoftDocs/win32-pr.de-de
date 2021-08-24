---
description: Aushandeln von Zuweisungen
ms.assetid: fe13477c-1a7b-4098-9d0f-c54783102bc9
title: Aushandeln von Zuweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710b8315bfd44371a82d995afa56483414623136a6ce5c510babd5ea07b4b8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790940"
---
# <a name="negotiating-allocators"></a>Aushandeln von Zuweisungen

Wenn zwei Stecknadeln eine Verbindung herstellen, benötigen sie einen Mechanismus zum Austauschen von Mediendaten. Dieser Mechanismus wird als Transport *bezeichnet.* Im Allgemeinen ist die DirectShow-Architektur für Transporte neutral. Zwei Filter können zustimmen, eine Verbindung mit jedem Transport herzustellen, der von beiden unterstützt wird.

Der häufigste Transport ist der *lokale Speichertransport,* bei dem sich die Mediendaten im Hauptspeicher befinden. Es gibt zwei Varianten des lokalen Speichertransports: das *Pushmodell* und das *Pullmodell*. Im Pushmodell über pusht der Quellfilter Daten mithilfe der [**IMemInputPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) am Eingabepin des Downstreamfilters an den Downstreamfilter. Im Pullmodell fordert der Downstreamfilter Daten vom Quellfilter an, indem er die [**IAsyncReader-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) auf dem Ausgabepin des Quellfilters verwendet. Weitere Informationen zu diesen beiden Datenflussmodellen finden Sie unter [Data Flow in the Filter Graph.](data-flow-in-the-filter-graph.md)

Beim lokalen Speichertransport wird das Objekt, das für die Zuweisung von Speicherpuffern zuständig ist, als Zuweisung *bezeichnet.* Eine Zuweisung unterstützt die [**IMemAllocator-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) Beide Stecknadeln teilen sich eine einzelne Zuweisung. Beide Pins können eine Zuweisung bereitstellen, aber der Ausgabepin wählt die zu verwendende Zuweisung aus.

Der Ausgabepin legt auch die Zuweisungseigenschaften fest, die bestimmen, wie viele Puffer von der Zuweisung erstellt werden, die Größe der einzelnen Puffer und die Arbeitsspeicherausrichtung. Der Ausgabepin kann für die Pufferanforderungen auf den Eingabepin zurückdrennen.

In einer **IMemInputPin-Verbindung** funktioniert die Zuweisungsaushandlung wie folgt:

1.  Optional ruft der Ausgabepin [**IMemInputPin::GetAllocatorRequirements auf.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements) Diese Methode ruft die Pufferanforderungen des Eingabepins ab, z. B. die Arbeitsspeicherausrichtung. Im Allgemeinen sollte der Ausgabepin die Anforderung des Eingabepins verwenden, es sei denn, es gibt einen guten Grund, dies nicht zu tun.
2.  Optional ruft der Ausgabepin [**IMemInputPin::GetAllocator auf.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator) Diese Methode fordert eine Zuweisung vom Eingabepin an. Der Eingabepin gibt einen Fehlercode an oder gibt einen Fehlercode zurück.
3.  Der Ausgabepin wählt eine Zuweisung aus. Sie kann eine vom Eingabepin bereitgestellte verwenden oder eine eigene erstellen.
4.  Der Ausgabepin ruft [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) auf, um die Zuweisungseigenschaften zu festlegen. Allerdings werden die angeforderten Eigenschaften von der Zuweisung möglicherweise nicht verwendet. (Dies kann z. B. passieren, wenn der Eingabepin die Zuweisung anordnt.) Die Zuweisung gibt die tatsächlichen Eigenschaften als Ausgabeparameter in der **SetProperties-Methode** zurück.
5.  Der Outpin ruft [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) auf, um den Eingabepin über die Auswahl zu informieren.
6.  Der Eingabepin sollte [**IMemAllocator::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) aufrufen, um zu überprüfen, ob die Zuweisungseigenschaften akzeptabel sind.
7.  Der Ausgabepin ist für das Committen und Decommitieren der Zuweisung verantwortlich. Dies tritt auf, wenn das Streaming gestartet und beendet wird.

In einer **IAsyncReader-Verbindung** funktioniert die Zuweisungsaushandlung wie folgt:

1.  Der Eingabepin ruft [**IAsyncReader::RequestAllocator**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) auf dem Ausgabepin auf. Der Eingabepin gibt die Pufferanforderungen an und stellt optional eine Zuweisung zur Wahl.
2.  Der Ausgabepin wählt eine Zuweisung aus. Sie kann die vom Eingabepin bereitgestellte (sofern vorhanden) verwenden oder eine eigene erstellen.
3.  Der Ausgabepin gibt die Zuweisung als ausgehenden Parameter in der **RequestAllocator-Methode** zurück. Der Eingabepin sollte die Zuweisungseigenschaften überprüfen.
4.  Der Eingabepin ist für das Committen und Decommitieren der Zuweisung verantwortlich.
5.  Während der Zuweisungsaushandlung kann bei beiden Pins jederzeit ein Fehler bei der Verbindung hergestellt werden.
6.  Wenn der Ausgabepin die Zuweisung des Eingabepins verwendet, kann er diese Zuweisung nur verwenden, um Stichproben an diesen Eingabepin zu liefern. Der besitzende Filter darf die Zuweisung nicht verwenden, um Stichproben an andere Pins zu liefern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bereitstellen einer benutzerdefinierten Zuweisung](providing-a-custom-allocator.md)
</dt> </dl>

 

 



