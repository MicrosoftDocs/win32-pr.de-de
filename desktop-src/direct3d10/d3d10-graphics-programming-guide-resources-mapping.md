---
description: Kopieren und Zugreifen auf Ressourcen Daten (Direct3D 10)
ms.assetid: 34fd4d15-ee64-4acf-967d-a4afb6f26329
title: Kopieren und Zugreifen auf Ressourcen Daten (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38bd075585ee3123e163075a50b06b53a77a214c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748520"
---
# <a name="copying-and-accessing-resource-data-direct3d-10"></a>Kopieren und Zugreifen auf Ressourcen Daten (Direct3D 10)

Es ist nicht mehr erforderlich, Ressourcen als in Videospeicher oder Systemspeicher zu erstellen. Oder, unabhängig davon, ob die Laufzeit den Arbeitsspeicher verwalten soll. Dank der Architektur des neuen WDDM (Windows Display Driver Model) erstellen Anwendungen nun Direct3D 10 Ressourcen mit unterschiedlichen [**nutzungsflags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) , um anzugeben, wie die Anwendung die Ressourcen Daten verwenden soll. Das neue Treibermodell virtualisiert den von den Ressourcen genutzten Arbeitsspeicher. Anschließend wird der Betriebssystem-/Treiber-/arbeitsspeichermanager zum Platzieren von Ressourcen im leistungsfähigsten Speicherbereich verwendet, der mit der erwarteten Nutzung möglich ist.

Der Standardfall ist, dass Ressourcen für die GPU verfügbar sind. Natürlich gibt es Zeiten, in denen die Ressourcen Daten für die CPU verfügbar sein müssen. Beim Kopieren von Ressourcen Daten, sodass der entsprechende Prozessor ohne Beeinträchtigung der Leistung darauf zugreifen kann, müssen Sie wissen, wie die API-Methoden funktionieren.

-   [Kopieren von Ressourcen Daten](#copying-and-accessing-resource-data-direct3d-10)
-   [Zugreifen auf Ressourcen Daten](#copying-and-accessing-resource-data-direct3d-10)

## <a name="copying-resource-data"></a>Kopieren von Ressourcen Daten

Ressourcen werden im Arbeitsspeicher erstellt, wenn Direct3D einen Create-Befehl ausführt. Sie können im Videospeicher, im Systemspeicher oder in einer beliebigen anderen Art von Arbeitsspeicher erstellt werden. Da das WDDM-Treibermodell diesen Arbeitsspeicher virtualisiert, müssen Anwendungen nicht mehr nachverfolgen, welche Art von Arbeitsspeicher Ressourcen in erstellt werden.

Im Idealfall befinden sich alle Ressourcen im Videospeicher, sodass die GPU unmittelbaren Zugriff auf Sie haben kann. Allerdings ist es manchmal erforderlich, dass die CPU die Ressourcen Daten liest oder dass die GPU auf Ressourcen Daten zugreift, auf die die CPU geschrieben hat. Direct3D 10 verarbeitet diese verschiedenen Szenarien, indem angefordert wird, dass die Anwendung eine Verwendung angibt, und bietet dann mehrere Methoden zum Kopieren von Ressourcen Daten bei Bedarf.

Abhängig davon, wie die Ressource erstellt wurde, ist es nicht immer möglich, direkt auf die zugrunde liegenden Daten zuzugreifen. Dies kann bedeuten, dass die Ressourcen Daten aus der Quell Ressource in eine andere Ressource kopiert werden müssen, auf die der entsprechende Prozessor zugreifen kann. Im Hinblick auf Direct3D 10 können auf Standard Ressourcen direkt durch die GPU zugegriffen werden, und auf dynamische und stagingressourcen kann direkt über die CPU zugegriffen werden.

Nachdem eine Ressource erstellt wurde, kann Sie [**nicht mehr**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) geändert werden. Kopieren Sie stattdessen den Inhalt einer Ressource in eine andere Ressource, die mit einer anderen Verwendung erstellt wurde. Direct3D 10 stellt diese Funktionalität mit drei verschiedenen Methoden bereit. Die ersten beiden Methoden ( [**ID3D10Device:: copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) und [**ID3D10Device:: copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) dienen zum Kopieren von Ressourcen Daten aus einer Ressource in eine andere. Die dritte Methode ([**ID3D10Device:: updatesubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)) ist so konzipiert, dass Daten aus dem Arbeitsspeicher in eine Ressource kopiert werden.

Es gibt zwei Hauptarten von Ressourcen: mappable und Non-mappable. Ressourcen, die mit dynamischer oder stagingverwendungen erstellt werden, sind mappable, während Ressourcen, die mit standardmäßigen oder unveränderlichen Verwendungen erstellt wurden, nicht mappbar sind.

Das Kopieren von Daten in nicht mappbare Ressourcen ist sehr schnell, da dies der häufigste Fall ist und für eine gute Leistung optimiert wurde. Da diese Ressourcen nicht direkt von der CPU zugänglich sind, werden Sie optimiert, sodass Sie von der GPU schnell bearbeitet werden können.

Das Kopieren von Daten zwischen mappable-Ressourcen ist problematisch, da die Leistung von der Nutzung abhängig ist, mit der die Ressource erstellt wurde. Beispielsweise kann die GPU eine dynamische Ressource recht schnell lesen, aber nicht in Sie schreiben, und die GPU kann die stagingressourcen nicht direkt lesen oder in diese schreiben.

Anwendungen, die Daten aus einer Ressource mit der standardmäßigen Verwendung in eine Ressource mit stagingverwendung kopieren möchten (um der CPU das Lesen der Daten zu ermöglichen, d. h. das GPU-Lese Back Problem), müssen dies mit Bedacht tun. Weitere Informationen zu diesem letzten Fall finden Sie unter [zugreifen auf Ressourcen Daten](#copying-and-accessing-resource-data-direct3d-10) .

## <a name="accessing-resource-data"></a>Zugreifen auf Ressourcen Daten

Der Zugriff auf eine Ressource erfordert die Zuordnung der Ressource. die Zuordnung bedeutet im Wesentlichen, dass die Anwendung versucht, dem CPU-Zugriff auf den Arbeitsspeicher zu übergeben. Der Prozess der Zuordnung einer Ressource, sodass die CPU auf den zugrunde liegenden Speicher zugreifen kann, kann zu Leistungs Engpässen führen. aus diesem Grund müssen Sie darauf achten, wie und wann diese Aufgabe durchgeführt werden soll.

Die Leistung kann angehalten werden, wenn die Anwendung versucht, eine Ressource zu einem falschen Zeitpunkt zuzuordnen. Wenn die Anwendung versucht, auf die Ergebnisse eines Vorgangs zuzugreifen, bevor dieser Vorgang abgeschlossen ist, tritt ein Pipeline-Stall ein.

Wenn Sie einen Zuordnungs Vorgang zum falschen Zeitpunkt durchführen, kann dies zu einem schwerwiegenden Leistungsabfall führen, indem die GPU und die CPU voneinander synchronisiert werden. Diese Synchronisierung wird ausgeführt, wenn die Anwendung auf eine Ressource zugreifen möchte, bevor Sie von der GPU in eine Ressource kopiert werden kann, die die CPU zuordnen kann.

Die CPU kann nur aus Ressourcen lesen, die mit dem d3d10 Usage-Staging-Flag erstellt wurden \_ \_ . Da mit diesem Flag erstellte Ressourcen nicht als Ausgaben der Pipeline festgelegt werden können, müssen die Daten in eine Ressource kopiert werden, die mit dem Staging-Flag erstellt wurde, wenn die CPU die Daten in einer von der GPU generierten Ressource lesen möchte. Die Anwendung kann dies mithilfe der [**ID3D10Device:: copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) -Methode oder der [**ID3D10Device:: copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) -Methode durchführen, um den Inhalt einer Ressource in eine andere zu kopieren. Die Anwendung kann dann durch Aufrufen der entsprechenden Map-Methode Zugriff auf diese Ressource erhalten. Wenn der Zugriff auf die Ressource nicht mehr benötigt wird, sollte die Anwendung die entsprechende unmap-Methode aufrufen. Beispiel: [**ID3D10Texture2D:: Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) und [**ID3D10Texture2D:: unmap**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-unmap). Die verschiedenen Map-Methoden geben abhängig von den eingabeflags bestimmte Werte zurück. Weitere Informationen finden Sie im [**Abschnitt Karten Hinweise**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture1d-map) .

> [!Note]  
> Wenn die Anwendung die Map-Methode aufruft, empfängt Sie einen Zeiger auf die Ressourcen Daten, auf die zugegriffen werden soll. Die Laufzeit stellt sicher, dass der Zeiger abhängig von der [Funktionsebene](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)über eine bestimmte Ausrichtung verfügt. Für [**D3D- \_ Funktions \_ Ebene von \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level) und höher wird der Zeiger auf 16 Bytes ausgerichtet. Für einen niedrigeren [**Wert als D3D \_ \_ Featureebene \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level)ist der Zeiger auf 4 Bytes ausgerichtet. Die 16-Byte-Ausrichtung ermöglicht es der Anwendung, [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))-optimierte Vorgänge für die Daten nativ auszuführen, ohne eine Neuausrichtung oder Kopie auszuführen.

 

### <a name="performance-considerations"></a>Überlegungen zur Leistung

Es empfiehlt sich, einen PC als einen Computer zu betrachten, der als parallele Architektur mit zwei Haupttypen von Prozessoren ausgeführt wird: eine oder mehrere CPU-und mindestens eine GPU. Wie bei jeder parallelen Architektur wird die beste Leistung erzielt, wenn jeder Prozessor mit ausreichenden Aufgaben geplant wird, um zu verhindern, dass er in den Leerlauf versetzt wird, und wenn die Arbeit eines Prozessors nicht auf die Arbeit eines anderen Prozessors wartet.

Das ungünstigste Szenario bei GPU-/CPU-Parallelität besteht darin, dass ein Prozessor gezwungen werden muss, auf die Ergebnisse der von einer anderen Aufgabe ausgeführten Arbeit zu warten. Direct3D 10 versucht, diese Kosten zu entfernen, indem die [**ID3D10Device:: copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) -und [**ID3D10Device:: copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) -Methoden asynchron gemacht werden. die Kopie wurde nicht notwendigerweise von dem Zeitpunkt ausgeführt, an dem die Methode zurückgegeben wird. Der Vorteil besteht darin, dass die Anwendung nicht die Leistungskosten für das eigentliche Kopieren der Daten abzahlt, bis die CPU auf die Daten zugreift. Dies ist der Fall, wenn Map aufgerufen wird. Wenn die Map-Methode aufgerufen wird, nachdem die Daten tatsächlich kopiert wurden, tritt kein Leistungsverlust auf. Wenn andererseits die Map-Methode aufgerufen wird, bevor die Daten kopiert wurden, tritt ein Pipeline-Stall auf.

Asynchrone Aufrufe in Direct3D 10 (bei denen es sich um die meisten Methoden und insbesondere renderingaufrufe handelt) werden in dem als Befehls Puffer bezeichneten Vorgang gespeichert. Dieser Puffer ist für den Grafiktreiber intern und wird zum Batches von Aufrufen an die zugrunde liegende Hardware verwendet, sodass der kostspielige Wechsel vom Benutzermodus in den Kernel Modus in Microsoft Windows so selten wie möglich erfolgt.

Der Befehls Puffer wird geleert, wodurch ein Benutzer-/kernelmodusschalter in einer von vier Situationen wie folgt verursacht wird.

1.  [**Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) wird aufgerufen.
2.  [**ID3D10Device:: Flush**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-flush) wird aufgerufen.
3.  Der Befehls Puffer ist voll. seine Größe ist dynamisch und wird vom Betriebs System und dem Grafiktreiber gesteuert.
4.  Die CPU erfordert Zugriff auf die Ergebnisse eines Befehls, der auf die Ausführung im Befehls Puffer wartet.

In den vier oben genannten Situationen ist die Zahl vier die wichtigste für die Leistung. Wenn die Anwendung einen [**ID3D10Device:: copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) -oder [**ID3D10Device:: copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) -Befehl ausgibt, wird dieser Befehl im Befehls Puffer in die Warteschlange eingereiht. Wenn die Anwendung dann versucht, die stagingressource, die das Ziel des Kopier Aufrufens war, vor dem leeren des Befehls Puffers zuzuordnen, wird ein Pipeline-Stall ausgelöst, da nicht nur der Kopiermethoden Aufrufe ausgeführt werden muss, sondern alle anderen gepufferten Befehle im Befehls Puffer ebenfalls ausgeführt werden müssen. Dies bewirkt, dass die GPU und CPU synchronisiert werden, da die CPU auf den Zugriff auf die stagingressource wartet, während die GPU den Befehls Puffer geleert und schließlich die Ressource abfüllt, die die CPU benötigt. Nachdem die GPU die Kopie abgeschlossen hat, beginnt die CPU mit dem Zugriff auf die stagingressource. während dieser Zeit befindet sich die GPU jedoch im Leerlauf.

Wenn dies häufig zur Laufzeit erfolgt, wird die Leistung erheblich beeinträchtigt. Aus diesem Grund sollte die Zuordnung von mit der Standardverwendung erstellten Ressourcen mit Bedacht erfolgen. Die Anwendung muss lange genug warten, bis der Befehls Puffer geleert ist, und daher wird die Ausführung aller Befehle beendet, bevor versucht wird, die entsprechende stagingressource zuzuordnen. Wie lange sollte die Anwendung warten? Mindestens zwei Frames, da dadurch die Parallelität zwischen den CPU (s) und der GPU für eine maximale Nutzung aktiviert wird. Die GPU funktioniert so, dass die GPU während der Verarbeitung von Frame N durch das Übermitteln von Aufrufen an den Befehls Puffer ausgelastet ist, dass die GPU mit dem Ausführen der Aufrufe aus dem vorherigen Frame, N-1, ausgelastet ist.

Wenn also eine Anwendung eine Ressource zuordnen möchte, die aus dem Videospeicher stammt und [**ID3D10Device:: copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) oder [**ID3D10Device:: copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) bei Frame n aufruft, beginnt dieser Aufruf tatsächlich mit der Ausführung bei Frame n + 1, wenn die Anwendung Aufrufe für den nächsten Frame übermittelt. Der Kopiervorgang sollte abgeschlossen sein, wenn die Anwendung den Frame "N + 2" verarbeitet.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Frame</th>
<th>GPU-/CPU-Status</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>N</td>
<td><ul>
<li>"CPU" gibt Rendering-Aufrufe für aktuellen Frame aus.</li>
</ul></td>
</tr>
<tr class="even">
<td>N + 1</td>
<td><ul>
<li>GPU führt Aufrufe aus, die während des Frame N von der CPU gesendet werden</li>
<li>"CPU" gibt Rendering-Aufrufe für aktuellen Frame aus.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N + 2</td>
<td><ul>
<li>Die GPU hat das Ausführen von Aufrufen von der CPU während Frame N abgeschlossen. die Ergebnisse sind bereit.</li>
<li>GPU-Aufrufe, die von der CPU während des Frame N + 1 gesendet werden.</li>
<li>"CPU" gibt Rendering-Aufrufe für aktuellen Frame aus.</li>
</ul></td>
</tr>
<tr class="even">
<td>N + 3</td>
<td><ul>
<li>Die GPU hat das Ausführen von Aufrufen von der CPU während des Frame N + 1 abgeschlossen. Die Ergebnisse sind bereit.</li>
<li>GPU führt Aufrufe aus, die während des Frames N + 2 von der CPU gesendet werden.</li>
<li>"CPU" gibt Rendering-Aufrufe für aktuellen Frame aus.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N + 4</td>
<td>...</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
