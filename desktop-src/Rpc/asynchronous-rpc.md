---
title: Asynchroner RPC
description: Ein asynchroner Remoteprozeduraufruf (RPC) ist eine Microsoft-Erweiterung, die mehrere Einschränkungen des herkömmlichen RPC-Modells behandelt, wie von Open Software Foundation \ 8211;Distributed Computing Environment (OSF-DCE) definiert.
ms.assetid: 2586c10e-8284-419f-a200-4f6b11953688
keywords:
- Remoteprozeduraufruf RPC , beschrieben, asynchroner RPC
- asynchroner RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f4a5f160054f78f0a5737993d1a030957af930ab036e73dbcea0a039125964
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023540"
---
# <a name="asynchronous-rpc"></a>Asynchroner RPC

Ein asynchroner Remoteprozeduraufruf (RPC) ist eine Microsoft-Erweiterung, die mehrere Einschränkungen des herkömmlichen RPC-Modells adressiert, wie von der Open Software Foundation –Distributed Computing Environment (OSF-DCE) definiert. Asynchroner RPC trennt einen Remoteprozeduraufruf von seinem Rückgabewert, wodurch die folgenden Einschränkungen des herkömmlichen, synchronen RPC behoben werden:

-   **Mehrere ausstehende Aufrufe von einem Singlethreadclient.** Im herkömmlichen RPC-Modell wird ein Client in einem Remoteprozeduraufruf blockiert, bis der Aufruf zurückgegeben wird. Dadurch wird verhindert, dass ein Client mehrere ausstehende Aufrufe hat, während sein Thread weiterhin für andere Arbeit verfügbar ist.
-   **Langsame oder verzögerte Clients.** Ein Client, der nur langsam Daten erzeugt, kann einen Remoteprozeduraufruf mit Anfangsdaten durchführen und dann zusätzliche Daten bereitstellen, während er erstellt wird. Dies ist bei herkömmlichem (synchronen) RPC nicht möglich.
-   **Langsame oder verzögerte Server.** Ein Remoteprozeduraufruf, der lange dauert, bindet den Dispatchthread für die Dauer der Aufgabe. Mit asynchronem RPC kann der Server einen separaten (asynchronen) Vorgang starten, um die Anforderung zu verarbeiten und die Antwort zurückzusenden, wenn sie verfügbar ist. Der Server kann die Antwort auch inkrementell senden, wenn Ergebnisse verfügbar werden, ohne dass für die Dauer des Remoteaufrufs ein Dispatchthread gebunden werden muss. Indem Sie die Clientanwendung asynchron gestalten, können Sie verhindern, dass ein langsamer Server eine Clientanwendung unnötig bindet.
-   **Übertragung großer Datenmengen.** Bei der Übertragung großer Datenmengen zwischen Client und Server, insbesondere bei langsamen Verknüpfungen, wird sowohl der Clientthread als auch der Server-Managerthread für die Dauer der Übertragung verbunden. Mit asynchronem RPC und Pipes kann die Datenübertragung inkrementell erfolgen, ohne dass der Client oder Server daran gehindert wird, andere Aufgaben auszuführen.

Sie nutzen asynchrone RPC-Mechanismen, indem Sie Funktionen mit dem \[ [**asynchronen**](/windows/desktop/Midl/async) Attribut deklarieren. \] Da Sie diese Deklaration in einer Attributkonfigurationsdatei (ACF) vornehmen, müssen Sie keine Änderungen an der IDL-Datei (Interface Definition Language) vornehmen. asynchroner RPC hat keine Auswirkungen auf das Wire Protocol (wie die Daten zwischen Client und Server übertragen werden). Dies bedeutet, dass sowohl synchrone als auch asynchrone Clients mit einer asynchronen Serveranwendung kommunizieren können.

Dieser Abschnitt bietet eine Übersicht über die Entwicklung verteilter Anwendungen mithilfe von asynchronen RPC. Die Übersicht wird in den folgenden Abschnitten dargestellt:

-   [Deklarieren asynchroner Funktionen](declaring-asynchronous-functions.md)
-   [Clientseitiger asynchroner RPC](client-side-asynchronous-rpc.md)
-   [Serverseitiger asynchroner RPC](server-side-asynchronous-rpc.md)
-   [Kausale Reihenfolge asynchroner Aufrufe](causal-ordering-of-asynchronous-calls.md)
-   [Fehlerbehandlung](error-handling.md)
-   [Asynchroner RPC über das Named Pipe-Protokoll](asynchronous-rpc-over-the-named-pipe-protocol.md)
-   [Verwenden von asynchronen RPC mit DCE Pipes](using-asynchronous-rpc-with-dce-pipes.md)
-   [Asynchroner DCOM](asynchronous-dcom.md)

 

 