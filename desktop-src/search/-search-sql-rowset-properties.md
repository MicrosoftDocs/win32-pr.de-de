---
description: Nachdem ein Ergebnis von einer Abfrage zurückgegeben wurde, können Sie auf mehrere Eigenschaften für das Rowset zugreifen.
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: Rowset-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e498c701224a879c09653d6f265151297d2ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346280"
---
# <a name="rowset-properties"></a>Rowset-Eigenschaften

Nachdem ein Ergebnis von einer Abfrage zurückgegeben wurde, können Sie auf mehrere Eigenschaften für das Rowset zugreifen.

Zusätzlich zu den standardmäßigen OLE-DB-Rowseteigenschaften bietet Windows Search SQL die folgenden vier benutzerdefinierten Eigenschaften. Die GUID für diesen Eigenschaften Satz ist {AA6EE6B0E828-11D0-B23E-00aa0047fc01}.

Windows Search unterstützt die Standard-OLE-DB-Eigenschaft DBPROP \_ CommandTimeout der Eigenschaften Gruppe [DBPROPSET- \_ Rowset](/previous-versions//ms691738(v=vs.85)) .



| Eigenschaftenname                  | PROPID/Typ | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Donotcomputeexpensive-Eigenschaften     | 15/VT \_ bool | Wenn diese Eigenschaft auf true festgelegt wird, werden teure Eigenschaften wie gefundene Ergebnisse und der maximale Rang, bei denen die gesamte Abfrage ausgewertet werden muss, beim Zugriff auf eine Rowseteigenschaft                                                                                                                                                                         |
| Maximaler Rang (max. \_ Rang)       | 6/VT \_ I4    | Der höchste Rang, der für jedes Ergebnis berechnet wird.                                                                                                                                                                                                                                                                                                          |
| Gefundene Ergebnisse (Ergebnisse \_ gefunden) | 7/VT \_ I4    | Die Gesamtanzahl der eindeutigen Elemente für diese Abfrage. Bei einer SELECT-Abfrage ist dies die Anzahl der Elemente im Rowset. Bei einer Gruppe bei der Abfrage ist dies die Anzahl eindeutiger Blatt Elemente. Diese Eigenschaft identifiziert nicht die Anzahl der Zeilen im Rowset der obersten Ebene (die Anzahl der Gruppen der obersten Ebene).                                                        |
| Where-ID (whereid)             | 8/VT \_ I4    | Der Bezeichner für die Einschränkungen, die für eine Abfrage verwendet werden. Wenn ein Rowset geöffnet ist, wenn eine neue Abfrage ausgeführt wird, kann die neue Abfrage die Einschränkungen der älteren Abfrage wieder verwenden und so die bereits abgeschlossenen Arbeiten nutzen. Weitere Informationen zur Verwendung von WHERE-Einschränkungen finden Sie in der [reusewhere-Funktion](-search-sql-reusewhere.md). |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Indizieren von Priorisierungs-und rowsetereignissen in Windows 7](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
