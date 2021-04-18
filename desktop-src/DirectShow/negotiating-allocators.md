---
description: Aushandeln von Zuweisungen
ms.assetid: fe13477c-1a7b-4098-9d0f-c54783102bc9
title: Aushandeln von Zuweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2faa393ba9fcd8585d68947cec172d4cfca6decf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344316"
---
# <a name="negotiating-allocators"></a>Aushandeln von Zuweisungen

Wenn zwei Pins eine Verbindung herstellen, benötigen Sie einen Mechanismus zum Austauschen von Mediendaten. Dieser Mechanismus wird als *Transport* bezeichnet. Im Allgemeinen ist die DirectShow-Architektur in Bezug auf Transporte neutral. Zwei Filter können eine Verbindung mit einem beliebigen von beiden unterstützten Transport herstellen.

Der häufigste Transport ist der *lokale Speicher* Transport, in dem sich die Mediendaten im Hauptspeicher befinden. Es sind zwei Varianten des lokalen Speicher Transports vorhanden: das *Push-Modell* und das *Pull-Modell*. Im Push-Modell überträgt der Quell Filterdaten mithilfe der [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle auf die Eingabe-PIN des downstreamfilters an den downstreamfilter. Im Pull-Modell fordert der Downstream-Filterdaten aus dem Quell Filter an und verwendet dabei die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle in der Ausgabe-PIN des Quell Filters. Weitere Informationen zu diesen beiden Datenfluss Modellen finden Sie unter [Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md).

Beim lokalen Speicher Transport wird das für die Zuordnung von Speicher Puffern verantwortliche Objekt als *Zuweisungs* Name bezeichnet. Eine Zuweisung unterstützt die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle. Beide Pins haben einen einzelnen Zuweiser gemeinsam. Beide Pins können eine Zuweisung bereitstellen, aber die Ausgabe-PIN wählt aus, welche Zuweisung verwendet werden soll.

Mit der Ausgabe-PIN werden auch die Zuweisungs Eigenschaften festgelegt, die bestimmen, wie viele Puffer von der Zuweisung, der Größe der einzelnen Puffer und der Arbeitsspeicher Ausrichtung erstellt werden. Die Ausgabe-PIN kann die Eingabe-PIN für die Puffer Anforderungen verzögern.

In einer **IMemInputPin** -Verbindung funktioniert die Zuordnungs Aushandlung wie folgt:

1.  Optional Ruft die Ausgabe-PIN [**IMemInputPin:: getallogorrequirements**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements)auf. Diese Methode ruft die Puffer Anforderungen der Eingabe-PIN ab, z. b. die Arbeitsspeicher Ausrichtung. Im Allgemeinen sollte die Ausgabe-PIN die Anforderung der Eingabe-PIN beachten, es sei denn, es gibt keinen guten Grund, warum dies nicht der Fall ist.
2.  Optional Ruft die Ausgabe-PIN [**IMemInputPin:: getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator)auf. Diese Methode fordert eine Zuweisung von der eingabepin an. Die Eingabe-PIN stellt eine bereit, oder es wird ein Fehlercode zurückgegeben.
3.  Mit dem Ausgabepin wird eine Zuweisung ausgewählt. Sie kann eine von der Eingabe-PIN bereitgestellte verwenden oder eine eigene erstellen.
4.  Die Ausgabe-PIN ruft [**imemzuzucator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) auf, um die zuordnereigenschaften festzulegen. Die Zuweisung berücksichtigt die angeforderten Eigenschaften jedoch möglicherweise nicht. (Dies kann beispielsweise der Fall sein, wenn die Eingabe-PIN die Zuweisung bereitstellt.) Die Zuweisung gibt die tatsächlichen Eigenschaften als Ausgabeparameter in der **SetProperties** -Methode zurück.
5.  Mit dem outpin wird [**IMemInputPin:: notifyzuweisung**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) aufgerufen, um die Eingabe-PIN der Auswahl zu informieren.
6.  Die eingabepin muss [**imemzucator:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getproperties) aufrufen, um zu überprüfen, ob die zuordnereigenschaften zulässig sind.
7.  Die Ausgabe-PIN ist für das committen und das Debuggen der Zuweisung verantwortlich. Dies tritt auf, wenn das Streaming gestartet und beendet wird.

In einer **iasynkreader** -Verbindung funktioniert die Zuordnungs Aushandlung wie folgt:

1.  Die eingabepin ruft [**iasynkreader:: requestzuweisung**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-requestallocator) in der Ausgabe-PIN auf. Die Eingabe-PIN gibt die Puffer Anforderungen an und stellt optional eine Zuweisung bereit.
2.  Mit dem Ausgabepin wird eine Zuweisung ausgewählt. Sie kann die von der Eingabe-PIN bereitgestellte, sofern vorhanden, oder eine eigene erstellen.
3.  Die Ausgabe-PIN gibt die Zuweisung als ausgehenden Parameter in der **requestzuweisung** -Methode zurück. Die eingabepin sollte die zuordnereigenschaften überprüfen.
4.  Die eingabepin ist für das committen und das committen der Zuweisung verantwortlich.
5.  Während des zuordneraushandlungs Prozesses kann jede PIN jederzeit einen Fehler bei der Verbindung herstellen.
6.  Wenn die Ausgabepin die Zuweisung der Eingabe-PIN verwendet, kann Sie diese Zuweisung nur für die Bereitstellung von Beispielen an diese Eingabe-PIN verwenden. Der besitzende Filter darf die Zuweisung nicht verwenden, um Stichproben an andere Pins zu übermitteln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bereitstellen einer benutzerdefinierten Zuweisung](providing-a-custom-allocator.md)
</dt> </dl>

 

 



