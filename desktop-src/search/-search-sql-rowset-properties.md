---
description: Nachdem ein Ergebnis von einer Abfrage zurückgegeben wurde, können Sie auf mehrere Eigenschaften für das Rowset zugreifen.
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: Rowset-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f753b607ff9579f3dffbe44209775ad5f81578bd9f15ddf2d4acd403bd266b5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863138"
---
# <a name="rowset-properties"></a>Rowset-Eigenschaften

Nachdem ein Ergebnis von einer Abfrage zurückgegeben wurde, können Sie auf mehrere Eigenschaften für das Rowset zugreifen.

Zusätzlich zu den standardmäßigen OLE-DB-Rowseteigenschaften bietet Windows Search-SQL die folgenden vier benutzerdefinierten Eigenschaften. Die GUID für diesen Eigenschaftensatz ist {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.

Windows Die Suche unterstützt die OLE-DB-Standardeigenschaft DBPROP \_ COMMANDTIMEOUT des [DBPROPSET \_ ROWSET-Eigenschaftensets.](/previous-versions//ms691738(v=vs.85))



| Eigenschaftenname                  | PROPID/type | Beschreibung                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DONOTCOMPUTEEXPENSIVEPROPS     | 15/VT \_ BOOL | Wenn Sie diese Einstellung auf TRUE festlegen, wird verhindert, dass teure Eigenschaften wie Ergebnisse gefunden und Max. Rangberechnlich sind, die eine Auswertung der gesamten Abfrage erfordern, wenn auf eine Rowseteigenschaft zugegriffen wird.                                                                                                                                                                         |
| Maximaler Rang (MAX \_ RANK)       | 6/VT \_ I4    | Der höchste Rang, der für ein beliebiges Ergebnis berechnet wird.                                                                                                                                                                                                                                                                                                          |
| Gefundene Ergebnisse (ERGEBNISSE \_ GEFUNDEN) | 7/VT \_ I4    | Die Gesamtanzahl eindeutiger Elemente für diese Abfrage. Bei einer SELECT-Abfrage ist dies die Anzahl der Elemente im Rowset. Bei einer GROUP ON-Abfrage ist dies die Anzahl eindeutiger Blattelemente. Diese Eigenschaft identifiziert nicht die Anzahl der Zeilen im Rowset der obersten Ebene (die Anzahl der Gruppen der obersten Ebene).                                                        |
| Where ID (WHEREID)             | 8/VT \_ I4    | Der Bezeichner für die Einschränkungen, die für eine Abfrage verwendet werden. Wenn ein Rowset geöffnet ist, wenn eine neue Abfrage ausgeführt wird, kann die neue Abfrage die Einschränkungen der älteren Abfrage wiederverwenden und so die bereits abgeschlossene Arbeit nutzen. Weitere Informationen zur Wiederverwendung von WHERE-Einschränkungen finden Sie in der [ReuseWhere-Funktion](-search-sql-reusewhere.md). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Indizierungspriorisierungs- und Rowsetereignisse in Windows 7](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
