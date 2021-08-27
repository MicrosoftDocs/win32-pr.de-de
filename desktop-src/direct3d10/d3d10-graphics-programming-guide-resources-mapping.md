---
description: Kopieren und Zugreifen auf Ressourcendaten (Direct3D 10)
ms.assetid: 34fd4d15-ee64-4acf-967d-a4afb6f26329
title: Kopieren und Zugreifen auf Ressourcendaten (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdbe3ec1dc970635a08cea455927f21d8928f48d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466837"
---
# <a name="copying-and-accessing-resource-data-direct3d-10"></a>Kopieren und Zugreifen auf Ressourcendaten (Direct3D 10)

Ressourcen müssen nicht mehr als im Videospeicher oder im Systemspeicher erstellt werden. Oder ob die Runtime den Arbeitsspeicher verwalten soll. Dank der Architektur des neuen WDDM (Windows Display Driver Model) erstellen Anwendungen jetzt Direct3D 10-Ressourcen mit unterschiedlichen Nutzungsflags, um anzugeben, wie die Anwendung die Ressourcendaten verwenden möchte. [](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) Das neue Treibermodell virtualisiert den von Ressourcen verwendeten Arbeitsspeicher. Dann liegt es in der Verantwortung des Betriebssystems, Treibers und Arbeitsspeicher-Managers, Ressourcen in dem bereich zu platzieren, der bei der erwarteten Nutzung möglichst leistungsreich ist.

Der Standardfall ist, dass Ressourcen für die GPU verfügbar sind. Natürlich gibt es zeiten, in denen die Ressourcendaten für die CPU verfügbar sein müssen. Das Kopieren von Ressourcendaten, sodass der entsprechende Prozessor darauf zugreifen kann, ohne die Leistung zu beeinträchtigen, erfordert ein gewisses Wissen über die Funktionsweise der API-Methoden.

-   [Kopieren von Ressourcendaten](#copying-and-accessing-resource-data-direct3d-10)
-   [Zugreifen auf Ressourcendaten](#copying-and-accessing-resource-data-direct3d-10)

## <a name="copying-resource-data"></a>Kopieren von Ressourcendaten

Ressourcen werden im Arbeitsspeicher erstellt, wenn Direct3D einen Create-Aufruf ausricht. Sie können im Videospeicher, Systemspeicher oder einer anderen Art von Arbeitsspeicher erstellt werden. Da das WDDM-Treibermodell diesen Arbeitsspeicher virtualisiert, müssen Anwendungen nicht mehr nachverfolgen, in welcher Art von Arbeitsspeicherressourcen erstellt wird.

Im Idealfall befinden sich alle Ressourcen im Videospeicher, damit die GPU sofort darauf zugreifen kann. Allerdings ist es manchmal erforderlich, dass die CPU die Ressourcendaten liest oder dass die GPU auf Ressourcendaten zugreifen kann, in die die CPU geschrieben hat. Direct3D 10 verarbeitet diese verschiedenen Szenarien, indem die Anwendung eine Verwendung anbietet und dann bei Bedarf mehrere Methoden zum Kopieren von Ressourcendaten anbietet.

Je nachdem, wie die Ressource erstellt wurde, ist es nicht immer möglich, direkt auf die zugrunde liegenden Daten zu zugreifen. Dies kann bedeuten, dass die Ressourcendaten aus der Quellressource in eine andere Ressource kopiert werden müssen, auf die der entsprechende Prozessor zugriff kann. Im Hinblick auf Direct3D 10 kann direkt über die GPU auf Standardressourcen zugegriffen werden, auf dynamische Ressourcen und Stagingressourcen kann direkt von der CPU zugegriffen werden.

Nachdem eine Ressource erstellt wurde, kann [**ihre Nutzung**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) nicht mehr geändert werden. Kopieren Sie stattdessen den Inhalt einer Ressource in eine andere Ressource, die mit einer anderen Verwendung erstellt wurde. Direct3D 10 bietet diese Funktionalität mit drei verschiedenen Methoden. Die ersten beiden Methoden ( [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) und [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) sind so konzipiert, dass Ressourcendaten von einer Ressource in eine andere kopiert werden. Die dritte Methode ([**ID3D10Device::UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)) dient zum Kopieren von Daten aus dem Arbeitsspeicher in eine Ressource.

Es gibt zwei Hauptarten von Ressourcen: mappable und non-mappable. Ressourcen, die mit dynamischen oder Stagingverwendungen erstellt wurden, können zugeordnet werden, während Ressourcen, die mit standard- oder unveränderlichen Verwendungen erstellt wurden, nicht zugeordnet werden können.

Das Kopieren von Daten zwischen nicht mappierbaren Ressourcen ist sehr schnell, da dies der häufigste Fall ist und für eine gute Leistung optimiert wurde. Da die CPU nicht direkt auf diese Ressourcen zugreifen kann, sind sie so optimiert, dass die GPU sie schnell bearbeiten kann.

Das Kopieren von Daten zwischen mappierbaren Ressourcen ist problematischer, da die Leistung von der Nutzung abhängig ist, mit der die Ressource erstellt wurde. Beispielsweise kann die GPU eine dynamische Ressource recht schnell lesen, aber nicht in sie schreiben, und die GPU kann keine direkten Lese- oder Schreibzugriffe auf Stagingressourcen ausführen.

Anwendungen, die Daten aus einer Ressource mit Standardverwendung in eine Ressource mit Stagingnutzung kopieren möchten (um der CPU das Lesen der Daten zu ermöglichen , d. h. das GPU-Rückleseproblem), müssen dies mit Vorsicht tun. Weitere [Informationen zu diesem letzten Fall finden](#copying-and-accessing-resource-data-direct3d-10) Sie unter Zugreifen auf Ressourcendaten.

## <a name="accessing-resource-data"></a>Zugreifen auf Ressourcendaten

Für den Zugriff auf eine Ressource ist eine Zuordnung der Ressource erforderlich. Zuordnung bedeutet im Wesentlichen, dass die Anwendung versucht, der CPU Zugriff auf den Arbeitsspeicher zu geben. Der Vorgang der Zuordnung einer Ressource, sodass die CPU auf den zugrunde liegenden Arbeitsspeicher zugreifen kann, kann zu Leistungsengpässen führen. Aus diesem Grund muss darauf achten, wie und wann diese Aufgabe ausgeführt werden soll.

Die Leistung kann zu einem Stopp führen, wenn die Anwendung versucht, eine Ressource zum falschen Zeitpunkt zu zuordnen. Wenn die Anwendung versucht, auf die Ergebnisse eines Vorgangs zu zugreifen, bevor dieser Vorgang abgeschlossen ist, tritt ein Pipeline-Fehler auf.

Das Ausführen eines Zuordnungsvorgang zum falschen Zeitpunkt kann zu einem schwerwiegenden Leistungsabfall führen, indem die GPU und die CPU gezwungen werden, sich miteinander zu synchronisieren. Diese Synchronisierung wird ausgeführt, wenn die Anwendung auf eine Ressource zugreifen möchte, bevor die GPU mit dem Kopieren in eine Ressource fertig ist, die die CPU zuordnen kann.

Die CPU kann nur aus Ressourcen lesen, die mit dem D3D10 \_ USAGE \_ STAGING-Flag erstellt wurden. Da ressourcen, die mit diesem Flag erstellt wurden, nicht als Ausgaben der Pipeline festgelegt werden können, müssen die Daten in eine Ressource kopiert werden, die mit dem Stagingflag erstellt wurde, wenn die CPU die Daten in einer von der GPU generierten Ressource lesen möchte. Die Anwendung kann dazu die [**Methoden ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) oder [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) verwenden, um den Inhalt einer Ressource in eine andere zu kopieren. Die Anwendung kann dann Zugriff auf diese Ressource erhalten, indem sie die entsprechende Map-Methode aufruft. Wenn der Zugriff auf die Ressource nicht mehr benötigt wird, sollte die Anwendung dann die entsprechende Unmap-Methode aufrufen. Beispiel: [**ID3D10Texture2D::Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) und [**ID3D10Texture2D::Unmap**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-unmap). Die verschiedenen Map-Methoden geben abhängig von den Eingabeflags einige bestimmte Werte zurück. Weitere [**Informationen finden Sie im Abschnitt Hinweise zur**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture1d-map) Karte.

> [!Note]  
> Wenn die Anwendung die Map-Methode aufruft, erhält sie einen Zeiger auf die Ressourcendaten, auf die sie zugreifen kann. Die Runtime stellt sicher, dass der Zeiger je nach Featureebene über eine bestimmte [Ausrichtung verfügt.](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) Für [**D3D \_ FEATURE LEVEL \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level) und höher ist der Zeiger auf 16 Bytes ausgerichtet. Bei niedriger als [**D3D \_ FEATURE \_ LEVEL \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level)wird der Zeiger auf 4 Bytes ausgerichtet. Die 16-Byte-Ausrichtung ermöglicht es der Anwendung, [SSE-optimierte](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))Vorgänge für die Daten nativ ohne Neuausrichtung oder Kopiervorgänge durchzuführen.

 

### <a name="performance-considerations"></a>Überlegungen zur Leistung

Es ist am besten, einen PC als Computer zu verwenden, der als parallele Architektur mit zwei Haupttypen von Prozessoren ausgeführt wird: eine oder mehrere CPUs und eine oder mehrere GPU-Prozessoren. Wie bei jeder parallelen Architektur wird die beste Leistung erzielt, wenn jeder Prozessor mit genügend Aufgaben geplant ist, um zu verhindern, dass er in den Leerlauf überläuft, und wenn die Arbeit eines Prozessors nicht auf die Arbeit eines anderen Prozessors wartet.

Das ungünstigste Szenario für GPU-/CPU-Parallelität ist die Notwendigkeit, einen Prozessor zu zwingen, auf die Ergebnisse der Von einem anderen ausgeführten Arbeit zu warten. Direct3D 10 versucht, diese Kosten zu entfernen, indem die Methoden [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) und [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) asynchron werden. Die Kopie wurde nicht unbedingt zu dem Zeitpunkt ausgeführt, zu dem die Methode zurückgegeben wird. Dies hat den Vorteil, dass die Anwendung die Leistungskosten für das kopieren der Daten erst dann übernimmt, wenn die CPU auf die Daten zutritt. Dies ist der Fall, wenn Map aufgerufen wird. Wenn die Map-Methode aufgerufen wird, nachdem die Daten tatsächlich kopiert wurden, tritt kein Leistungsverlust auf. Wenn andererseits die Map-Methode aufgerufen wird, bevor die Daten kopiert wurden, tritt ein Pipeline-Fehler auf.

Asynchrone Aufrufe in Direct3D 10 (die den großteil der Methoden und insbesondere Renderingaufrufe sind) werden in einem sogenannten Befehlspuffer gespeichert. Dieser Puffer ist für den Grafiktreiber intern und wird für Batchaufrufe an die zugrunde liegende Hardware verwendet, sodass der kostspielige Wechsel vom Benutzermodus zum Kernelmodus in Microsoft Windows so selten wie möglich erfolgt.

Der Befehlspuffer wird geleert, wodurch ein Benutzer-/Kernelmoduswechsel in einer von vier Situationen verursacht wird, die wie folgt sind.

1.  [**Vorhanden**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) wird aufgerufen.
2.  [**ID3D10Device::Flush**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-flush) wird aufgerufen.
3.  Der Befehlspuffer ist voll. Seine Größe ist dynamisch und wird vom Betriebssystem und dem Grafiktreiber gesteuert.
4.  Die CPU erfordert Zugriff auf die Ergebnisse eines Befehls, der auf die Ausführung im Befehlspuffer wartet.

Von den vier oben genannten Situationen ist Nummer 4 für die Leistung am wichtigsten. Wenn die Anwendung einen [**ID3D10Device::CopyResource-**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) oder [**ID3D10Device::CopySubresourceRegion-Aufruf**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) aus gibt, wird dieser Aufruf im Befehlspuffer in die Warteschlange gestellt. Wenn die Anwendung dann versucht, die Stagingressource, die das Ziel des Kopieraufrufs war, zu zuordnen, bevor der Befehlspuffer geleert wurde, tritt ein Pipelinestaufstand auf, da nicht nur der Copy-Methodenaufruf ausgeführt werden muss, sondern auch alle anderen gepufferten Befehle im Befehlspuffer ausgeführt werden müssen. Dies verursacht die Synchronisierung von GPU und CPU, da die CPU auf den Zugriff auf die Stagingressource wartet, während die GPU den Befehlspuffer leert und schließlich die Ressource auffüllt, die die CPU benötigt. Sobald die GPU die Kopie abgeschlossen hat, beginnt die CPU mit dem Zugriff auf die Stagingressource. Während dieser Zeit befindet sich die GPU jedoch im Leerlauf.

Wenn Sie dies häufig zur Laufzeit tun, wird die Leistung erheblich beeinträchtigt. Aus diesem Grund sollte die Zuordnung von Ressourcen, die mit Standardnutzung erstellt wurden, mit Vorsicht erfolgen. Die Anwendung muss lange genug warten, bis der Befehlspuffer geleert wird, und daher müssen alle diese Befehle ausgeführt werden, bevor sie versucht, die entsprechende Stagingressource zu zuordnen. Wie lange sollte die Anwendung warten? Mindestens zwei Frames, da dadurch die Parallelität zwischen den CPUs und der GPU maximal genutzt werden kann. Die GPU funktioniert so, dass während die Anwendung Frame N verarbeitet, indem Aufrufe an den Befehlspuffer gesendet werden, die GPU mit der Ausführung der Aufrufe aus dem vorherigen Frame N-1 beschäftigt ist.

Wenn also eine Anwendung eine Ressource zuordnen möchte, die aus dem Videospeicher stammt und [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) oder [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) in Frame N aufruft, beginnt dieser Aufruf tatsächlich mit der Ausführung im Frame N+1, wenn die Anwendung Aufrufe für den nächsten Frame überträgt. Die Kopie sollte abgeschlossen sein, wenn die Anwendung Frame N+2 verarbeitet.




| Frame | GPU/CPU-Status | 
|-------|----------------|
| N | <ul><li>CPU-Probleme rendern Aufrufe für den aktuellen Frame.</li></ul> | 
| N+1 | <ul><li>GPU, die aufrufe, die während Frame N von der CPU gesendet werden.</li><li>CPU-Probleme rendern Aufrufe für den aktuellen Frame.</li></ul> | 
| N+2 | <ul><li>GPU hat die Ausführung von Aufrufen abgeschlossen, die während frame N von der CPU gesendet wurden. Ergebnisse bereit.</li><li>GPU, die aufrufe, die während des Frames N+1 von der CPU gesendet werden.</li><li>CPU-Probleme rendern Aufrufe für den aktuellen Frame.</li></ul> | 
| N+3 | <ul><li>GPU hat die Ausführung von Aufrufen beendet, die während des Frames N+1 von der CPU gesendet wurden. Ergebnisse bereit.</li><li>GPU zum Ausführen von Aufrufen, die während des Frames N+2 von der CPU gesendet werden.</li><li>CPU-Probleme rendern Aufrufe für den aktuellen Frame.</li></ul> | 
| N+4 | ... | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
