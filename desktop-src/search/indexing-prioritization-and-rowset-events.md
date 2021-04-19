---
description: Enthält eine Übersicht über die Einführung der Indizierungs Priorisierung und der rowsetereignisse für Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: Indizieren von Priorisierungs-und rowsetereignissen in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6610500a3c2fcd359f346e5239507fb15ad896d
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106366357"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a>Indizieren von Priorisierungs-und rowsetereignissen in Windows 7

In diesem Thema wird die Einführung der Indizierungs Priorisierung und der rowsetereignisse für Windows 7 beschrieben.

Dieses Thema ist wie folgt organisiert:

-   [Indizieren von Priorisierung und rowsetereignissen](#indexing-prioritization-and-rowset-events)
    -   [Irowsetpriorization-Beispiele](#irowsetpriorization-examples)
    -   [Irowsetpriorisierungsereignisse](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a>Indizieren von Priorisierung und rowsetereignissen

In Windows 7? und höher gibt es einen Prioritäts Stapel, in dem der Kontext einer bestimmten Abfrage den Client anfordern kann, dass die in dieser Abfrage verwendeten Bereiche priorisiert werden, die mit den normalen Elementen priorisiert sind.

Dieser Priorisierungs Stapel hat die folgenden Eigenschaften:

-   Elemente im Stapel können die Priorität "Vordergrund", "hoch" oder "niedrig" aufweisen:
    -   **Vordergrund**: Backoff-Logik wird übersprungen, und die Indizierung verläuft so schnell, wie der Computer zulässt.
    -   **Hoch**: Priorisierung wurde mit Backoff angefordert.
    -   **Niedrig**: Es wurde eine Priorisierung angefordert, nicht auf Kosten anderer Bereiche im Stapel, sondern oberhalb der Indizierung ohne Priorität.
-   Jede Anforderung für hohe oder Vordergrund Priorität bestößt die anfordernde Abfrage automatisch am Anfang des Stapels.
-   Nur das Element oben im Stapel kann eine Vordergrund Priorität haben.
-   Eine Abfrage mit Vordergrund Priorität, die bei Priorität nach unten gesetzt wird, empfängt ein Ereignis, das die Vordergrund Priorität verliert und mit einem Backoff zu einer hohen Priorität geworden ist.

Der Prioritäts Stapel legt eine Gesamt Priorität von Elementen fest, die im Indexer wie folgt verarbeitet werden:

-   Benachrichtigungen mit hoher Priorität verfügen über keinen Backoff und werden in der Regel nur für eine kleine Anzahl von Elementen gesendet. Windows-Explorer verwendet diese Priorität z. b. bei kleinen Kopier-Engine-Vorgängen.
-   Der Prioritäts Stapel ist der obere Rand des Stapels, verfügt über einen Backoff und ist die zuletzt angeforderte Prioritäts Abfrage.
-   Zweite Abfrage im Stapel.
-   Dritte Abfrage im Stapel.
-   Vierte Abfrage im Stapel usw.
-   Elemente mit normaler Priorität.
-   Gelöschte Elemente.
    > [!Note]  
    > Elemente in jeder Gruppe werden intern durch die ältere Semantik pro Element priorisiert.

     

### <a name="irowsetpriorization-examples"></a>Irowsetpriorization-Beispiele

Die primäre API für Priorisierungs arbeiten ist über die folgende Schnittstelle verfügbar, die durch Abfragen des zurückgegebenen Rowsets aufgerufen werden kann:


```
typedef [v1_enum] enum
{
    PRIORITY_LEVEL_FOREGROUND           = 0,    // process items in the scope first as quickly as possible
    PRIORITY_LEVEL_HIGH                 = 1,    // process items in the scope first at the normal rate
    PRIORITY_LEVEL_LOW                  = 2,    // process items in this scope before those at the normal rate, but after any other prioritization requests
    PRIORITY_LEVEL_DEFAULT              = 3     // process items at the normal indexer rate
} PRIORITY_LEVEL;


[
    object,
    uuid(IRowsetPrioritization_GUID),
    pointer_default(unique)
]
interface IRowsetPrioritization : IUnknown
{
    // Sets or retrieves the current indexer prioritization level for the scope specified by
    // this query.

    HRESULT SetScopePriority( [in] PRIORITY_LEVEL priority, [in] DWORD scopeStatisticsEventFrequency );
    HRESULT GetScopePriority( [out] PRIORITY_LEVEL * priority, [out] DWORD * scopeStatisticsEventFrequency );

    // Gets information describing the scope specified by this query:
    // indexedDocumentCount     -   The total number of documents currently indexed in the scope
    // oustandingAddCount       -   The total number of documents yet to be indexed in the scope (those not yet included in indexedDocumentCount)
    // oustandingModifyCount    -   The total number of documents indexed in the scope that need to be re-indexed (included in indexedDocumentCount)
    
    HRESULT GetScopeStatistics( [out] DWORD * indexedDocumentCount, [out] DWORD * oustandingAddCount, [out] DWORD * oustandingModifyCount );
};
```



Die rowsetpriorisierung funktioniert wie folgt:

1.  [**Irowsetpriorisierung**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) wird mit der [IUnknown:: QueryInterface-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein Indexer-Rowset abgerufen. **DBPROP \_ Enablerowsetevents** muss mit der OLE DB [ICommandProperties:: SetProperties](/previous-versions/windows/desktop/ms711497(v=vs.85)) -Methode auf " **true** " festgelegt werden, bevor die Abfrage ausgeführt wird, um die rowsetpriorisierung zu verwenden.
2.  [**Irowsetprioritisierung:: setscopepriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) legt die Priorisierung für die Bereiche fest, die der Abfrage angehören, und das Intervall, das das Bereichs Statistik Ereignis ausgelöst wird, wenn ausstehende Dokumente innerhalb der Abfrage Bereiche indiziert werden müssen. Dieses Ereignis wird ausgelöst, wenn die Prioritätsstufe auf Default festgelegt ist.
3.  [**Irowsetprioritisierung:: getscopestatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) kann verwendet werden, um die Anzahl der indizierten Elemente im Bereich, die Anzahl der ausstehenden Dokumente, die dem Bereich hinzugefügt werden sollen, und die Anzahl der Dokumente, die in diesem Bereich neu indiziert werden müssen, zu erhalten.

### <a name="irowsetprioritization-events"></a>Irowsetpriorisierungsereignisse

Es gibt drei rowsetereignisse in [**irowsetevents:: onrowsetevent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) in der [**RowSetEvent- \_ Typenumeration**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type) :


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



Die rowsetereignisse lauten wie folgt:

-   Das Ereignis **RowSetEvent \_ Type \_ dataabgelaufgibt** an, dass Daten, die das Rowset unterstützen, abgelaufen sind und dass ein neues Rowset angefordert werden sollte.
-   Das Ereignis " **\_ \_ foregroundlost" des rowsettyps** gibt an, dass ein Element mit der Vordergrund Priorität im Priorisierungs Stapel herabgestuft wurde, da sich eine andere Person vor dieser Abfrage selbst priorisiert hat.
-   Das Ereignis **RowSetEvent \_ Type \_ scopestatistics** bietet Ihnen die gleichen Informationen, die über den [**irowsetprioritisierung:: getscopestatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) -Methodenaufrufe verfügbar sind, aber über einen Push-Mechaniker wie folgt:
    -   Das Ereignis tritt auf, wenn die Priorisierungs-API verwendet wurde, um eine nicht standardmäßige Priorisierungs Ebene und eine Statistik Ereignis Häufigkeit ungleich NULL anzufordern.
    -   Das Ereignis tritt nur auf, wenn Statistiken tatsächlich geändert werden und das in [**irowsetpriorisierung**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) angegebene Intervall abgelaufen ist (das Intervall garantiert nicht die Häufigkeit des Ereignisses).
    -   Dieses Ereignis stellt sicher, dass der Status "Sprung 0" (null Elemente, die noch nicht hinzugefügt werden müssen, 0 verbleibende modifizierungwerte) nicht ausgelöst wird, vorausgesetzt, dass ein Ereignis ungleich NULL ausgelöst wurde.
    -   Der Indexer kann Elemente verarbeiten, ohne dieses Ereignis zu senden, wenn die Warteschlange vor der Statistik Ereignis Häufigkeit entfernt wird.

## <a name="additional-resources"></a>Weitere Ressourcen

Sehen Sie sich die folgenden Ressourcen im Zusammenhang mit Priorisierung und Rowsets an:

-   Schnittstellen:
    -   [**IRow-tevents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [**Irowsetpriorisierung**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   Aufzählungen:
    -   [**Priorisieren von \_ Flags**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [**Prioritäts \_ Stufe**](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [**rowevent- \_ Ausdruck ItemState**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [**rowsertevent- \_ Typ**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows 7-Suche](./-search-3x-wds-overview.md)
</dt> <dt>

[Neu bei der Windows 7-Suche](new-for-windows-7-search.md)
</dt> <dt>

[Windows Shell-Bibliotheken in Windows 7](-search-win7-development-scenarios.md)
</dt> </dl>

 

 