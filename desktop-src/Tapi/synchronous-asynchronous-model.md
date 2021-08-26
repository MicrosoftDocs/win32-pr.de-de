---
description: Die interaktive Art der Telefonie erfordert, dass TAPI eine Echtzeitbetriebsumgebung ist.
ms.assetid: b8512588-ec28-4fbe-b47f-b900e2dba1f2
title: Synchrones/asynchrones Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354bc8e32cdd1bb2bcefac0fe3e4d77361f3be9e37cd6a1549aa157d4b997f43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975520"
---
# <a name="synchronousasynchronous-model"></a>Synchrones/asynchrones Modell

Die interaktive Art der Telefonie erfordert, dass TAPI eine Echtzeitbetriebsumgebung ist. Viele der TAPI-Funktionen müssen schnell abgeschlossen werden und ihre Ergebnisse synchron an die Anwendung zurückgeben. Andere Funktionen (z. B. Wählen) können möglicherweise nicht so schnell abgeschlossen werden und funktionieren daher asynchron.

Telefonievorgänge werden entweder synchron oder asynchron abgeschlossen. Diese beiden Modelle unterscheiden sich wie folgt. *Synchrone* Funktionen führen die gesamte Anforderung aus, bevor der Thread des Aufrufers vom Funktionsaufruf zurückgeben darf. *Asynchrone* Funktionen geben zurück, bevor die Anforderung vollständig ausgeführt wurde. Wenn die asynchrone Anforderung später abgeschlossen wird, meldet der Dienstanbieter den Abschluss, indem er eine Rückrufprozedur aufruft, die TAPI ursprünglich früh in der Initialisierungssequenz bereitgestellt hat.

-   Asynchrone Vorgänge verfügen über einen Parameter namens *dwRequestID* des definierten [Typs DRV \_ REQUESTID](./drv-requestid.md) als ersten Parameter. Ein solcher Vorgang führt einen Teil seiner Verarbeitung im Funktionsaufruf und den Rest der Verarbeitung in einem unabhängigen Ausführungsthread aus, nachdem der Funktionsaufruf zurückgegeben wurde. Wenn die Funktion zurückgegeben wird, gibt sie entweder ein negatives Fehlerergebnis oder die (positive) *dwRequestID* zurück, die im Funktionsaufruf übergeben wurde. Das negative Fehlerergebnis gibt an, dass der Vorgang abgeschlossen (und fehlgeschlagen) ist. Die positive *dwRequestID gibt* an, dass der Vorgang im unabhängigen Thread fortgesetzt wird. In einem solchen Fall ruft der Dienstanbieter schließlich die [**ASYNC \_ COMPLETION-Prozedur**](/windows/win32/api/tspi/nc-tspi-async_completion) auf und überträgt *die dwRequestID* und einen Ergebniscode, um das Ergebnis des Vorgangs anzugeben. Der Ergebniscode ist 0 (null) für den Erfolg oder einer der gleichen (negativen) Fehlerergebnisse. In jedem Fall darf der Dienstanbieter niemals null oder einen anderen positiven Wert als *dwRequestID* von einer Funktion zurückgeben, die als asynchron festgelegt ist, da dies zu unerwarteten Ergebnissen führen kann. Dienstanbieter sollten eingabedaten immer aus dem Anwendungsspeicher in den Speicher des Dienstanbieters kopieren, bevor sie von einer asynchronen Funktion zurückkehren.
-   Synchrone Vorgänge haben *dwRequestID nicht* als ersten Parameter. Ein solcher Vorgang führt die vollständige Verarbeitung im Ausführungsthread des Aufrufers durch und gibt das Endergebnis zurück, wenn er zurückgegeben wird. Das Ergebnis ist 0 (null) für den Erfolg oder ein negativer Fehlercode für einen Fehler. Der Dienstanbieter aufruft [**ASYNC \_ COMPLETION nicht**](/windows/win32/api/tspi/nc-tspi-async_completion) für synchrone Vorgänge.

Es ist interessant, den Zeitpunkt eines "Abschluss"-Rückrufs relativ zum Zeitpunkt der Rückgabe der ursprünglichen Anforderung zu berücksichtigen. Eine typische asynchrone Anforderung wird vom Dienstanbieter wie im folgenden Pseudocode implementiert:

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

Wenn der Vorgang sehr schnell abgeschlossen wird (oder die ursprüngliche Anforderung sehr langsam zurückgegeben wird), kann der Interrupthandler, der nach Abschluss eines physischen Vorgangs ausgeführt wird, möglicherweise ausgelöst werden, bevor die ursprüngliche Anforderung an die Anwendung oder sogar an TAPI zurückgegeben wird. Dieses Verhalten ist zulässig. TAPI garantiert, dass die Benachrichtigung über den endgültigen Abschluss an die Anwendung übermittelt wird, nachdem die ursprüngliche Anforderung zurückgegeben wurde.

**TAPI 2.x:** Listet auf, welcher Status, ob jede Funktion synchron oder asynchron abgeschlossen wird, in [der TAPI-Kurzfunktionsreferenz angezeigt wird.](./tapi-quick-function-reference.md)

 

 
