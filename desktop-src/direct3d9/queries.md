---
description: Es gibt mehrere Typen von Abfragen, die zum Abfragen des Status von Ressourcen entworfen wurden.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Abfragen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f450aa7015d4b66ad28b6c4d0632b2995bedd7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859974"
---
# <a name="queries-direct3d-9"></a>Abfragen (Direct3D 9)

Es gibt mehrere Typen von Abfragen, die zum Abfragen des Status von Ressourcen entworfen wurden. Der Status einer bestimmten Ressource umfasst den GPU-Status (Graphics Processing Unit), den Treiber Status oder den Lauf Zeit Status. Um den Unterschied zwischen den unterschiedlichen Abfrage Typen zu verstehen, müssen Sie die Abfrage Zustände verstehen. Im folgenden Zustands Übergangs Diagramm werden die einzelnen Abfrage Zustände erläutert.

![Diagramm zur Darstellung von Übergängen zwischen Abfrage Zuständen](images/queries.png)

Das Diagramm zeigt drei Zustände, die jeweils durch Kreise definiert werden. Jede der vollwertigen Linien sind Anwendungs gesteuerte Ereignisse, die einen Zustandsübergang verursachen. Die gestrichelte Linie ist ein Ressourcen gesteuertes Ereignis, das eine Abfrage aus dem ausgestellten Zustand in den signalisierten Zustand wechselt. Jeder dieser Zustände hat einen anderen Zweck:

-   Der Status "signalisiert" ähnelt einem Leerlaufzustand. Das Query-Objekt wurde generiert und wartet darauf, dass die Anwendung die Abfrage ausgibt. Nachdem eine Abfrage abgeschlossen und in den signalisierten Zustand umgestellt wurde, kann die Antwort auf die Abfrage abgerufen werden.
-   Der erstellungstatus ist wie ein Stagingbereich für eine Abfrage. Aus dem Erteilungs Status wurde eine Abfrage ausgegeben (durch Aufrufen von [**D3DISSUE \_ Begin**](d3dissue-begin.md)), hat sich jedoch noch nicht in den ausgestellten Zustand versetzt. Wenn eine Anwendung ein Abfrage Ende ausgibt (durch Aufrufen von [**D3DISSUE \_ End**](d3dissue-end.md)), wechselt die Abfrage in den ausgegebene Zustand.
-   Der ausgegebene Zustand bedeutet, dass die Abfrage, die abgefragt wird, die Abfrage steuert. Sobald die Ressource abgeschlossen ist, überträgt die Ressource den Zustands Automat in den signalisierten Zustand. Während des ausgestellten Zustands muss die Anwendung Abfragen, um den Übergang in den signalisierten Zustand zu erkennen. Nachdem der Übergang in den signalisierten Zustand erfolgt ist, gibt [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) das Abfrageergebnis (über ein Argument) an die Anwendung zurück.

In der folgenden Tabelle sind die verfügbaren Abfrage Typen aufgelistet.



| Abfragetyp        | Problem Ereignis                                                                      | GetData-Puffer                                                              | Typ      | Impliziter Beginn der Abfrage                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| Bandwidthtimings  | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**](d3ddevinfo-d3d9bandwidthtimings.md) | Retail/Debug | –                                              |
| Cacheutilization  | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9CACHEUTILIZATION**](d3ddevinfo-d3d9cacheutilization.md) | Retail/Debug | –                                              |
| EREIGNIS             | [**D3DISSUE \_ Ende**](d3dissue-end.md)                                            | BOOL                                                                        | Retail/Debug | [**"Kreatedevice"**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| Interfacetimings  | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9INTERFACETIMINGS**](d3ddevinfo-d3d9interfacetimings.md) | Retail/Debug | –                                              |
| Okklusions         | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | DWORD                                                                       | Retail/Debug | –                                              |
| Pipelinetimings   | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9PIPELINETIMINGS**](d3ddevinfo-d3d9pipelinetimings.md)   | Retail/Debug | –                                              |
| RESOURCEMANAGER   | [**D3DISSUE \_ Ende**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md)           | Nur Debuggen   | [**Anzahl**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| timestamp         | [**D3DISSUE \_ Ende**](d3dissue-end.md)                                            | UINT64                                                                      | Retail/Debug | –                                              |
| Timestampdisjoint | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | BOOL                                                                        | Retail/Debug | –                                              |
| Timestampfreq     | [**D3DISSUE \_ Ende**](d3dissue-end.md)                                            | UINT64                                                                      | Retail/Debug | –                                              |
| VCACHE            | [**D3DISSUE \_ Ende**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ VCACHE**](d3ddevinfo-vcache.md)                             | Retail/Debug | [**"Kreatedevice"**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| Vertexstats       | [**D3DISSUE \_ Ende**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ D3DVERTEXSTATS**](d3ddevinfo-d3dvertexstats.md)             | Nur Debuggen   | [**Anzahl**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| Vertextierungen     | [**D3DISSUE \_ BEGIN**](d3dissue-begin.md), [ **D3DISSUE \_ End**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9STAGETIMINGS**](d3ddevinfo-d3d9stagetimings.md)         | Retail/Debug | –                                              |



 

Einige Abfragen erfordern ein Begin-und End-Ereignis, während andere nur ein End-Ereignis benötigen. Die Abfragen, die nur ein End-Ereignis erfordern, beginnen, wenn ein anderes impliziertes Ereignis auftritt (das in der Tabelle aufgelistet ist). Alle Abfragen geben eine Antwort zurück, mit Ausnahme der Ereignis Abfrage, deren Antwort immer " **true**" ist. Eine Anwendung verwendet entweder den Status der Abfrage oder den Rückgabecode von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).

## <a name="create-a-query"></a>Erstellen einer Abfrage

Bevor Sie eine Abfrage erstellen, können Sie überprüfen, ob die Laufzeit Abfragen unterstützt, indem Sie [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) mit einem **null** -Zeiger wie dem folgenden aufrufen:


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



Diese Methode gibt einen Erfolgs Code zurück, wenn eine Abfrage erstellt werden kann. Andernfalls wird ein Fehlercode zurückgegeben. Nach erfolgreicher Ausführung von " [**kreatequery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) " können Sie ein Abfrageobjekt wie folgt erstellen:


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



Wenn dieser Befehl erfolgreich ausgeführt wird, wird ein Abfrageobjekt erstellt. Die Abfrage befindet sich im Wesentlichen im Zustand "signalisiert" im Zustand "signalisiert" (mit einer nicht initialisierten Antwort) und wartet auf die Ausstellung. Wenn Sie mit der Abfrage fertig sind, geben Sie Sie wie jede andere Schnittstelle frei.

## <a name="issue-a-query"></a>Ausstellen einer Abfrage

Eine Anwendung ändert einen Abfrage Zustand, indem eine Abfrage ausgegeben wird. Im folgenden finden Sie ein Beispiel für die Ausgabe einer Abfrage:


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



Eine Abfrage im signalisierten Zustand geht wie folgt vor, wenn Sie ausgestellt wird:



| Problemtyp                                | Die Abfrage wechselt zum. . . |
|-------------------------------------------|--------------------------------|
| [**D3DISSUE \_ Begin**](d3dissue-begin.md) | Der Status wird aufgebaut.                |
| [**D3DISSUE \_ Ende**](d3dissue-end.md)     | Ausgegebener Zustand.                  |



 

Eine Abfrage im Erstellungs Status geht wie folgt vor, wenn Sie ausgestellt wird:



| Problemtyp                                | Die Abfrage wechselt zum. . .                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [**D3DISSUE \_ Begin**](d3dissue-begin.md) | (Kein Übergang, bleibt im Erstellungs Status. Startet die Abfrage Klammer neu.) |
| [**D3DISSUE \_ Ende**](d3dissue-end.md)     | Ausgegebener Zustand.                                                             |



 

Eine Abfrage im ausgestellten Status wird wie folgt ausgeführt, wenn Sie ausgestellt wird:



| Problemtyp                                | Die Abfrage wechselt zum. . .                    |
|-------------------------------------------|---------------------------------------------------|
| [**D3DISSUE \_ Begin**](d3dissue-begin.md) | Der Status wird erstellt, und die Abfrage Klammer wird neu gestartet.    |
| [**D3DISSUE \_ Ende**](d3dissue-end.md)     | Der Status wird nach dem verwerfen der vorhandenen Abfrage ausgegeben. |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a>Überprüfen Sie den Abfrage Status, und erhalten Sie die Antwort auf die Abfrage.

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) führt zwei Aufgaben aus:

1.  Gibt den Abfrage Status im Rückgabecode zurück.
2.  Gibt die Antwort auf die Abfrage in *pData* zurück.

Im folgenden werden die [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) -Rückgabecodes von den drei Abfrage Zuständen aufgeführt:



| Abfragestatus | GetData-Rückgabecode |
|-------------|---------------------|
| Ausgeschil    | S \_ OK               |
| Erstellen    | Fehlercode          |
| Ausgestellt      | S \_ false            |



 

Wenn eine Abfrage z. b. den ausgegebene Status aufweist und die Antwort auf die Abfrage nicht verfügbar ist, gibt [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) den Wert "false" zurück \_ . Wenn die Ressource die Arbeit beendet und die Anwendung ein Abfrage Ende ausgegeben hat, überträgt die Ressource die Abfrage in den signalisierten Zustand. Im signalisierten Zustand gibt **GetData** "S \_ OK" zurück. Dies bedeutet, dass die Antwort auf die Abfrage auch in " *pData*" zurückgegeben wird. Hier ist beispielsweise die Sequenz von Ereignissen, die die Anzahl der in einer Rendering-Sequenz gezeichneten Pixel zurückgibt:

-   Erstellen der Abfrage
-   Geben Sie ein Begin-Ereignis aus.
-   Zeichnen Sie etwas.
-   Geben Sie ein End-Ereignis aus.

Im folgenden finden Sie die entsprechende Code Sequenz:


```
IDirect3DQuery9* pOcclusionQuery;
DWORD numberOfPixelsDrawn;

m_pD3DDevice->CreateQuery(D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery);

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_BEGIN);

// API render loop
...
Draw(...)
...

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pOcclusionQuery->GetData( &numberOfPixelsDrawn, 
                                  sizeof(DWORD), D3DGETDATA_FLUSH ))
    ;
```



Diese Codezeilen führen verschiedene Aktionen aus:

-   Ruft [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) auf, um die Anzahl der gezeichneten Pixel zurückzugeben.
-   Geben Sie [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md) an, damit die Ressource die Abfrage in den signalisierten Zustand versetzen kann.
-   Rufen Sie die Abfrage Ressource durch Aufrufen von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) aus einer-Schleife ab. Solange **GetData** "S false" zurückgibt \_ , bedeutet dies, dass die Ressource die Antwort noch nicht zurückgegeben hat.

Der Rückgabewert von " [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) " weist im Wesentlichen darauf hin, in welchem Zustand die Abfrage ist. Mögliche Werte sind s \_ OK, s \_ false und ein Fehler. Ruft **GetData** nicht für eine Abfrage auf, die sich im Erstellungs Status befindet.

-   S \_ OK bedeutet, dass die Ressource (GPU oder Treiber oder Laufzeit) abgeschlossen ist. Die Abfrage wird in den signalisierten Zustand zurückversetzt. Die Antwort (sofern vorhanden) wird von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)zurückgegeben.
-   ' \_ False ' bedeutet, dass die Ressource (GPU oder Treiber oder Runtime) noch keine Antwort zurückgeben kann. Dies kann daran liegen, dass die GPU noch nicht abgeschlossen wurde oder die Arbeit noch nicht gesehen hat.
-   Ein Fehler bedeutet, dass die Abfrage einen Fehler generiert hat, von dem Sie nicht wieder hergestellt werden kann. Dies kann der Fall sein, wenn das Gerät während einer Abfrage verloren geht. Nachdem eine Abfrage einen Fehler generiert hat (außer S \_ false), muss die Abfrage neu erstellt werden, wodurch die Abfrage Sequenz aus dem signalisierten Zustand neu gestartet wird.

Anstatt [**D3DGETDATA \_ Flush**](d3dgetdata-flush.md)anzugeben, das aktuellere Informationen bereitstellt, können Sie NULL angeben. Dies ist eine genauere Überprüfung, wenn sich die Abfrage im ausgeführten Zustand befindet. Die Angabe von 0 (null) bewirkt, dass [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) den Befehls Puffer nicht leert. Aus diesem Grund muss sorgfältig vorgegangen werden, um die Endlosschleifen zu vermeiden (Weitere Informationen finden Sie unter **GetData** ). Da die Laufzeit im Befehls Puffer Aufgaben in die Warteschlange einreiht, ist **D3DGETDATA \_ Flush** ein Mechanismus zum Leeren des Befehls Puffers für den Treiber (und somit die GPU; siehe [exakte Profilerstellung Direct3D API-Aufrufe (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). Während der Leerung des Befehls Puffers kann eine Abfrage in den signalisierten Zustand übergehen.

## <a name="example-an-event-query"></a>Beispiel: eine Ereignis Abfrage

Ein Begin-Ereignis wird von einer Ereignis Abfrage nicht unterstützt.

-   Erstellen der Abfrage
-   Geben Sie ein End-Ereignis aus.
-   Ruft ab, bis sich die GPU im Leerlauf befindet.
-   Geben Sie ein End-Ereignis aus.


```
IDirect3DQuery9* pEventQuery = NULL;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;

... // API calls

// Add an end marker to the command buffer queue.
pEventQuery->Issue(D3DISSUE_END);

// Force the driver to execute the commands from the command buffer.
// Empty the command buffer and wait until the GPU is idle.
while(S_FALSE == pEventQuery->GetData( NULL, 0, D3DGETDATA_FLUSH ))
    ;
```



Dies ist die Sequenz von Befehlen, die von einer Ereignis Abfrage zum Erstellen von Profilen für API-Aufrufe (Application Programming Interface) verwendet werden (siehe [exakte Profilerstellung Direct3D API-Aufrufe (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). Diese Sequenz verwendet Marker, um den Arbeitsaufwand im Befehls Puffer zu steuern.

Beachten Sie, dass Anwendungen besonders auf die großen Kosten achten müssen, die mit dem leeren des Befehls Puffers verbunden sind, da dies dazu veranlasst, dass das Betriebssystem in den Kernel Modus wechselt und somit eine beträchtliche Leistungs Einbuße auftritt. Anwendungen sollten auch wissen, dass CPU-Zyklen verschwendet werden, indem auf den Abschluss von Abfragen gewartet wird.

Abfragen sind eine Optimierung, die beim Rendern verwendet wird, um die Leistung zu verbessern. Daher ist es nicht vorteilhaft, Zeit mit dem warten auf den Abschluss einer Abfrage zu warten. Wenn eine Abfrage ausgegeben wird und die Ergebnisse zu dem Zeitpunkt, zu dem Sie von der Anwendung überprüft wird, noch nicht bereit sind, konnte der Optimierungs Versuch nicht erfolgreich ausgeführt werden, und das Rendering sollte wie gewohnt fortgesetzt werden.

Das klassische Beispiel hierfür ist die Okklusion. Anstelle der obigen **while** -Schleife kann eine Anwendung, die Abfragen verwendet, die Okklusions-culsierung implementieren, um zu überprüfen, ob eine Abfrage zu dem Zeitpunkt abgeschlossen ist, zu dem das Ergebnis benötigt wird. Wenn die Abfrage noch nicht abgeschlossen wurde, fahren Sie (als Ungünstigster Fall Szenario) fort, als ob das Objekt, für das getestet wird, nicht verdeckt (d.h. sichtbar) ist, und Rendering Sie es. Der Code würde etwa wie folgt aussehen.


```
IDirect3DQuery9* pOcclusionQuery = NULL;
m_pD3DDevice->CreateQuery( D3DQUERYTYPE_OCCLUSION, &pOcclusionQuery );

// Add a begin marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_BEGIN );

... // API calls

// Add an end marker to the command buffer queue.
pOcclusionQuery->Issue( D3DISSUE_END );

// Avoid flushing and letting the CPU go idle by not using a while loop.
// Check if queries are finished:
DWORD dwOccluded = 0;
if( S_FALSE == pOcclusionQuery->GetData( &dwOccluded, sizeof(DWORD), 0 ) )
{
    // Query is not done yet or object not occluded; avoid flushing/wait by continuing with worst-case scenario
    pSomeComplexMesh->Render();
}
else if( dwOccluded != 0 )
{
    // Query is done and object is not occluded.
    pSomeComplexMesh->Render();
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Themen](advanced-topics.md)
</dt> </dl>

 

 
