---
description: In diesem Thema werden die Details des Ereignisses bei Verwendung der Datenproxyfunktionen für die Ink-Analyse erläutert.
ms.assetid: 837867a4-7cda-41b0-b20d-eec9a3a7fb86
title: Datenproxy-Ereignisfluss
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b88fbb43e54b19486a6413bc44319fa2dd737486
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432542"
---
# <a name="data-proxy-event-flow"></a>Datenproxy-Ereignisfluss

In diesem Thema werden die Details des Ereignisses bei Verwendung der Datenproxyfunktionen für die Ink-Analyse erläutert.

## <a name="data-proxy-event-flow-overview"></a>Übersicht über den Datenproxyereignisfluss

Bei der Verwendung des Datenproxys von [**InkAnalyzer**](inkanalyzer.md)wird davon ausgegangen, dass die Anwendung, die InkAnalyzer integriert, bereits über ein vorhandenes Dokumentmodell verfügt, an das die Ergebnisse der Analyse als Proxy verwendet werden sollen. Es wird auch davon ausgegangen, dass die Anwendung Ergebnisse aus einem vorherigen Analysevorgang enthält, auf dem sie in ihrem Dokumentmodell aufbauen möchten. Es kann auch Nicht-Ink-Kontext geben, der dem **InkAnalyzer** in Form eines **ImageNode** oder **TextWordNode**[**ContextNode**](icontextnode.md) hinzugefügt werden kann, um möglicherweise mit Ink kommentiert zu werden.

Der Schlüssel zum Datenproxysystem ist, dass die Anwendung [**contextNode**](icontextnode.md) mit partiallyPopulated als "teilweise [**aufgefüllt" kennzeichnet.**](icontextnode-setpartiallypopulated.md) Wenn dieses Flag true ist, geht [**InkAnalyzer**](inkanalyzer.md) davon aus, dass drei Dinge über **diesen ContextNode:**

-   Der Speicherort des [**ContextNode ist**](icontextnode.md) richtig.
-   Der Typ von [**ContextNode ist**](icontextnode.md) richtig.
-   Alle anderen Informationen zu [**diesem ContextNode werden**](icontextnode.md) an anderer Stelle gespeichert.

Wenn und wenn [**der InkAnalyzer**](inkanalyzer.md) zusätzliche Informationen zu [**einem ContextNode**](icontextnode.md) benötigt, wird basierend auf diesen drei Regeln das [**PopulateContextNode-Ereignis**](-ianalysisproxyevents-populatecontextnode.md) aufgerufen und auf den in Frage gestellten **ContextNode** verwiesen. Dadurch kann die Anwendung alle bekannten Informationen für diesen **ContextNode** festlegen, bevor **der InkAnalyzer** ihn genauer untersucht. Nach der Behandlung eines **PopulateContextNode-Ereignisses** muss der **kontextspezifische ContextNode** über eine gültige Location-Eigenschaft verfügen, die richtige Anzahl von Unterknoten festlegen, wenn es sich um einen **ContextNode-Container** handelt oder die richtigen Striche festgelegt wurden, indem [**SetStrokes**](icontextnode-setstrokes.md)verwendet wird, wenn es sich um einen Ink leaf **ContextNode handelt.** Wenn dieser Speicherort und die Unter- oder Strichinformationen nicht ordnungsgemäß festgelegt werden, führt dies zu einer **InvalidOperation-Ausnahme.** Die Unterknoten für einen **Container ContextNode** können selbst als teilweise aufgefüllt festgelegt werden. In diesem Fall werden weitere **PopulateContextNode-Ereignisse** ausgelöst, wenn **der InkAnalyzer** feststellt, dass sie für den aktuellen Analysevorgang benötigt werden.

In den folgenden Tabellen wird beschrieben, wann [**das PopulateContextNode-Ereignis**](-ianalysisproxyevents-populatecontextnode.md) während der gesamten Verwendung von [**InkAnalyzer ausgelöst wird.**](inkanalyzer.md)

Nachdem [**der InkAnalyzer**](inkanalyzer.md) einige Restuls berechnet hat, wird er auf die Anwendung zurückschauen, um die Ergebnisse zu aktualisieren. Das erste ausgelöste Ereignis ist das [**InkAnalyzerStateChanging-Ereignis.**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Dieses Ereignis gibt der Anwendung lediglich an, dass sich der Strukturzustand des **InkAnalyzer-Objekts** ändert. Dadurch können Anwendungen das [**Flag PartiallyPopulated**](icontextnode-setpartiallypopulated.md) auf "true" für alle [**ContextNodes**](icontextnodes.md) festlegen, deren Zustand an anderer Stelle gespeichert ist. Der **InkAnalyzer** gibt dann eine Reihe von [**PopulateContextNode-Ereignissen**](-ianalysisproxyevents-populatecontextnode.md) aus, um den aktuellen Zustand der Daten zu bestimmen. Sobald dies determiend ist, wird ein Abstimmungsvorgang durchgeführt, um zu bestimmen, welche Hintergrundergebnisse noch angewendet werden können.

Um Ergebnisse auf [**InkAnalyzer anzuwenden,**](inkanalyzer.md) werden eine Reihe von Strukturänderungsereignissen ausgelöst. Die Strukturänderungsereignisse beschreiben schritt für Schritt alle Änderungen, die zum Aktualisieren der Ergebnisse erforderlich sind. Diese Ereignisse sind für die Handhabung in der -Vererbung ohne Interuption oder Canceling vorgesehen. Wenn der Analysevorgang (über die [**Abort-Methode)**](iinkanalyzer-abort.md) während der Verarbeitung der Strukturänderungsereignisse abgebrochen wird, ist der Zustand des **InkAnalyzer** ungültig, und das gesamte Dokument muss möglicherweise erneut analysiert werden.

In den folgenden Tabellen wird beschrieben, wann die Strukturänderungsereignisse während der gesamten Verwendung von InkAnalyzer ausgelöst werden. Die Tabellen verweisen auf die im folgenden Ereignisflussdiagramm gezeigten Zeitstempel.

![iimage mit dem Flow zwischen der Anwendungsbenutzeroberfläche und dem Hintergrundanalysegerät](images/7a0a54af-889e-43ed-8689-7f2d685567bf.jpg)

### <a name="adding-a-stroke"></a>Hinzufügen eines Strichs



| Zeitstempel | Ereignistyp oder -zweck | Ausgelöstes Ereignis | Kommentar                          |
|--------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T1, T5 und T9<br/> | \[Innerhalb des Aufrufs von AddStroke() \] \[ Tree exploration Event\]<br/> | [**PopulateContextNode-Ereignis**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst<br/> | Je nachdem, wie viele nicht klassifizierte [**ContextNodes**](icontextnodes.md) vorhanden sind und [**der PartiallyPopulated-Wert**](icontextnode-setpartiallypopulated.md) auf TRUE festgelegt ist, kann n Anzahl von [**PopulateContextNode-Ereignissen**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst werden.<br/> |
| T1, T5 und T9<br/> | \[Strukturänderungsereignis\]<br/>                                  | [**Ausgelöstes ContextNodeCreated-Ereignis**](-ianalysisproxyevents-contextnodecreated.md)<br/>   | Als Ergebnis des Aufrufs der [**AddStroke-Methode**](iinkanalyzer-addstroke.md) wird nur ein [**ContextNodeCreated-Ereignis**](-ianalysisproxyevents-contextnodecreated.md) ausgelöst. Allen Strichen wird der gleiche nicht klassifizierte [**ContextNode hinzugefügt.**](icontextnode.md)<br/>                      |



 

### <a name="deleting-a-stroke"></a>Löschen eines Strichs



| Zeitstempel | Ereignistyp oder -zweck | Ausgelöstes Ereignis | Kommentar                          |
|---------------------------|-----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T2, T6 und T10<br/> | \[Innerhalb des Aufrufs von [**RemoveStroke**](iinkanalyzer-removestroke.md)() \] \[ Tree exploration Event\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Ereignis ausgelöst<br/> | Abhängig davon, wie viele [**ContextNodes**](icontextnodes.md) im Zusammenhang mit den zu löschenden Strichen den [**PartiallyPopulated-Wert**](icontextnode-setpartiallypopulated.md) true haben, kann eine Reihe von [**PopulateContextNode-Ereignissen**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst werden.<br/> |
| T2, T6 und T10<br/> | \[Strukturänderungsereignis\]<br/>                                                                          | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Ereignis ausgelöst<br/> | Abhängig vom gelöschten Ink-Inhalt und der aktuellen Analysestruktur kann eine beliebige Anzahl von [**ContextNodeDeleting-Ereignissen**](-ianalysisproxyevents-contextnodedeleting.md) ausgelöst werden.<br/>                                                                                                       |



 

### <a name="calling-the-backgroundanalyze-method"></a>Aufrufen der BackgroundAnalyze-Methode



| Zeitstempel | Ereignistyp oder -zweck | Ausgelöstes Ereignis | Kommentar                          |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T3<br/>         | \[Innerhalb des Aufrufs von [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md)() \] \[ Tree exploration Event\]<br/> | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Ereignis ausgelöst<br/> | Es kann n Anzahl von [**PopulateContextNode-Ereignissen**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst werden, je nachdem, wie viele [**ContextNodes**](icontextnodes.md) in der gesamten Struktur den [**PartiallyPopulated-Wert**](icontextnode-createpartiallypopulatedsubnode.md) true haben (ein Ereignis pro [**ContextNode,**](icontextnode.md) das im aktuellen Analysevorgang benötigt wird).<br/> |



 

### <a name="after-the-call-to-backgroundanalyze-returns"></a>Nach der Rückgabe des Aufrufs von BackgroundAnalyze()



| Zeitstempel | Ereignistyp oder -zweck | Ausgelöstes Ereignis | Kommentar                          |
|-----------------------|---------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------|
| T3 bis T7<br/>   | \[Vom BG-Thread ausgelöste Ereignisse\]<br/> | Aktivitätsereignis ausgelöst<br/> | Während dieses Analysezeitraums im Hintergrund werden mehrere Aktivitätsereignisse ausgelöst.<br/> |



 

### <a name="when-intermediateresults-are-ready"></a>Wenn IntermediateResults bereit sind



| Zeitstempel | Ereignistyp oder -zweck | Ausgelöstes Ereignis | Kommentar                          |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T7 bis T8<br/>   | \[Vom BG-Thread ausgelöste Ereignisse, die den Start des ersten Abgleichsvorgang signalisierenden\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Ereignis ausgelöst<br/>         | Nur ein [**InkAnalyzerStateChanging-Ereignis**](-ianalysisproxyevents-inkanalyzerstatechanging.md) wurde ausgelöst. Dieses Ereignis wird ausgelöst, bevor der Status von [**InkAnalyzer**](inkanalyzer.md)überprüft wird. Dadurch kann die Anwendung den [**PartiallyPopulated-Wert**](icontextnode-setpartiallypopulated.md) auf allen Knoten festlegen oder die erforderlichen lokalen Dokumentsperren durchführen.<br/> |
| T7 bis T8<br/>   | \[Tree exploration Event\]<br/>                                                              | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Ereignis ausgelöst<br/>                   | Je nach Ink-Inhalt kann n Anzahl [**von PopulateContextNode-Ereignissen**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                               |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Ereignis ausgelöst<br/>                     | Je nach Ink-Inhalt kann n Anzahl von [**ContextNodeCreated-Ereignissen**](-ianalysisproxyevents-contextnodecreated.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                                 |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Ereignis ausgelöst<br/>                   | Je nach Ink-Inhalt kann n Anzahl von [**ContextNodeDeleting-Ereignissen**](-ianalysisproxyevents-contextnodedeleting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                               |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Je nach Ink-Inhalt können n [**ContextNodeMovingToPosition-Ereignisse**](-ianalysisproxyevents-contextnodemovingtoposition.md) ausgelöst werden.<br/>                                                                                                                                                                                                                               |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Je nach Ink-Inhalt können n [**ContextNodeReparenting-Ereignisse**](-ianalysisproxyevents-contextnodereparenting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                         |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Je nach Ink-Inhalt kann eine n Anzahl von [**StrokeReparented-Ereignissen**](-ianalysisproxyevents-strokereparented.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                                     |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Je nach Ink-Inhalt können n [**ContextNodeLinkAdding-Ereignisse**](-ianalysisproxyevents-contextnodelinkadding.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                           |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Je nach Ink-Inhalt können n [**ContextNodeLinkDeleting-Ereignisse**](-ianalysisproxyevents-contextnodelinkdeleting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                       |
| T7 bis T8<br/>   | \[Strukturänderungsereignis\]<br/>                                                             | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Ausgelöstes Ereignis<br/> | Je nach Ink-Inhalt können n [**ContextNodePropertiesUpdated-Ereignisse**](-ianalysisproxyevents-contextnodepropertiesupdated.md) ausgelöst werden. **ContextNodePropertiesUpdated** wird als rasied geplant, nachdem alle anderen [**ContextNode-Änderungsereignisse**](icontextnode.md) während dieses [**Abstimmungszeitraums**](iinkanalyzer-reconcile.md) ausgelöst wurden.<br/>              |
| T7 bis T8<br/>   | \[Das Ereignis gibt das Ende des ersten Abstimmungsvorgangs an.\]<br/>                            | [**IntermediateResults**](-ianalysisevents-intermediateresults.md) Ausgelöstes Ereignis<br/>                        | Pro Analysevorgang wird nur ein [**IntermediateResults-Ereignis**](-ianalysisevents-intermediateresults.md) ausgelöst.<br/>                                                                                                                                                                                                                                                                  |



 

### <a name="after-intermediateresults-have-been-handled"></a>Nach der Behandlung von IntermediateResults



| Zeitstempel | Ereignistyp oder -zweck | Ausgelöstes Ereignis | Kommentar                          |
|-----------------------|---------------------------------------------|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| T8 bis T11<br/>  | \[Vom BG-Thread ausgelöste Ereignisse\]<br/> | [**Aktivität**](-ianalysisevents-activity.md) Ausgelöstes Ereignis<br/> | Während dieser Hintergrundphase der Analyse werden mehrere [**Aktivitätsereignisse**](-ianalysisevents-activity.md) ausgelöst.<br/> |



 

### <a name="when-final-results-are-ready"></a>Wenn die endgültigen Ergebnisse bereit sind



| Zeitstempel | Ereignistyp oder -zweck | Ausgelöstes Ereignis | Kommentar                          |
|-----------------------|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T11 bis T12<br/> | \[Vom BG-Thread ausgelöste Ereignisse, die den Start des zweiten Abstimmungsvorgangs signalisierenden\]<br/> | [**InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) Ausgelöstes Ereignis<br/>         | Nur ein [**InkAnalyzerStateChanging-Ereignis**](-ianalysisproxyevents-inkanalyzerstatechanging.md) wurde ausgelöst. Dieses Ereignis wird ausgelöst, bevor der Zustand von [**InkAnalyzer**](inkanalyzer.md)überprüft wird, wodurch die Anwendung die Möglichkeit erhält, den [**PartiallyPopulated-Wert**](icontextnode-setpartiallypopulated.md) auf allen Knoten festzulegen oder eine erforderliche lokale Dokumentsperre auszuführen.<br/> |
| T11 bis T12<br/> | \[Strukturuntersuchungsereignis\]<br/>                                                               | [**PopulateContextNode**](-ianalysisproxyevents-populatecontextnode.md) Ausgelöstes Ereignis<br/>                   | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**PopulateContextNode-Ereignissen**](-ianalysisproxyevents-populatecontextnode.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                             |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeCreated**](-ianalysisproxyevents-contextnodecreated.md) Ausgelöstes Ereignis<br/>                     | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodeCreated-Ereignissen**](-ianalysisproxyevents-contextnodecreated.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                               |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeDeleting**](-ianalysisproxyevents-contextnodedeleting.md) Ausgelöstes Ereignis<br/>                   | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodeDeleting-Ereignissen**](-ianalysisproxyevents-contextnodedeleting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                             |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md)<br/>                | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodeMovingToPosition-Ereignissen**](-ianalysisproxyevents-contextnodemovingtoposition.md) ausgelöst werden.<br/>                                                                                                                                                                                                                             |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeReparenting**](-ianalysisproxyevents-contextnodereparenting.md)<br/>                          | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodeReparenting-Ereignissen**](-ianalysisproxyevents-contextnodereparenting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                       |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**StrokeReparented**](-ianalysisproxyevents-strokereparented.md)<br/>                                      | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**StrokeReparented-Ereignissen**](-ianalysisproxyevents-strokereparented.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                                   |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeLinkAdding**](-ianalysisproxyevents-contextnodelinkadding.md)<br/>                            | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodeLinkAdding-Ereignissen**](-ianalysisproxyevents-contextnodelinkadding.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                         |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodeLinkDeleting**](-ianalysisproxyevents-contextnodelinkdeleting.md)<br/>                        | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodeLinkDeleting-Ereignissen**](-ianalysisproxyevents-contextnodelinkdeleting.md) ausgelöst werden.<br/>                                                                                                                                                                                                                                     |
| T11 bis T12<br/> | \[Strukturänderungsereignis\]<br/>                                                              | [**ContextNodePropertiesUpdated**](-ianalysisproxyevents-contextnodepropertiesupdated.md) Ausgelöstes Ereignis<br/> | Je nach Ink-Inhalt kann eine beliebige Anzahl von [**ContextNodePropertiesUpdated-Ereignissen**](-ianalysisproxyevents-contextnodepropertiesupdated.md) ausgelöst werden. **ContextNodePropertiesUpdated** wird als rasied geplant, nachdem alle anderen [**ContextNode-Änderungsereignisse**](icontextnode.md) während dieses [**Abstimmungszeitraums**](iinkanalyzer-reconcile.md) ausgelöst wurden.<br/>            |
| T11 bis T12<br/> | \[Das Ereignis gibt das Ende des zweiten Abstimmungsvorgangs an.\]<br/>                            | [**Ergebnisse**](-ianalysisevents-results.md) Ausgelöstes Ereignis<br/>                                                | Pro Analysevorgang wird nur ein [**Ergebnisereignis**](-ianalysisevents-results.md) ausgelöst.<br/>                                                                                                                                                                                                                                                                                          |



 

 

 




