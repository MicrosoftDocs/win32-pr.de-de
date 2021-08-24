---
description: Kopieren und Zugreifen auf Ressourcendaten (Direct3D 10)
ms.assetid: 34fd4d15-ee64-4acf-967d-a4afb6f26329
title: Kopieren und Zugreifen auf Ressourcendaten (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ffe7bcec876382e17bfd9421d8d6bf715981ec4623d6c264078116536ef269e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409430"
---
# <a name="copying-and-accessing-resource-data-direct3d-10"></a>Kopieren und Zugreifen auf Ressourcendaten (Direct3D 10)

Es ist nicht mehr erforderlich, ressourcen so zu betrachten, als ob sie im Video- oder Systemspeicher erstellt werden. Oder ob die Laufzeit den Arbeitsspeicher verwalten soll. Dank der Architektur des neuen WDDM (Windows Display Driver Model) erstellen Anwendungen jetzt Direct3D 10-Ressourcen mit unterschiedlichen Verwendungsflags, um anzugeben, wie die Anwendung die Ressourcendaten verwenden möchte. [](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) Das neue Treibermodell virtualisiert den von Ressourcen verwendeten Arbeitsspeicher. dann ist der Betriebssystem-/ Treiber-/Arbeitsspeicher-Manager dafür verantwortlich, Ressourcen im leistungsstärksten Speicherbereich zu platzieren, der angesichts der erwarteten Auslastung möglich ist.

Der Standardfall ist, dass Ressourcen für die GPU verfügbar sind. Natürlich gibt es Zeiten, in denen die Ressourcendaten für die CPU verfügbar sein müssen. Das Kopieren von Ressourcendaten, sodass der entsprechende Prozessor ohne Beeinträchtigung der Leistung darauf zugreifen kann, erfordert kenntnisse über die Funktionsweise der API-Methoden.

-   [Kopieren von Ressourcendaten](#copying-and-accessing-resource-data-direct3d-10)
-   [Zugreifen auf Ressourcendaten](#copying-and-accessing-resource-data-direct3d-10)

## <a name="copying-resource-data"></a>Kopieren von Ressourcendaten

Ressourcen werden im Arbeitsspeicher erstellt, wenn Direct3D einen Create-Aufruf ausführt. Sie können im Videospeicher, Systemspeicher oder in einer beliebigen anderen Art von Arbeitsspeicher erstellt werden. Da das WDDM-Treibermodell diesen Arbeitsspeicher virtualisiert, müssen Anwendungen nicht mehr nachverfolgen, in welcher Art von Arbeitsspeicherressourcen erstellt werden.

Im Idealfall befinden sich alle Ressourcen im Videospeicher, damit die GPU sofort darauf zugreifen kann. Manchmal ist es jedoch erforderlich, dass die CPU die Ressourcendaten liest oder dass die GPU auf Ressourcendaten zugreift, in die die CPU geschrieben wurde. Direct3D 10 verarbeitet diese verschiedenen Szenarien, indem die Anwendung eine Verwendung anfordert und dann bei Bedarf mehrere Methoden zum Kopieren von Ressourcendaten anbietet.

Je nachdem, wie die Ressource erstellt wurde, ist es nicht immer möglich, direkt auf die zugrunde liegenden Daten zuzugreifen. Dies kann bedeuten, dass die Ressourcendaten aus der Quellressource in eine andere Ressource kopiert werden müssen, auf die der entsprechende Prozessor zugreifen kann. Im Hinblick auf Direct3D 10 kann direkt über die GPU auf Standardressourcen zugegriffen werden, auf dynamische Ressourcen und Stagingressourcen kann direkt von der CPU zugegriffen werden.

Nachdem eine Ressource erstellt wurde, kann ihre [**Nutzung**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) nicht mehr geändert werden. Kopieren Sie stattdessen den Inhalt einer Ressource in eine andere Ressource, die mit einer anderen Verwendung erstellt wurde. Direct3D 10 bietet diese Funktionalität mit drei verschiedenen Methoden. Die ersten beiden Methoden( [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) und [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) wurden entwickelt, um Ressourcendaten von einer Ressource in eine andere zu kopieren. Die dritte Methode ([**ID3D10Device::UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)) dient zum Kopieren von Daten aus dem Arbeitsspeicher in eine Ressource.

Es gibt zwei Hauptarten von Ressourcen: mappable und non-mappable. Ressourcen, die mit dynamischen oder Stagingverwendungen erstellt werden, können zugeordnet werden, während Ressourcen, die mit Standardverwendungen oder unveränderlichen Verwendungen erstellt wurden, nicht zugeordnet werden können.

Das Kopieren von Daten zwischen nicht abbildbaren Ressourcen ist sehr schnell, da dies der häufigste Fall ist und für eine optimale Leistung optimiert wurde. Da die CPU nicht direkt auf diese Ressourcen zugreifen kann, sind sie so optimiert, dass die GPU sie schnell bearbeiten kann.

Das Kopieren von Daten zwischen zugeordneten Ressourcen ist problematischer, da die Leistung von der Nutzung abhängt, mit der die Ressource erstellt wurde. Beispielsweise kann die GPU eine dynamische Ressource relativ schnell lesen, aber nicht in sie schreiben, und die GPU kann nicht direkt in Stagingressourcen lesen oder schreiben.

Anwendungen, die Daten aus einer Ressource mit Standardnutzung in eine Ressource mit Stagingnutzung kopieren möchten (damit die CPU die Daten lesen kann , d. h. das GPU-Rückleseproblem), müssen dies mit Vorsicht tun. Weitere Informationen zu diesem letzten Fall finden Sie unter Zugreifen auf [Ressourcendaten.](#copying-and-accessing-resource-data-direct3d-10)

## <a name="accessing-resource-data"></a>Zugreifen auf Ressourcendaten

Für den Zugriff auf eine Ressource muss die Ressource zugeordnet werden. Zuordnung bedeutet im Wesentlichen, dass die Anwendung versucht, der CPU Zugriff auf den Arbeitsspeicher zu gewähren. Der Prozess der Zuordnung einer Ressource, sodass die CPU auf den zugrunde liegenden Arbeitsspeicher zugreifen kann, kann zu Leistungsengpässen führen. Aus diesem Grund muss sorgfältig darauf geachtet werden, wie und wann diese Aufgabe ausgeführt werden soll.

Die Leistung kann angehalten werden, wenn die Anwendung versucht, eine Ressource zur falschen Zeit zuzuordnen. Wenn die Anwendung versucht, auf die Ergebnisse eines Vorgangs zuzugreifen, bevor dieser Vorgang abgeschlossen ist, wird eine Pipeline angehalten.

Das Ausführen eines Zuordnungsvorgangs zur falschen Zeit kann zu einem schwerwiegenden Leistungsverlust führen, da gpu und CPU miteinander synchronisiert werden müssen. Diese Synchronisierung findet statt, wenn die Anwendung auf eine Ressource zugreifen möchte, bevor die GPU sie in eine Ressource kopiert, die die CPU zuordnen kann.

Die CPU kann nur aus Ressourcen lesen, die mit dem STAGINGflag D3D10 USAGE erstellt \_ \_ wurden. Da ressourcen, die mit diesem Flag erstellt wurden, nicht als Ausgaben der Pipeline festgelegt werden können, müssen die Daten in eine Ressource kopiert werden, die mit dem Stagingflag erstellt wurde, wenn die CPU die Daten in einer von der GPU generierten Ressource lesen möchte. Die Anwendung kann dazu die Methoden [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) oder [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) verwenden, um den Inhalt einer Ressource in eine andere zu kopieren. Die Anwendung kann dann Zugriff auf diese Ressource erhalten, indem sie die entsprechende Map-Methode aufruft. Wenn der Zugriff auf die Ressource nicht mehr benötigt wird, sollte die Anwendung die entsprechende Unmap-Methode aufrufen. Beispiel: [**ID3D10Texture2D::Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) und [**ID3D10Texture2D::Unmap**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-unmap). Die verschiedenen Map-Methoden geben abhängig von den Eingabeflags einige bestimmte Werte zurück. Weitere Informationen finden Sie [**im Abschnitt Map Remarks (Hinweise zur Karte).**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture1d-map)

> [!Note]  
> Wenn die Anwendung die Map-Methode aufruft, erhält sie einen Zeiger auf die Ressourcendaten, auf die zugegriffen werden soll. Die Runtime stellt sicher, dass der Zeiger abhängig von der Funktionsebene eine bestimmte Ausrichtung [hat.](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) Für [**D3D \_ FEATURE LEVEL \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level) und höher wird der Zeiger auf 16 Bytes ausgerichtet. Bei niedriger als [**D3D \_ FEATURE \_ LEVEL \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level)wird der Zeiger auf 4 Bytes ausgerichtet. Mit der 16-Byte-Ausrichtung kann die Anwendung [SSE-optimierte](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))Vorgänge für die Daten nativ ausführen, ohne dass eine neu ausgerichtete Ausrichtung oder Kopie erfolgt.

 

### <a name="performance-considerations"></a>Überlegungen zur Leistung

Es ist am besten, sich einen PC als Computer zu vorstellen, der als parallele Architektur mit zwei Hauptprozessortypen ausgeführt wird: mindestens eine CPU und mindestens eine GPU. Wie bei jeder parallelen Architektur wird die beste Leistung erzielt, wenn jeder Prozessor mit genügend Aufgaben geplant ist, um zu verhindern, dass er in den Leerlauf geht und wenn die Arbeit eines Prozessors nicht auf die Arbeit eines anderen Prozessors wartet.

Das worst-case-Szenario für GPU-/CPU-Parallelität ist die Notwendigkeit, einen Prozessor zu zwingen, auf die Ergebnisse der arbeit zu warten, die von einem anderen ausgeführt wird. Direct3D 10 versucht, diese Kosten zu entfernen, indem die Methoden [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) und [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) asynchron werden. Die Kopie wurde nicht notwendigerweise bis zum Zeitpunkt der Rückgabe der Methode ausgeführt. Der Vorteil besteht darin, dass die Anwendung die Leistungskosten des tatsächlichen Kopierens der Daten erst dann bezahlt, wenn die CPU auf die Daten zugreift, d. h. wenn Map aufgerufen wird. Wenn die Map-Methode aufgerufen wird, nachdem die Daten tatsächlich kopiert wurden, tritt kein Leistungsverlust auf. Wenn dagegen die Map-Methode aufgerufen wird, bevor die Daten kopiert wurden, tritt ein Pipelinefehler auf.

Asynchrone Aufrufe in Direct3D 10 (die den Großteil der Methoden und insbesondere Renderingaufrufe darstellen) werden in einem sogenannten Befehlspuffer gespeichert. Dieser Puffer ist für den Grafiktreiber intern und wird zum Batchen von Aufrufen der zugrunde liegenden Hardware verwendet, sodass der kostspielige Wechsel vom Benutzermodus in den Kernelmodus in Microsoft Windows so selten wie möglich erfolgt.

Der Befehlspuffer wird geleert, wodurch ein Benutzer-/Kernelmoduswechsel in einer von vier Situationen verursacht wird, die wie folgt aussehen.

1.  [**Present**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) wird aufgerufen.
2.  [**ID3D10Device::Flush**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-flush) wird aufgerufen.
3.  Der Befehlspuffer ist voll. Seine Größe ist dynamisch und wird vom Betriebssystem und dem Grafiktreiber gesteuert.
4.  Die CPU erfordert Zugriff auf die Ergebnisse eines Befehls, der auf die Ausführung im Befehlspuffer wartet.

Von den vier oben genannten Situationen ist Nummer vier die wichtigste Für die Leistung. Wenn die Anwendung einen [**ID3D10Device::CopyResource-**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) oder [**ID3D10Device::CopySubresourceRegion-Aufruf**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) ausgibt, wird dieser Aufruf im Befehlspuffer in die Warteschlange eingereiht. Wenn die Anwendung dann versucht, die Stagingressource zuzuordnen, die das Ziel des Kopieraufrufs war, bevor der Befehlspuffer geleert wurde, tritt ein Pipelinefehler auf, da nicht nur der Copy-Methodenaufruf ausgeführt werden muss, sondern auch alle anderen gepufferten Befehle im Befehlspuffer ausgeführt werden müssen. Dies führt dazu, dass gpu und CPU synchronisiert werden, da die CPU auf den Zugriff auf die Stagingressource wartet, während die GPU den Befehlspuffer leert und schließlich die Ressource auffüllt, die die CPU benötigt. Sobald die GPU die Kopie abgeschlossen hat, beginnt die CPU mit dem Zugriff auf die Stagingressource, während dieser Zeit befindet sich die GPU jedoch im Leerlauf.

Wenn Sie dies zur Laufzeit häufig tun, wird die Leistung erheblich beeinträchtigt. Aus diesem Grund sollte die Zuordnung von Ressourcen, die mit der Standardnutzung erstellt wurden, mit Vorsicht erfolgen. Die Anwendung muss lange genug warten, bis der Befehlspuffer geleert wurde, und daher muss die Ausführung aller dieser Befehle abgeschlossen sein, bevor versucht wird, die entsprechende Stagingressource zuzuordnen. Wie lange sollte die Anwendung warten? Mindestens zwei Frames, da dadurch die Parallelität zwischen cpu(s) und GPU maximal genutzt werden kann. Während die Anwendung Frame N verarbeitet, indem Aufrufe an den Befehlspuffer übermittelt werden, ist die GPU mit der Ausführung der Aufrufe aus dem vorherigen Frame N-1 ausgelastet.

Wenn eine Anwendung also eine Ressource zuordnen möchte, die aus dem Videospeicher stammt und [**ID3D10Device::CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) oder [**ID3D10Device::CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) in Frame N aufruft, beginnt dieser Aufruf tatsächlich mit der Ausführung bei Frame N+1, wenn die Anwendung Aufrufe für den nächsten Frame übermittelt. Die Kopie sollte abgeschlossen sein, wenn die Anwendung Frame N+2 verarbeitet.



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
<li>CPU-Probleme rendern Aufrufe für den aktuellen Frame.</li>
</ul></td>
</tr>
<tr class="even">
<td>N+1</td>
<td><ul>
<li>GPU, die Aufrufe ausführt, die von der CPU während Frame N gesendet werden.</li>
<li>CPU-Probleme rendern Aufrufe für den aktuellen Frame.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N+2</td>
<td><ul>
<li>GPU hat die Ausführung von Aufrufen abgeschlossen, die während frame N von der CPU gesendet wurden. Ergebnisse sind bereit.</li>
<li>GPU, die Aufrufe ausführt, die von der CPU während Frame N+1 gesendet werden.</li>
<li>CPU-Probleme rendern Aufrufe für den aktuellen Frame.</li>
</ul></td>
</tr>
<tr class="even">
<td>N+3</td>
<td><ul>
<li>GPU hat die Ausführung von Aufrufen abgeschlossen, die von der CPU während Frame N+1 gesendet wurden. Ergebnisse bereit.</li>
<li>GPU, die Aufrufe ausführt, die von der CPU während Frame N+2 gesendet werden.</li>
<li>CPU-Probleme rendern Aufrufe für den aktuellen Frame.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N+4</td>
<td>...</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
