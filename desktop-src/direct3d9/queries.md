---
description: Es gibt mehrere Arten von Abfragen, die zum Abfragen des Status von Ressourcen entwickelt wurden.
ms.assetid: 2c65d199-141d-43a7-b513-4cb4459d7c27
title: Abfragen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2113500673def3e2cca5816e534b567a29fc322fb51f853db98eada20ba62674
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068994"
---
# <a name="queries-direct3d-9"></a>Abfragen (Direct3D 9)

Es gibt mehrere Arten von Abfragen, die zum Abfragen des Status von Ressourcen entwickelt wurden. Der Status einer bestimmten Ressource umfasst den GPU-Status (Graphics Processing Unit), den Treiberstatus oder den Laufzeitstatus. Um den Unterschied zwischen den verschiedenen Abfragetypen zu verstehen, müssen Sie die Abfragezustände verstehen. Im folgenden Zustandsübergangsdiagramm werden die einzelnen Abfragezustände erläutert.

![Diagramm mit Übergängen zwischen Abfragezuständen](images/queries.png)

Das Diagramm zeigt drei Zustände, die jeweils durch Kreise definiert sind. Jede der soliden Linien sind anwendungsgesteuerte Ereignisse, die einen Zustandsübergang verursachen. Die gestrichelte Linie ist ein ressourcengesteuertes Ereignis, bei dem eine Abfrage vom zustandsgesteuerten Zustand in den signalisierten Zustand wechselt. Jeder dieser Zustände hat einen anderen Zweck:

-   Der signalisierte Zustand ist wie ein Leerlaufzustand. Das Abfrageobjekt wurde generiert und wartet darauf, dass die Anwendung die Abfrage aus gibt. Nachdem eine Abfrage abgeschlossen und wieder in den signalisierten Zustand überwechselt wurde, kann die Antwort auf die Abfrage abgerufen werden.
-   Der Gebäudezustand ist wie ein Stagingbereich für eine Abfrage. Vom Gebäudezustand aus wurde eine Abfrage ausgegeben (durch Aufrufen von [**D3DISSUE \_ BEGIN),**](d3dissue-begin.md)aber noch nicht in den Zustand ausgestellt. Wenn eine Anwendung ein Abfrageende aus gibt (durch Aufrufen [**von D3DISSUE \_ END),**](d3dissue-end.md)geht die Abfrage in den Zustand ausgestellt über.
-   Der Status Ausgestellt bedeutet, dass die abgefragte Ressource die Kontrolle über die Abfrage hat. Sobald die Ressource ihre Arbeit abgeschlossen hat, geht die Ressource den Zustandscomputer in den signalisierten Zustand über. Während des Status "Ausgestellt" muss die Anwendung eine Abfrage senden, um den Übergang in den signalisierten Zustand zu erkennen. Sobald der Übergang in den signalisierten Zustand erfolgt ist, gibt [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) das Abfrageergebnis (über ein Argument) an die Anwendung zurück.

In der folgenden Tabelle sind die verfügbaren Abfragetypen aufgeführt.



| Abfragetyp        | Problemereignis                                                                      | GetData-Puffer                                                              | Runtime      | Impliziter Anfang der Abfrage                      |
|-------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------|--------------|--------------------------------------------------|
| BANDWIDTHTIMINGS  | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9BANDWIDTHTIMINGS**](d3ddevinfo-d3d9bandwidthtimings.md) | Einzelhandel/Debuggen | Nicht zutreffend                                              |
| CACHEUTILIZATION  | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9CACHEUTILIZATION**](d3ddevinfo-d3d9cacheutilization.md) | Einzelhandel/Debuggen | Nicht zutreffend                                              |
| EREIGNIS             | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | BOOL                                                                        | Einzelhandel/Debuggen | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| INTERFACETIMINGS  | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9INTERFACETIMINGS**](d3ddevinfo-d3d9interfacetimings.md) | Einzelhandel/Debuggen | Nicht zutreffend                                              |
| Okklusion         | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | DWORD                                                                       | Einzelhandel/Debuggen | Nicht zutreffend                                              |
| PIPELINETIMINGS   | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9PIPELINETIMINGS**](d3ddevinfo-d3d9pipelinetimings.md)   | Einzelhandel/Debuggen | Nicht zutreffend                                              |
| Resourcemanager   | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ ResourceManager**](d3ddevinfo-resourcemanager.md)           | Nur Debuggen   | [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| timestamp         | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | UINT64                                                                      | Einzelhandel/Debuggen | Nicht zutreffend                                              |
| TIMESTAMPDISJOINT | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | BOOL                                                                        | Einzelhandel/Debuggen | Nicht zutreffend                                              |
| TIMESTAMPFREQ     | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | UINT64                                                                      | Einzelhandel/Debuggen | Nicht zutreffend                                              |
| Vcache            | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ VCACHE**](d3ddevinfo-vcache.md)                             | Einzelhandel/Debuggen | [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) |
| VERTEXSTATS       | [**D3DISSUE \_ END**](d3dissue-end.md)                                            | [**D3DDEVINFO \_ D3DVERTEXSTATS**](d3ddevinfo-d3dvertexstats.md)             | Nur Debuggen   | [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)     |
| VERTEXTIMINGS     | [**D3DISSUE \_ BEGIN,**](d3dissue-begin.md) [ **D3DISSUE \_ END**](d3dissue-end.md) | [**D3DDEVINFO \_ D3D9STAGETIMINGS**](d3ddevinfo-d3d9stagetimings.md)         | Einzelhandel/Debuggen | Nicht zutreffend                                              |



 

Einige abfragen erfordern ein Begin- und Endereignis, während andere nur ein Endereignis erfordern. Die Abfragen, die nur ein Endereignis erfordern, beginnen, wenn ein anderes implizites Ereignis auftritt (das in der Tabelle aufgeführt ist). Alle Abfragen geben eine Antwort zurück, mit Ausnahme der Ereignisabfrage, deren Antwort immer **TRUE ist.** Eine Anwendung verwendet entweder den Status der Abfrage oder den Rückgabecode von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata).

## <a name="create-a-query"></a>Erstellen einer Abfrage

Bevor Sie eine Abfrage erstellen, können Sie überprüfen, ob die Laufzeit Abfragen unterstützt, indem Sie [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) mit einem **NULL-Zeiger** wie dem folgenden aufrufen:


```
IDirect3DQuery9* pEventQuery;

// Create a device pointer m_pd3dDevice

// Create a query object
HRESULT hr = m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, NULL);
```



Diese Methode gibt einen Erfolgscode zurück, wenn eine Abfrage erstellt werden kann. Andernfalls wird ein Fehlercode zurückgegeben. Sobald [**CreateQuery**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery) erfolgreich ist, können Sie ein Abfrageobjekt wie folgt erstellen:


```
IDirect3DQuery9* pEventQuery;
m_pd3dDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);
```



Wenn dieser Aufruf erfolgreich ist, wird ein Abfrageobjekt erstellt. Die Abfrage befindet sich im Wesentlichen im Leerlauf im signalisierten Zustand (mit einer nicht initialisierten Antwort), die auf die Ausgabe wartet. Wenn Sie die Abfrage abgeschlossen haben, geben Sie sie wie jede andere Schnittstelle frei.

## <a name="issue-a-query"></a>Ausstellen einer Abfrage

Eine Anwendung ändert einen Abfragezustand, indem sie eine Abfrage ausgibt. Hier sehen Sie ein Beispiel für die Ausgabe einer Abfrage:


```
IDirect3DQuery9* pEventQuery;
m_pD3DDevice->CreateQuery(D3DQUERYTYPE_EVENT, &pEventQuery);

// Issue a Begin event
pEventQuery->Issue(D3DISSUE_BEGIN);

or

// Issue an End event
pEventQuery->Issue(D3DISSUE_END);
```



Eine Abfrage im signalisierten Zustand geht wie folgt über, wenn sie ausgegeben wird:



| Problemtyp                                | Abfrageübergänge zu . . . |
|-------------------------------------------|--------------------------------|
| [**D3DISSUE \_ BEGIN**](d3dissue-begin.md) | Erstellungsstatus.                |
| [**D3DISSUE \_ END**](d3dissue-end.md)     | Ausgestellter Zustand.                  |



 

Eine Abfrage im Gebäudezustand geht wie folgt über, wenn sie ausgegeben wird:



| Problemtyp                                | Abfrageübergänge zu . . .                                            |
|-------------------------------------------|---------------------------------------------------------------------------|
| [**D3DISSUE \_ BEGIN**](d3dissue-begin.md) | (Kein Übergang, verbleibt im Gebäudezustand. Startet die Abfrageklammer neu.) |
| [**D3DISSUE \_ END**](d3dissue-end.md)     | Ausgestellter Zustand.                                                             |



 

Eine Abfrage im Zustand "Ausgestellt" geht wie folgt über, wenn sie ausgegeben wird:



| Problemtyp                                | Abfrageübergänge zu . . .                    |
|-------------------------------------------|---------------------------------------------------|
| [**D3DISSUE \_ BEGIN**](d3dissue-begin.md) | Erstellen des Zustands und Neustarten der Abfrageklammer.    |
| [**D3DISSUE \_ END**](d3dissue-end.md)     | Ausgestellter Zustand nach dem Abbrechen der vorhandenen Abfrage. |



 

## <a name="check-the-query-state-and-get-the-answer-to-the-query"></a>Überprüfen des Abfragestatus und Abrufen der Antwort auf die Abfrage

[**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) führt zwei Dinge aus:

1.  Gibt den Abfragezustand im Rückgabecode zurück.
2.  Gibt die Antwort auf die Abfrage in *pData* zurück.

Aus jedem der drei Abfragezustände finden [**Sie**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) hier die GetData-Rückgabecodes:



| Abfragestatus | GetData-Rückgabecode |
|-------------|---------------------|
| Signalisiert    | S \_ OK               |
| Erstellen    | Fehlercode          |
| Ausgestellt      | S \_ FALSE            |



 

Wenn sich beispielsweise eine Abfrage im Zustand "Ausgestellt" befindet und die Antwort auf die Abfrage nicht verfügbar ist, gibt [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) S \_ FALSE zurück. Wenn die Ressource ihre Arbeit beendet und die Anwendung ein Abfrageende ausgegeben hat, geht die Ressource in den signalisierten Zustand über. Vom signalisierten Zustand gibt **GetData** S \_ OK zurück, was bedeutet, dass die Antwort auf die Abfrage auch in *pData* zurückgegeben wird. Hier ist beispielsweise die Sequenz von Ereignissen angegeben, um die Anzahl der in einer Rendersequenz gezeichneten Pixel zurückzugeben:

-   Erstellen der Abfrage
-   Ein Startereignis ausstellen.
-   Zeichnen Sie etwas.
-   Ein Endereignis ausstellen.

Im Folgenden ist die entsprechende Codesequenz angegeben:


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



Diese Codezeilen erledigen mehrere Dinge:

-   Rufen [**Sie GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) auf, um die Anzahl der gezeichneten Pixel zurückzugeben.
-   Geben Sie [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md) an, damit die Ressource die Abfrage in den signalisierten Zustand übergehen kann.
-   Fragen Sie die Abfrageressource ab, indem [**Sie GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) aus einer Schleife aufrufen. Solange **GetData** S \_ FALSE zurückgibt, bedeutet dies, dass die Ressource die Antwort noch nicht zurückgegeben hat.

Der Rückgabewert von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) teilt Ihnen im Wesentlichen mit, in welchem Zustand sich die Abfrage befindet. Mögliche Werte sind S \_ OK, S \_ FALSE und ein Fehler. Rufen **Sie GetData** nicht für eine Abfrage auf, die sich im Erstellungszustand befindet.

-   S \_ OK bedeutet, dass die Ressource (GPU, Treiber oder Runtime) abgeschlossen ist. Die Abfrage kehrt in den signalisierten Zustand zurück. Die Antwort (sofern vorhanden) wird von [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)zurückgegeben.
-   S \_ FALSE bedeutet, dass die Ressource (GPU, Treiber oder Laufzeit) noch keine Antwort zurückgeben kann. Dies kann daran liegt, dass die GPU nicht abgeschlossen ist oder die Arbeit noch nicht angezeigt wurde.
-   Ein Fehler bedeutet, dass die Abfrage einen Fehler generiert hat, von dem sie nicht wiederhergestellt werden kann. Dies kann der Fall sein, wenn das Gerät während einer Abfrage verloren geht. Sobald eine Abfrage einen Fehler generiert hat (mit Ausnahme von S \_ FALSE), muss die Abfrage neu erstellt werden, wodurch die Abfragesequenz aus dem signalisierten Zustand neu gestartet wird.

Anstatt [**D3DGETDATA \_ FLUSH**](d3dgetdata-flush.md)anzugeben, die aktuellere Informationen bereitstellt, können Sie 0 (null) angeben. Dies ist eine einfachere Überprüfung, wenn sich die Abfrage im ausgegebenen Zustand befindet. Die Bereitstellung von 0 führt dazu, dass [**GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) den Befehlspuffer nicht leert. Aus diesem Grund muss darauf geachtet werden, dass keine schleifendefiniert sind (weitere Informationen finden Sie unter **GetData).** Da die Laufzeit Arbeit im Befehlspuffer in die Warteschlange einreiht, ist **D3DGETDATA \_ FLUSH** ein Mechanismus zum Leeren des Befehlspuffers an den Treiber (und somit die GPU; siehe [Genaue Profilerstellung für Direct3D-API-Aufrufe (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). Während der Befehlspufferlöschung kann eine Abfrage in den signalisierten Zustand übergehen.

## <a name="example-an-event-query"></a>Beispiel: Eine Ereignisabfrage

Eine Ereignisabfrage unterstützt kein Startereignis.

-   Erstellen der Abfrage
-   Ein Endereignis ausstellen.
-   Fragt ab, bis sich die GPU im Leerlauf befindet.
-   Ein Endereignis ausstellen.


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



Dies ist die Sequenz von Befehlen, die von einer Ereignisabfrage zum Profilieren von API-Aufrufen (Application Programming Interface) verwendet werden (siehe [Genaue Profilerstellung für Direct3D-API-Aufrufe (Direct3D 9)](accurately-profiling-direct3d-api-calls.md)). Diese Sequenz verwendet Marker, um die Arbeitsmenge im Befehlspuffer zu steuern.

Beachten Sie, dass Anwendungen besonders auf die hohen Kosten achten sollten, die mit dem Leeren des Befehlspuffers verbunden sind, da dies dazu führt, dass das Betriebssystem in den Kernelmodus wechselt, was zu erheblichen Leistungseinbußen führt. Anwendungen sollten auch die Auslastung von CPU-Zyklen beachten, indem sie auf den Abschluss von Abfragen warten.

Abfragen sind eine Optimierung, die während des Renderings verwendet werden soll, um die Leistung zu erhöhen. Daher ist es nicht vorteilhaft, auf den Abschluss einer Abfrage zu warten. Wenn eine Abfrage ausgegeben wird und die Ergebnisse zum Zeitpunkt der Anwendungsüberprüfung noch nicht bereit sind, war der Optimierungsversuch nicht erfolgreich, und das Rendering sollte normal fortgesetzt werden.

Das klassische Beispiel hierfür ist occlusion Culling. Anstelle der  obigen while-Schleife kann eine Anwendung, die Abfragen verwendet, Okklusions-Culling implementieren, um zu überprüfen, ob eine Abfrage abgeschlossen war, bis sie das Ergebnis benötigt. Wenn die Abfrage nicht abgeschlossen ist, fahren Sie (im schlimmsten Fall) so fort, als ob das objekt, für das getestet wird, nicht verdeckt (d. h. es ist sichtbar) ist, und rendern Sie es. Der Code sieht in etwa wie folgt aus.


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

[Weiterführende Themen](advanced-topics.md)
</dt> </dl>

 

 
