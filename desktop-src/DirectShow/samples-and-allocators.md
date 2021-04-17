---
description: Beispiele und Zuweisungen
ms.assetid: 1fbea741-f29a-4815-9885-94ca9cf4bb95
title: Beispiele und Zuweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9132ff2c70b5ade63f8853b5c03bacb7a25371
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104567190"
---
# <a name="samples-and-allocators"></a>Beispiele und Zuweisungen

Wenn eine PIN Mediendaten an eine andere Pin übergibt, übergibt sie keinen direkten Zeiger auf den Speicherpuffer. Stattdessen übermittelt Sie einen Zeiger auf ein COM-Objekt, das den Arbeitsspeicher verwaltet. Dieses Objekt, das als *Medien Beispiel* bezeichnet wird, macht die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle verfügbar. Die empfangende Pin greift durch Aufrufen von **imediasample** -Methoden (z. b. [**imediasample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer), [**imediasample:: GetSize**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getsize)) und [**imediasample:: getactualdatalength**](/windows/win32/api/strmif/nf-strmif-imediasample-getactualdatalength)auf den Speicherpuffer zu.

Beispiele sind immer Downstream, von der Ausgabe-PIN an die Eingabe-PIN. Im Push-Modell liefert die Ausgabepin ein Beispiel, indem [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) für die Eingabe-PIN aufgerufen wird. Die Eingabe-PIN verarbeitet die Daten entweder synchron (d. h. vollständig innerhalb der **Receive** -Methode) oder verarbeitet sie asynchron in einem Arbeits Thread. Die eingabepin darf innerhalb der **Receive** -Methode blockiert werden, wenn Sie auf Ressourcen warten muss.

Ein anderes com-Objekt, das als *Zuweisung* bezeichnet wird, ist für das Erstellen und Verwalten von Medien Beispielen verantwortlich. Zuweisungen machen die [**imemzuzucator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle verfügbar. Wenn ein Filter ein Medien Beispiel mit einem leeren Puffer benötigt, ruft er die [**imemzuzucator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) -Methode auf, die einen Zeiger auf das Beispiel zurückgibt. Jede Pin-Verbindung hat eine Zuweisung gemeinsam. Wenn zwei Pins eine Verbindung herstellen, entscheiden Sie, welchen Filter die Zuweisung bereitstellen soll. Die Pins legen auch Eigenschaften für die Zuweisung fest, z. b. die Anzahl der Puffer und die Größe der einzelnen Puffer. (Ausführliche Informationen finden Sie unter Gewusst [wie: Filtern](how-filters-connect.md) von Verbindungen und [Aushandeln von Zuweisungen](negotiating-allocators.md).)

Die folgende Abbildung zeigt die Beziehungen zwischen der Zuweisung, den Medien Beispielen und dem Filter.

![Medien Beispiele und-Zuweisungen](images/mediasamples.png)

**Verweis Zähler für Medien Beispiele**

Eine Zuweisung erstellt einen begrenzten Pool von Beispielen. Einige Beispiele werden möglicherweise verwendet, andere sind für **GetBuffer** -Aufrufe verfügbar. Der Zuweiser verwendet die Verweis Zählung, um die Beispiele nachzuverfolgen. Die **GetBuffer** -Methode gibt ein Beispiel mit einem Verweis Zähler von 1 zurück. Wenn der Verweis Zähler auf NULL wechselt, wechselt das Beispiel zurück in den Pool des zuordcators, wo es im nächsten **GetBuffer** -Befehl verwendet werden kann. Solange der Verweis Zähler über 0 (null) bleibt, ist das Beispiel für **GetBuffer** nicht verfügbar. Wenn jedes zu der Zuweisung gehörende Beispiel verwendet wird, blockiert die **GetBuffer** -Methode, bis eine Stichprobe verfügbar wird.

Angenommen, eine Eingabe-PIN empfängt ein Beispiel. Wenn das Beispiel synchron in der **Receive** -Methode verarbeitet wird, erhöht es nicht den Verweis Zähler. Nach dem **Empfang** gibt die Ausgabe-PIN das Beispiel frei, der Verweis Zähler wird auf 0 (null) zurückgesetzt, und das Beispiel kehrt in den Pool des zuordcators zurück. Wenn die Eingabe-PIN dagegen das Beispiel auf einem Arbeits Thread verarbeitet, erhöht es den Verweis Zähler, bevor die **Receive** -Methode verlassen wird. Der Verweis Zähler ist jetzt 2. Wenn die Ausgabe-PIN das Beispiel freigibt, wird die Anzahl auf 1 gesetzt. Das Beispiel wird noch nicht in den Pool zurückgegeben. Nachdem der Arbeits Thread mit dem Beispiel erstellt wurde, wird Release aufgerufen, um das Beispiel frei **zugeben** . Nun wird das Beispiel in den Pool zurückgegeben.

Wenn eine PIN eine Stichprobe empfängt, kann Sie die Daten in ein anderes Beispiel kopieren oder das ursprüngliche Beispiel ändern und diese an den nächsten Filter übermitteln. Möglicherweise kann ein Beispiel die gesamte Länge des Diagramms übertragen, wobei jeder Filter die **adressf** aufrufen und die **Freigabe wiederum freigibt** . Daher muss die Ausgabepin nach dem Aufruf von **Receive** nie ein Beispiel wieder verwenden, da das Beispiel für einen downstreamfilter verwendet werden kann. Die Ausgabe-PIN muss immer **GetBuffer** aufrufen, um ein neues Beispiel zu erhalten.

Dieser Mechanismus verringert die Menge an Speicher Belegung, da Filter die gleichen Puffer wieder verwenden. Außerdem wird verhindert, dass Filter versehentlich Daten schreiben, die noch nicht verarbeitet wurden, da die Zuweisung eine Liste der verfügbaren Beispiele beibehält.

Ein Filter kann separate Zuweisungen für die Eingabe und die Ausgabe verwenden. Dies kann der Fall sein, wenn die Eingabedaten erweitert werden (z. b. durch das komprimieren). Wenn die Ausgabe nicht größer als die Eingabe ist, kann ein Filter die Daten direkt verarbeiten, ohne Sie in ein neues Beispiel zu kopieren. In diesem Fall können zwei oder mehr Pin-Verbindungen eine Zuweisung gemeinsam verwenden.

**Commit und Commit von Zuweisungen**

Wenn ein Filter zuerst eine Zuweisung erstellt, hat die Zuweisung keine Speicherpuffer reserviert. An diesem Punkt treten beim Aufrufen der **GetBuffer** -Methode Fehler auf. Beim Starten des Streamings Ruft die Ausgabepin [**imemallocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit)auf, wodurch die Zuweisung für die Zuweisung ausgeführt wird, wodurch Arbeitsspeicher belegt wird. Pins können nun **GetBuffer** aufrufen.

Wenn das Streaming beendet wird, ruft die PIN [**imemzuzucator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit)auf, der die Zuweisung decommittet. Alle nachfolgenden Aufrufe von **GetBuffer** schlagen fehl, bis für die Zuweisung erneut ein Commit ausgeführt wird. Wenn derzeit Aufrufe von **GetBuffer** blockiert werden, die auf eine Stichprobe warten, geben Sie sofort einen Fehlercode zurück. Die **Decommit** -Methode kann den Arbeitsspeicher in Abhängigkeit von der Implementierung freigeben. Beispielsweise wartet die [**cmemzuordcator**](cmemallocator.md) -Klasse, bis die dekonstruktormethode Arbeitsspeicher freigibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 
