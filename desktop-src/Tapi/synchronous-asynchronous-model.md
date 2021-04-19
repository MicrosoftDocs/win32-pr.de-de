---
description: Die interaktive Art von Telefonie erfordert TAPI, dass Sie eine echt Zeit Umgebung ist.
ms.assetid: b8512588-ec28-4fbe-b47f-b900e2dba1f2
title: Synchrones/Asynchrones Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02b3d3b58e9704719e502fa3efc11bc4dc216479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349207"
---
# <a name="synchronousasynchronous-model"></a>Synchrones/Asynchrones Modell

Die interaktive Art von Telefonie erfordert TAPI, dass Sie eine echt Zeit Umgebung ist. Viele der TAPI-Funktionen müssen schnell ausgeführt werden, und die Ergebnisse werden synchron an die Anwendung zurückgegeben. Andere Funktionen (z. b. die Wahl) können möglicherweise nicht so schnell wie möglich ausgeführt werden und werden daher asynchron ausgeführt.

Telefonievorgänge werden entweder synchron oder asynchron ausgeführt. Diese beiden Modelle unterscheiden sich wie folgt. *Synchrone Funktionen* führen die gesamte Anforderung aus, bevor der Thread des Aufrufers vom Funktionsaufruf zurückgegeben werden kann. *Asynchrone Funktionen* geben zurück, bevor die Anforderung vollständig ausgeführt wurde. Wenn die asynchrone Anforderung zu einem späteren Zeitpunkt abgeschlossen wird, meldet der Dienstanbieter den Abschluss, indem er eine Rückruf Prozedur aufführt, die TAPI ursprünglich in der Initialisierungs Sequenz bereitgestellt hat.

-   Asynchrone Vorgänge haben einen Parameter mit dem Namen " *dwrequestid* " des definierten Typs " [drv \_ RequestId](./drv-requestid.md) " als ersten Parameter. Ein solcher Vorgang führt einen Teil seiner Verarbeitung im Funktions aufrub und den Rest der Verarbeitung in einem unabhängigen Ausführungs Thread aus, nachdem der Funktions Aufrufwert zurückgegeben wurde. Wenn die Funktion zurückgegeben wird, gibt Sie entweder ein negatives Fehler Ergebnis oder die (positive) *dwrequestid* zurück, die im Funktions aufrufsbefehl ausgegeben wurde. Das negative Fehler Ergebnis zeigt an, dass der Vorgang beendet wurde (und fehlgeschlagen ist). Die zurückgegebene positive *dwrequestid* gibt an, dass der Vorgang im unabhängigen Thread fortgesetzt wird. In einem solchen Fall ruft der Dienstanbieter schließlich die asynchrone [**\_ Abschluss**](/windows/win32/api/tspi/nc-tspi-async_completion) Prozedur auf und übergibt dabei die *dwrequestid* und einen Ergebniscode, um das Ergebnis des Vorgangs anzuzeigen. Der Ergebniscode ist 0 (null) für Erfolg oder einer der gleichen (negativen) Fehler Ergebnisse. In jedem Fall darf der Dienstanbieter niemals NULL oder einen anderen positiven Wert als " *dwrequestid* " aus einer Funktion zurückgeben, die als asynchron festgelegt ist, da dies zu unerwarteten Ergebnissen führen kann. Dienstanbieter sollten vor der Rückgabe einer asynchronen Funktion immer Eingabedaten aus dem Anwendungs Speicher in den Speicher des Dienstanbieters kopieren.
-   Bei synchronen Vorgängen ist *dwrequestid* nicht als erster Parameter vorhanden. Ein solcher Vorgang führt die gesamte Verarbeitung im Ausführungs Thread des Aufrufers durch und gibt das Endergebnis zurück, wenn es zurückgegeben wird. Das Ergebnis ist 0 (null) für Erfolg oder ein negativer Fehlercode für den Fehler. Der Dienstanbieter ruft den asynchronen [**\_ Abschluss**](/windows/win32/api/tspi/nc-tspi-async_completion) nicht für synchrone Vorgänge auf.

Es ist interessant, die zeitliche Steuerung eines "Abschluss"-Rückrufs in Bezug auf die Rückgabe der ursprünglichen Anforderung zu überprüfen. Eine typische asynchrone Anforderung wird vom Dienstanbieter wie im folgenden Pseudocode implementiert:

``` syntax
Some_request(Request_ID, ...) {
  check parameters for validity
  check device state for validity
  store Request_ID for Completion Interrupt Handler's use
  manipulate device registers to start physical operation
  return Request_ID  // to indicate asynch operation
}
Operation Completion Interrupt Handler: {
  if operation was successful then
    call "completion" callback passing Request_ID and "success"
  else
    call "completion" callback passing Request_ID and "error num"
  endif
}
```

Wenn der Vorgang sehr schnell abgeschlossen wird (oder wenn die ursprüngliche Anforderung sehr langsam zurückgegeben wird), kann es vorkommen, dass der Interrupt-Handler, der ausgeführt wird, wenn ein physischer Vorgang abgeschlossen wird, ausgelöst werden kann, bevor die ursprüngliche Anforderung an die Anwendung oder sogar an TAPI zurückgegeben wird Dieses Verhalten ist zulässig. TAPI stellt sicher, dass die endgültige Abschluss Benachrichtigung an die Anwendung übermittelt wird, nachdem die ursprüngliche Anforderung zurückgegeben wurde.

**TAPI 2. x:** Listet den Status auf, ob jede Funktion synchron oder asynchron in der [TAPI-schnell Funktionsreferenz](./tapi-quick-function-reference.md)auftritt.

 

 
