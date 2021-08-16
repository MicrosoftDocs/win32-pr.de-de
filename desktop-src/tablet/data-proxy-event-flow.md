---
description: In diesem Thema werden die Details zum Ereignis bei Verwendung der Funktionen des Ink-Analysedatenproxys erläutert.
ms.assetid: 837867a4-7cda-41b0-b20d-eec9a3a7fb86
title: Flow für Datenproxyereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ae6eab209466094ec79c0ed96923a28751b86c585d9ef750f9d12ef892036c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092806"
---
# <a name="data-proxy-event-flow"></a>Flow für Datenproxyereignisse

In diesem Thema werden die Details zum Ereignis bei Verwendung der Funktionen des Ink-Analysedatenproxys erläutert.

## <a name="data-proxy-event-flow-overview"></a>Data Proxy Event Flow Overview (Übersicht über Datenproxyereignisse)

Bei der Datenproxyverwendung von [**InkAnalyzer**](inkanalyzer.md)wird davon ausgegangen, dass die Anwendung, die InkAnalyzer integriert, bereits über ein vorhandenes Dokumentmodell verfügt, an das die Ergebnisse der Analyse übermittelt werden sollen. Es wird auch davon ausgegangen, dass die Anwendung Über Ergebnisse aus einem vorherigen Analysevorgang verfügt, auf dem sie in ihrem Dokumentmodell aufbauen möchten. Es kann auch einen Nicht-Ink-Kontext geben, der dem **InkAnalyzer** in Form eines **ImageNode-** oder **TextWordNode-Kontextknotens**[](icontextnode.md) hinzugefügt werden kann, um potenziell mit Ink versehen zu werden.

Der Schlüssel für das Datenproxysystem besteht darin, dass die Anwendung [**den ContextNode**](icontextnode.md) mit [**partiallyPopulated**](icontextnode-setpartiallypopulated.md)als "teilweise aufgefüllt" kennzeichnet. Wenn dieses Flag "true" ist, geht [**InkAnalyzer**](inkanalyzer.md) davon aus, dass drei Dinge über **diesen ContextNode** erforderlich sind:

-   Der Speicherort des [**ContextNode**](icontextnode.md) ist richtig.
-   Der Typ von [**ContextNode**](icontextnode.md) ist richtig.
-   Alle anderen Informationen zu [**diesem ContextNode**](icontextnode.md) werden an anderer Stelle gespeichert.

Wenn und wenn [**inkAnalyzer**](inkanalyzer.md) zusätzliche Informationen zu einem [**ContextNode**](icontextnode.md) benötigt, wird basierend auf diesen drei Regeln das [**PopulateContextNode-Ereignis**](-ianalysisproxyevents-populatecontextnode.md) auslösen und auf den betreffenden **ContextNode** verwiesen. Dies gibt der Anwendung die Möglichkeit, alle bekannten Informationen zu diesem **ContextNode** festzulegen, bevor **inkAnalyzer** sie genauer betrachtet. Nach der Behandlung eines **PopulateContextNode-Ereignisses** muss der betreffende **ContextNode** über eine gültige Location-Eigenschaft und die richtige Anzahl von Unterknoten verfügen, wenn es sich um einen **ContextNode-Container** handelt oder die richtigen Striche festgelegt sind, indem [**SetStrokes**](icontextnode-setstrokes.md)verwendet wird, wenn es sich um ein Ink-Blatt **contextNode** handelt. Wenn Sie diesen Speicherort und die Informationen zu Unterknoten oder Strichen nicht ordnungsgemäß festlegen, wird eine **InvalidOperation-Ausnahme** ausgelöst. Die Unterknoten für einen **ContextNode-Container** können selbst als teilweise aufgefüllt festgelegt werden. In diesem Fall werden weitere **PopulateContextNode-Ereignisse** ausgelöst, wenn **der InkAnalyzer** feststellt, dass sie für den aktuellen Analysevorgang benötigt werden.

In den folgenden Tabellen wird beschrieben, wann das [**PopulateContextNode-Ereignis**](-ianalysisproxyevents-populatecontextnode.md) während der verwendung von [**InkAnalyzer**](inkanalyzer.md)ausgelöst wird.

Nachdem [**InkAnalyzer**](inkanalyzer.md) einige Restuls berechnet hat, wird er auf die Anwendung zurückgreifen, um die Ergebnisse zu aktualisieren. Das erste ausgelöste Ereignis ist das [**InkAnalyzerStateChanging-Ereignis.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Dieses Ereignis gibt der Anwendung einfach an, dass sich der Strukturzustand des **InkAnalyzer-Objekts** gerade ändert. Dies bietet Anwendungen die Möglichkeit, das [**PartiallyPopulated-Flag**](icontextnode-setpartiallypopulated.md) für alle [**ContextNodes,**](icontextnodes.md) deren Zustand an anderer Stelle gespeichert ist, auf TRUE festzulegen. **InkAnalyzer** wird dann eine Reihe von [**PopulateContextNode-Ereignissen**](-ianalysisproxyevents-populatecontextnode.md) auslösen, um den aktuellen Zustand der Daten zu bestimmen. Sobald dies abschüssig ist, wird ein Abstimmungsvorgang erzwungen, um zu bestimmen, welche Hintergrundergebnisse noch angewendet werden können.

Um Ergebnisse auf [**inkAnalyzer**](inkanalyzer.md) anzuwenden, wird eine Reihe von Strukturänderungsereignissen ausgelöst. Die Strukturänderungsereignisse beschreiben Schritt für Schritt alle Änderungen, die zum Aktualisieren der Ergebnisse erforderlich sind. Diese Ereignisse sollen ohne Interuption oder Abbruch behandelt werden. Wenn der Analysevorgang (über die [**Abort-Methode)**](iinkanalyzer-abort.md) während der Verarbeitung der Strukturänderungsereignisse abgebrochen wird, ist der Zustand von **InkAnalyzer** ungültig, und das gesamte Dokument muss möglicherweise erneut analysiert werden.

In den folgenden Tabellen wird beschrieben, wann die Strukturänderungsereignisse während der Verwendung von InkAnalyzer ausgelöst werden. Die Tabellen beziehen sich auf die Zeitstempel, die im folgenden Ereignisflussdiagramm dargestellt werden.

![Abbildung des Flows zwischen der Benutzeroberfläche der Anwendung und der Hintergrundanalyse](images/7a0a54af-889e-43ed-8689-7f2d685567bf.jpg)

### <a name="adding-a-stroke"></a>Hinzufügen eines Strichs



| Zeitstempel | Ereignistyp oder Zweck | Ausgelöstes Ereignis | Kommentar                          |
|--------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T1, T5 und T9<br/> | \[Innerhalb des Aufrufs von AddStroke() \] \[ Tree exploration Event\]<br/> | [**PopulateContextNode-Ereignis**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst<br/> | Je nachdem, wie viele **Nicht klassifizierte**[**ContextNodes**](icontextnodes.md) vorhanden sind und der [**PartiallyPopulated-Wert**](icontextnode-setpartiallypopulated.md) auf TRUE festgelegt ist, können n [**PopulateContextNode-Ereignisse**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst werden.<br/> |
| T1, T5 und T9<br/> | \[Strukturänderungsereignis\]<br/>                                  | [**ContextNodeCreated-Ereignis**](-ianalysisproxyevents-contextnodecreated.md) ausgelöst<br/>   | Aufgrund des Aufrufs der [**AddStroke-Methode**](iinkanalyzer-addstroke.md) wird nur ein [**ContextNodeCreated-Ereignis**](-ianalysisproxyevents-contextnodecreated.md) ausgelöst. Allen Strichen wird der gleiche nicht klassifizierte [**ContextNode**](icontextnode.md)hinzugefügt.<br/>                      |



 

### <a name="deleting-a-stroke"></a>Löschen eines Strichs



| Zeitstempel | Ereignistyp oder Zweck | Ausgelöstes Ereignis | Kommentar                          |
|---------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T2, T6 und T10<br/> | \[Innerhalb des [**Aufrufs von RemoveStroke**](iinkanalyzer-removestroke.md)() \] \[ Tree exploration Event\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Ausgelöstes Ereignis<br/> | Je nachdem, wie viele [**ContextNodes**](icontextnodes.md) im Zusammenhang mit den gelöschten Strichen den Wert [**PartiallyPopulated**](icontextnode-setpartiallypopulated.md) aufweisen, kann eine Reihe von [**PopulateContextNode-Ereignissen**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst werden.<br/> |
| T2, T6 und T10<br/> | \[Strukturänderungsereignis\]<br/>                                                                          | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Ausgelöstes Ereignis<br/> | Abhängig vom gelöschten Ink-Inhalt und der aktuellen Analysestruktur können beliebig viele [**ContextNodeDeleting-Ereignisse**](-ianalysisproxyevents-contextnodedeleting.md) ausgelöst werden.<br/>                                                                                                       |



 

### <a name="calling-the-backgroundanalyze-method"></a>Aufrufen der BackgroundAnalyze-Methode



| Zeitstempel | Ereignistyp oder Zweck | Ausgelöstes Ereignis | Kommentar                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T3<br/>         | \[Innerhalb des Aufrufs von [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)() \] \[ Tree exploration Event\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Ausgelöstes Ereignis<br/> | Je nachdem, wie viele [**ContextNodes**](icontextnodes.md) in der strukturweiten Struktur den [**PartiallyPopulated-Wert**](icontextnode-createpartiallypopulatedsubnode.md) true haben (ein Ereignis pro [**ContextNode,**](icontextnode.md) das im aktuellen Analysevorgang benötigt wird), kann eine n Anzahl von [**PopulateContextNode-Ereignissen**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst werden.<br/> |



 

### <a name="after-the-call-to-backgroundanalyze-returns"></a>Nach der Rückgabe von Call to BackgroundAnalyze()



| Zeitstempel | Ereignistyp oder Zweck | Ausgelöstes Ereignis | Kommentar                          |
|-----------------------|---------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------|
| T3 bis T7<br/>   | \[Vom BG-Thread ausgelöste Ereignisse\]<br/> | Ausgelöstes Aktivitätsereignis<br/> | Während dieser Hintergrundphase der Analyse werden mehrere Aktivitätsereignisse ausgelöst.<br/> |



 

### <a name="when-intermediateresults-are-ready"></a>Wenn IntermediateResults bereit sind



| Zeitstempel | Ereignistyp oder Zweck | Ausgelöstes Ereignis | Kommentar                          |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T7 bis T8<br/>   | \[Vom BG-Thread ausgelöste Ereignisse, die den Start des ersten Abstimmungsvorgangs signalisierenden\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Ausgelöstes Ereignis<br/>         | Nur ein [**InkAnalyzerStateChanging-Ereignis**](-ianalysisproxyevents-inkanalyzerstatechanging.md) wurde ausgelöst. Dieses Ereignis wird ausgelöst, bevor der Zustand von [**InkAnalyzer**](inkanalyzer.md)überprüft wird, wodurch die Anwendung die Möglichkeit erhält, den [**PartiallyPopulated-Wert**](icontextnode-setpartiallypopulated.md) auf beliebigen Knoten festzulegen oder alle erforderlichen lokalen Dokumentsperren auszuführen.<br/> |
| T7 bis T8<br/>   | \[Strukturuntersuchungsereignis\]<br/>                                                              | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Ausgelöstes Ereignis<br/>                   | Je nach Ink-Inhalt können n [**PopulateContextNode-Ereignisse**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                               |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Ausgelöstes Ereignis<br/>                     | Je nach Ink-Inhalt können n [**ContextNodeCreated-Ereignisse**](-ianalysisproxyevents-contextnodecreated.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                                 |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Ausgelöstes Ereignis<br/>                   | Je nach Ink-Inhalt können n [**ContextNodeDeleting-Ereignisse**](-ianalysisproxyevents-contextnodedeleting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                               |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Je nach Ink-Inhalt kann n Anzahl von [**ContextNodeMovingToPosition-Ereignissen**](-ianalysisproxyevents-contextnodemovingtoposition.md) ausgelöst werden.<br/>                                                                                                                                                                                                                               |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Je nach Ink-Inhalt kann n Anzahl von [**ContextNodeReparenting-Ereignissen**](-ianalysisproxyevents-contextnodereparenting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                         |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Je nach Freiheitsinhalt kann n Anzahl von [**StrokeReparented-Ereignissen**](-ianalysisproxyevents-strokereparented.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                                     |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Je nach Ink-Inhalt kann n Anzahl von [**ContextNodeLinkAdding-Ereignissen**](-ianalysisproxyevents-contextnodelinkadding.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                           |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Je nach Ink-Inhalt können [**n ContextNodeLinkDeleting-Ereignisse**](-ianalysisproxyevents-contextnodelinkdeleting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                       |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Ereignis ausgelöst<br/> | Je nach Ink-Inhalt kann n Anzahl von [**ContextNodePropertiesUpdated-Ereignissen**](-ianalysisproxyevents-contextnodepropertiesupdated.md) ausgelöst werden. **ContextNodePropertiesUpdated** wird geplant, nachdem alle anderen [**ContextNode-Änderungsereignisse**](icontextnode.md) während dieses Abstimmungszeitraums [**ausgelöst**](iinkanalyzer-reconcile.md) wurden.<br/>              |
| T7 bis T8<br/>   | \[Ereignis gibt das Ende des ersten Abgleichsvorgang an.\]<br/>                            | [**IntermediateResults**](-ianalysisevents-intermediateresults.md) Ereignis ausgelöst<br/>                        | Pro Analysevorgang wird nur ein [**IntermediateResults-Ereignis**](-ianalysisevents-intermediateresults.md) ausgelöst.<br/>                                                                                                                                                                                                                                                                  |



 

### <a name="after-intermediateresults-have-been-handled"></a>Nachdem IntermediateResults verarbeitet wurde



| Zeitstempel | Ereignistyp oder -zweck | Ausgelöstes Ereignis | Kommentar                          |
|-----------------------|---------------------------------------------|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| T8 bis T11<br/>  | \[Vom BG-Thread ausgelöste Ereignisse\]<br/> | [**Aktivität**](-ianalysisevents-activity.md) Ereignis ausgelöst<br/> | Während [**dieses**](-ianalysisevents-activity.md) Analysezeitraums im Hintergrund werden mehrere Aktivitätsereignisse ausgelöst.<br/> |



 

### <a name="when-final-results-are-ready"></a>Wenn die endgültigen Ergebnisse bereit sind



| Zeitstempel | Ereignistyp oder -zweck | Ausgelöstes Ereignis | Kommentar                          |
|-----------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T11 bis T12<br/> | \[Vom BG-Thread ausgelöste Ereignisse, die den Beginn des zweiten Abgleichsvorganges signalisierenden\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Ereignis ausgelöst<br/>         | Nur ein [**InkAnalyzerStateChanging-Ereignis**](-ianalysisproxyevents-inkanalyzerstatechanging.md) wurde ausgelöst. Dieses Ereignis wird ausgelöst, bevor der Zustand von [**InkAnalyzer**](inkanalyzer.md)überprüft wird. Dadurch kann die Anwendung den [**PartiallyPopulated-Wert**](icontextnode-setpartiallypopulated.md) auf allen Knoten festlegen oder die erforderlichen lokalen Dokumentsperren durchführen.<br/> |
| T11 bis T12<br/> | \[Tree exploration Event\]<br/>                                                               | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Ereignis ausgelöst<br/>                   | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**PopulateContextNode-Ereignissen**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                             |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Ereignis ausgelöst<br/>                     | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodeCreated-Ereignissen**](-ianalysisproxyevents-contextnodecreated.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                               |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Ereignis ausgelöst<br/>                   | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodeDeleting-Ereignissen**](-ianalysisproxyevents-contextnodedeleting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                             |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodeMovingToPosition-Ereignissen**](-ianalysisproxyevents-contextnodemovingtoposition.md) ausgelöst werden.<br/>                                                                                                                                                                                                                             |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Abhängig vom Inhalt der Ink-Datei kann eine beliebige Anzahl von [**ContextNodeReparenting-Ereignissen**](-ianalysisproxyevents-contextnodereparenting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                       |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Je nach Freiheitsinhalt kann eine beliebige Anzahl von [**StrokeReparented-Ereignissen**](-ianalysisproxyevents-strokereparented.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                                   |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodeLinkAdding-Ereignissen**](-ianalysisproxyevents-contextnodelinkadding.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                         |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodeLinkDeleting-Ereignissen**](-ianalysisproxyevents-contextnodelinkdeleting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                     |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Ereignis ausgelöst<br/> | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodePropertiesUpdated-Ereignissen**](-ianalysisproxyevents-contextnodepropertiesupdated.md) ausgelöst werden. **ContextNodePropertiesUpdated** wird geplant, nachdem alle anderen [**ContextNode-Änderungsereignisse**](icontextnode.md) während dieses Abstimmungszeitraums [**ausgelöst**](iinkanalyzer-reconcile.md) wurden.<br/>            |
| T11 bis T12<br/> | \[Ereignis gibt das Ende des zweiten Abstimmungsvorgang an.\]<br/>                            | [**Ergebnisse**](-ianalysisevents-results.md) Ereignis ausgelöst<br/>                                                | Pro [**Analysevorgang**](-ianalysisevents-results.md) wird nur ein Results-Ereignis ausgelöst.<br/>                                                                                                                                                                                                                                                                                          |



 

 

 




