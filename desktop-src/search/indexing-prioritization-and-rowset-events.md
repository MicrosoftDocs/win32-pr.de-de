---
description: Beschreibt die Einführung der Indizierungspriorisierung und von Rowsetereignissen für Windows 7.
ms.assetid: 6cdfb7d3-f849-432c-960f-912e5024c583
title: Indizieren von Priorisierungs- und Rowsetereignissen in Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92491300127c60ebdf2a265583fca77e77a09907b7f42b471f6d3d047a7f6aa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680501"
---
# <a name="indexing-prioritization-and-rowset-events-in-windows-7"></a>Indizieren von Priorisierungs- und Rowsetereignissen in Windows 7

In diesem Thema wird die Einführung von Indizierungspriorisierung und Rowsetereignissen für Windows 7 beschrieben.

Dieses Thema ist wie folgt organisiert:

-   [Indizieren von Priorisierungs- und Rowsetereignissen](#indexing-prioritization-and-rowset-events)
    -   [IRowsetPriorization-Beispiele](#irowsetpriorization-examples)
    -   [IRowsetPrioritization-Ereignisse](#indexing-prioritization-and-rowset-events-in-windows-7)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="indexing-prioritization-and-rowset-events"></a>Indizieren von Priorisierungs- und Rowsetereignissen

In Windows 7? und höher gibt es einen Prioritätsstapel, in dem der Kontext einer bestimmten Abfrage vom Client angefordert werden kann, dass die in dieser Abfrage verwendeten Bereiche über denen der normalen Elemente priorisiert werden.

Dieser Priorisierungsstapel weist die folgenden Merkmale auf:

-   Elemente im Stapel können vordergrund, hoch oder mit niedriger Priorität sein:
    -   **Vordergrund:** Die Backofflogik wird übersprungen, und die Indizierung wird so schnell fortgesetzt, wie der Computer dies zulässt.
    -   **Hoch:** Die Priorisierung wurde mit Backoff angefordert.
    -   **Niedrig:** Die Priorisierung wurde angefordert, nicht auf Kosten anderer Bereiche im Stapel, sondern oberhalb der nicht priorisierten Indizierung.
-   Jede Anforderung für hohe oder Vordergrundpriorität führt dazu, dass die anfordernde Abfrage automatisch am Anfang des Stapels angezeigt wird.
-   Nur das Element oben im Stapel kann eine Vordergrundpriorität haben.
-   Eine Abfrage mit Vordergrundpriorität, die in prioritätsbegrenzt ist, empfängt ein Ereignis, das sie darüber informiert, dass sie die Vordergrundpriorität verloren hat und mit Backoff zu einer hohen Priorität geworden ist.

Der Prioritätsstapel legt die Gesamtpriorität von Elementen fest, die im Indexer wie folgt verarbeitet werden:

-   Benachrichtigungen mit hoher Priorität haben kein Backoff und werden in der Regel nur für eine kleine Anzahl von Elementen gesendet. Beispielsweise verwendet Windows Explorer diese Priorität für kleine Kopiermodulvorgänge.
-   Prioritätsstapel befindet sich am Anfang des Stapels, verfügt über ein Backoff und ist die letzte angeforderte Prioritätsabfrage.
-   Zweite Abfrage im Stapel.
-   Dritte Abfrage im Stapel.
-   Vierte Abfrage im Stapel usw.
-   Normale Prioritätselemente.
-   Gelöschte Elemente.
    > [!Note]  
    > Elemente innerhalb jeder Gruppe werden intern über die ältere Semantik pro Element priorisiert.

     

### <a name="irowsetpriorization-examples"></a>IRowsetPriorization-Beispiele

Die primäre API für priorisierte Aufgaben ist über die folgende Schnittstelle verfügbar, die durch Abfragen des zurückgegebenen Rowsets aufgerufen werden kann:


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



Die Rowsetpriorisierung funktioniert wie folgt:

1.  [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) wird mit [der IUnknown::QueryInterface-Methode](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein Indexerrowset erworben. **DBPROP \_ ENABLEROWSETEVENTS** muss mit der OLE DB [ICommandProperties::SetProperties-Methode](/previous-versions/windows/desktop/ms711497(v=vs.85)) vor dem Ausführen der Abfrage auf **TRUE** festgelegt werden, damit die Rowsetpriorisierung verwendet werden kann.
2.  [**IRowsetPrioritization::SetScopePriority**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-setscopepriority) legt die Priorisierung für die Bereiche fest, die zur Abfrage gehören, und das Intervall, in dem das Bereichsstatistikereignis ausgelöst wird, wenn ausstehende Dokumente innerhalb der Abfragebereiche indiziert werden sollen. Dieses Ereignis wird ausgelöst, wenn die Prioritätsstufe auf den Standardwert festgelegt ist.
3.  [**IRowsetPrioritization::GetScopeStatistics**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) kann verwendet werden, um die Anzahl der indizierten Elemente im Bereich, die Anzahl der ausstehenden Dokumente, die dem Bereich hinzugefügt werden sollen, und die Anzahl der Dokumente abzurufen, die innerhalb dieses Bereichs neu indiziert werden müssen.

### <a name="irowsetprioritization-events"></a>IRowsetPrioritization-Ereignisse

Es gibt drei Rowsetereignisse in [**IRowsetEvents::OnRowsetEvent**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetevents-onrowsetevent) in der [**ROWSETEVENT \_ TYPE-Enumeration:**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)


```
    // This method allows for future notifications of various actions about your rowset or items within
    // eventType:                               - An identifier of the particular event being sent
    // pVarEventData:                           - The expected value of the EventData for each event type
    //      ROWSETEVENT_TYPE_DATAEXPIRED        - VT_EMPTY
    //      ROWSETEVENT_TYPE_FOREGROUNDLOST     - VT_EMPTY
    //      ROWSETEVENT_TYPE_SCOPESTATISTICS    - VT_VECTOR | VT_UI4 - 3 elements (0 = indexed items, 1 = outstanding adds, 2 = oustanding modifies)

    HRESULT OnRowsetEvent( [in] ROWSETEVENT_TYPE eventType, [in] REFPROPVARIANT eventData );
```



Die Rowsetereignisse sind wie folgt:

-   Das **ROWSETEVENT \_ TYPE \_ DATAEXPIRED-Ereignis** gibt an, dass die Daten, die das Rowset sichern, abgelaufen sind und dass ein neues Rowset angefordert werden soll.
-   Das **ROWSET \_ TYPE \_ FOREGROUNDLOST-Ereignis** gibt an, dass ein Element mit Vordergrundpriorität im Priorisierungsstapel herabgestuft wurde, da sich eine andere Person vor dieser Abfrage priorisiert hat.
-   Das **ROWSETEVENT \_ TYPE \_ SCOPESTATISTICS-Ereignis** bietet Ihnen die gleichen Informationen, die über den Aufruf der [**IRowsetPrioritization::GetScopeStatistics-Methode**](/windows/desktop/api/Searchapi/nf-searchapi-irowsetprioritization-getscopestatistics) verfügbar sind, aber über einen Push-Schieber wie folgt:
    -   Das Ereignis tritt auf, wenn die Priorisierungs-API verwendet wurde, um eine nicht standardmäßige Priorisierungsebene und eine Statistikereignishäufigkeit ungleich Null anzufordern.
    -   Das Ereignis tritt nur auf, wenn sich statistiken tatsächlich ändern und das in der [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization) angegebene Intervall verstrichen ist (das Intervall garantiert nicht die Häufigkeit des Ereignisses).
    -   Für dieses Ereignis wird garantiert der Zustand "Null springen" ausgelöst (null elemente, die hinzugefügt werden müssen, 0 (null) ändert sich, sofern ein Ereignis ungleich 0 (null) ausgelöst wurde.
    -   Der Indexer kann Elemente verarbeiten, ohne dieses Ereignis zu senden, wenn die Warteschlange vor der Häufigkeit des Statistikereignisses geleert wird.

## <a name="additional-resources"></a>Weitere Ressourcen

Sehen Sie sich die folgenden Ressourcen im Zusammenhang mit Priorisierung und Rowsets an:

-   Schnittstellen:
    -   [**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)
    -   [**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)
-   Aufzählungen:
    -   [**PRIORISIEREN \_ VON FLAGS**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)
    -   [**\_PRIORITÄTSSTUFE**](/windows/win32/api/searchapi/ne-searchapi-priority_level)
    -   [**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)
    -   [**\_ROWSETEVENT-TYP**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Windows 7 Suche](./-search-3x-wds-overview.md)
</dt> <dt>

[Neu für Windows 7-Suche](new-for-windows-7-search.md)
</dt> <dt>

[Windows Shellbibliotheken in Windows 7](-search-win7-development-scenarios.md)
</dt> </dl>

 

 