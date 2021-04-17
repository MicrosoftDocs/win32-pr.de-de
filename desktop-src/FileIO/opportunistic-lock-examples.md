---
description: Diagramme von Netzwerkverkehrs Ansichten für eine opportunistische Sperre der Ebene 1, eine opportunistische Batch Sperre und eine opportunistische Filter-Sperre.
ms.assetid: 78830113-b18e-40c7-8ec4-8896dbc58030
title: Beispiele für die opportunistische Sperre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8b8a0c5b04897ddc2fc8f2e3bdec20f2fdb02d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529264"
---
# <a name="opportunistic-lock-examples"></a>Beispiele für die opportunistische Sperre

In den folgenden Beispielen werden Daten-und SMB-Nachrichten Bewegungen angezeigt, wenn opportunistische Sperren erstellt und beschädigt werden. Beachten Sie, dass Clients Datei Attributdaten und Datei Daten zwischenspeichern können.

Beachten Sie auch, dass diese Beispiele auf Situationen basieren, in denen Client Anwendungen opportunistische Sperren von Remote Servern anfordern. Diese Prozesse werden automatisch vom Netzwerkredirector und dem Remote Server initiiert – es gibt keine direkte Beteiligung durch die Client Anwendung oder Anwendungen. Die in diesen Beispielen beschriebenen Prozesse können in Situationen verallgemeinert werden, in denen lokale Client Anwendungen direkt opportunistische Sperren aus dem lokalen Dateisystem anfordern, mit der Ausnahme, dass kein Datenaustausch über das Netzwerk beteiligt ist.

## <a name="level-1-opportunistic-lock"></a>Opportunistische Sperre der Ebene 1

Das folgende Diagramm zeigt eine Netzwerkverkehrs Ansicht einer opportunistischen Sperre auf Ebene 1 für eine Datei. Die Pfeile geben die Richtung der Daten Verschiebung an, falls vorhanden.



| Ereignis | Client X                                          | Server                                   | Client Y                                          |
|-------|---------------------------------------------------|------------------------------------------|---------------------------------------------------|
| 1     | Öffnet die Datei, fordert Ebene 1 Sperre = =>          |                                          |                                                   |
| 2     |                                                   | <= = gibt eine opportunistische Sperre der Ebene 1 aus. |                                                   |
| 3     | Führt Lese-, Schreib-und andere Vorgänge aus = => |                                          |                                                   |
| 4     |                                                   |                                          | <= = Anforderungen zum Öffnen der Datei                      |
| 5     |                                                   | <= = opportunistische Sperre wird unterbrochen         |                                                   |
| 6     | Verwirft Read-Ahead-Daten                          |                                          |                                                   |
| 7     | Schreibt Data = =>                                |                                          |                                                   |
| 8     | Sendet "Close" oder "Done" Message = =>            |                                          |                                                   |
| 9     |                                                   | Okays-Öffnungsvorgang = =>              |                                                   |
| 10    | Führt Lese-, Schreib-und andere Vorgänge aus = => |                                          | <= = führt Lese-, Schreib-und andere Vorgänge aus. |



 

In Ereignis 1 öffnet Client X eine Datei und fordert im Rahmen des Öffnungs Vorgangs eine opportunistische Sperre der Ebene 1 für die Datei an. In Ereignis 2 gewährt der Server die Sperre der Ebene 1, da die Datei von keinem anderen Client geöffnet ist. Der Client greift in Ereignis 3 auf die übliche Weise auf die Datei zu.

In Ereignis 4 versucht Client Y, die Datei zu öffnen und eine opportunistische Sperre zu anfordern. Der Server sieht, dass die Datei in Client X geöffnet ist. Der Server ignoriert die Anforderung von Y, während der Client X alle Schreib Daten leert und den Lesecache für die Datei verlässt.

Der Server erzwingt das Bereinigen von x, indem er eine SMB-Nachricht sendet, die die opportunistische Sperre, Ereignis 5, unterbricht. Client X "im Hintergrund" löscht alle Read-Ahead-Daten; Dies bedeutet, dass dieser Prozess keinen Netzwerk Datenverkehr generiert. In Ereignis 7 schreibt Client X alle zwischengespeicherten Schreib Daten auf den Server. Wenn Client x das Schreiben zwischen gespeicherter Daten auf den Server abgeschlossen hat, sendet Client x entweder eine "Close"-oder eine "Done"-Meldung an den Server, Ereignis 8.

Nachdem der Server benachrichtigt wurde, dass Client X den Schreib Cache auf den Server geleert hat oder die Datei geschlossen hat, kann der Server die Datei für den Client Y öffnen, und zwar in Ereignis 9. Da auf dem Server nun zwei Clients mit derselben Datei geöffnet sind, wird für keine dieser beiden Clients eine opportunistische Sperre erteilt. Beide Clients fahren mit dem Lesen aus der Datei fort, und eine oder keines von beiden wird in die Datei geschrieben.

## <a name="batch-opportunistic-lock"></a>Batch-opportunistische Sperre

Das folgende Diagramm zeigt eine Netzwerkverkehrs Ansicht einer Batch opportunistischen Sperre. Die Pfeile geben die Richtung der Daten Verschiebung an, falls vorhanden.



| Ereignis | Client X                               | Server                                 | Client Y                                          |
|-------|----------------------------------------|----------------------------------------|---------------------------------------------------|
| 1     | Öffnet die Datei, fordert Batch Sperre = => |                                        |                                                   |
| 2     |                                        | <= = erteilt eine opportunistische Batch Sperre |                                                   |
| 3     | Lese Datei = =>                      |                                        |                                                   |
| 4     |                                        | <= = sendet Daten                      |                                                   |
| 5     | Schließt die Datei.                            |                                        |                                                   |
| 6     | Öffnet die Datei.                             |                                        |                                                   |
| 7     | Sucht nach Daten                      |                                        |                                                   |
| 8     | Reads Data = =>                      |                                        |                                                   |
| 9     |                                        | <= = sendet Daten                      |                                                   |
| 10    | Schließt die Datei.                            |                                        |                                                   |
| 11    |                                        |                                        | <= = öffnet die Datei.                                 |
| 12    |                                        | <= = opportunistische Sperre wird unterbrochen       |                                                   |
| 13    | Schließt File = =>                     |                                        |                                                   |
| 14    |                                        | Okays-Öffnungsvorgang = =>            |                                                   |
| 15    |                                        |                                        | <= = führt Lese-, Schreib-und andere Vorgänge aus. |



 

In der opportunistischen Batch-Sperre öffnet Client x eine Datei, Ereignis 1, und der Server erteilt Client x eine Batch Sperre in Ereignis 2. Client X versucht, Daten, Ereignis 3, zu lesen, auf die der Server mit Daten antwortet, Ereignis 4.

Das Ereignis 5 zeigt die opportunistische Sperre des Batches bei der Arbeit. Die Anwendung auf dem Client X schließt die Datei. Der Netzwerkredirector filtert jedoch den Close-Vorgang heraus und überträgt keine close-Nachricht und führt so eine "Stille" Schließung durch. Der Netzwerkredirector kann dies tun, weil der Client X den alleinigen Besitz der Datei besitzt. Später wird die Datei in Ereignis 6 von der Anwendung erneut geöffnet. Auch hier werden keine Daten über das Netzwerk übertragen. Soweit der Server betroffen ist, wurde die Datei auf diesem Client seit Ereignis 2 geöffnet.

Die Ereignisse 7, 8 und 9 zeigen den üblichen Kurs des Netzwerkverkehrs. In Ereignis 10 tritt ein weiterer automatischer Schluss Vorgang auf.

In Ereignis 11 versucht Client Y, die Datei zu öffnen. Der Server zeigt die Datei an, die der Client x geöffnet hat, obwohl Sie von der Anwendung auf dem Client x geschlossen wurde. Daher sendet der Server eine Nachricht, die die opportunistische Sperre an den Client x unterbricht. Client x sendet nun die Close-Nachricht über das Netzwerk, Ereignis 13. Das Ereignis 14 folgt, wenn der Server die Datei für den Client Y öffnet. Die Anwendung auf dem Client X hat die Datei geschlossen und führt somit keine Übertragung zum oder vom Server für diese Datei durch. Der Client Y startet Datenübertragungen wie gewohnt in Ereignis 15.

Zwischen dem Zeitpunkt, zu dem Client X die Sperre für die Datei in Ereignis 2 erhält, und dem abschließenden schließen bei Ereignis 13, sind alle Datei Daten, die vom Client zwischengespeichert wurden, gültig, und zwar trotz der zwischengeschalteten und schließenden Anwendungs Vorgänge. Nachdem die opportunistische Sperre jedoch abgebrochen wurde, können zwischengespeicherte Daten nicht als gültig betrachtet werden.

## <a name="filter-opportunistic-lock"></a>Opportunistische Sperre Filtern

Das folgende Diagramm zeigt eine Netzwerkverkehrs Ansicht einer Filter opportunistischen Sperre. Die Pfeile geben die Richtung der Daten Verschiebung an, falls vorhanden.



| Ereignis | Client X                                | Server                   | Client Y                    |
|-------|-----------------------------------------|--------------------------|-----------------------------|
| 1     | Öffnet die Datei ohne Zugriffsrechte = => |                          |                             |
| 2     |                                         | <= = öffnet die Datei.    |                             |
| 3     | Anforderungs Filter Sperre = =>              |                          |                             |
| 4     |                                         | <= = erteilt Sperre       |                             |
| 5     | Öffnet die Datei zum Lesen = =>           |                          |                             |
| 6     |                                         | <= = öffnet die Datei erneut.  |                             |
| 7     | Liest Daten mithilfe des Read-Handles = => |                          |                             |
| 8     |                                         | <= = sendet Daten        |                             |
| 9     |                                         | <= = sendet Daten        |                             |
| 10    |                                         | <= = sendet Daten        |                             |
| 11    |                                         |                          | <= = öffnet die Datei.       |
| 12    |                                         | Öffnet die Datei = =>    |                             |
| 13    |                                         |                          | <= = fordert Filter Sperre an |
| 14    |                                         | Verweigert Filter Lock = => |                             |
| 15    |                                         |                          | <= = liest Daten           |
| 16    |                                         | Daten werden gesendet = =>        |                             |
| 17    | Liest (zwischengespeicherte) Daten                     |                          |                             |
| 18    | Schließt File = =>                      |                          |                             |
| 19    |                                         |                          | <= = schließt die Datei.          |



 

In der opportunistischen Filter-Sperre öffnet Client X eine Datei, Ereignis 1, und der Server antwortet in Ereignis 2. Der Client fordert dann eine opportunistische Filter Sperre in Ereignis 3 an, gefolgt vom Server, der die opportunistische Sperre in Ereignis 4 erteilt. Client X öffnet die Datei dann erneut zum Lesen in Ereignis 5, auf den der Server in Ereignis 6 antwortet. Der Client versucht dann, Daten zu lesen, auf die der Server mit Daten antwortet, Ereignis 8.

Das Ereignis 9 zeigt die opportunistische Sperre des Filters bei der Arbeit. Der Server liest den Client vor und sendet die Daten über das Netzwerk, auch wenn der Client ihn nicht angefordert hat. Der Client speichert die Daten zwischen. In Ereignis 10 erwartet der Server auch eine zukünftige Daten Anforderung und sendet einen anderen Teil der Datei, damit der Client zwischengespeichert wird.

In Ereignis 11 und 12 wird die Datei von einem anderen Client, Y, geöffnet. Client Y fordert außerdem eine opportunistische Filter Sperre an. In Ereignis 14 verweigert der Server Sie. In Ereignis 15 fordert Client Y Daten an, die der Server in Ereignis 16 sendet. Keines dieser Auswirkungen wirkt sich auf den Client X aus. Diese Datei kann jederzeit von einem anderen Client für den Lesezugriff geöffnet werden. Kein anderer Client wirkt sich auf die Filter Sperre von Client X aus.

Das Ereignis 17 zeigt Client X-Lesedaten. Da der Server die Daten jedoch bereits gesendet hat und diese vom Client zwischengespeichert wurden, überschreitet der Datenverkehr das Netzwerk nicht.

In diesem Beispiel versucht Client X nie, alle Daten in der Datei zu lesen, sodass der Read-Ahead-Vorgang, der durch die Ereignisse 9 und 10 angegeben wird, "verschwendet" wird. Das heißt, dass die Daten nie tatsächlich verwendet werden. Dies ist ein akzeptabler Verlust, da der Lesevorgang die Anwendung bereinigt hat.

In Ereignis 18 schließt Client X die Datei. Der Netzwerkredirector des Clients bricht die zwischengespeicherten Daten ab. Der Server schließt die Datei.

 

 



