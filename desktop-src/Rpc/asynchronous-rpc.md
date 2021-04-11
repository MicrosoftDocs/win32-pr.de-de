---
title: Asynchroner RPC
description: Bei asynchronem Remote Prozedur Aufruf (RPC) handelt es sich um eine Microsoft-Erweiterung, die verschiedene Einschränkungen des herkömmlichen RPC-Modells behandelt, wie in Open Software Foundation \ 8211; DCE (verteilte Computing Environment) definiert.
ms.assetid: 2586c10e-8284-419f-a200-4f6b11953688
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, asynchroner RPC
- asynchroner RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ac79a30fd01aeba1efb3cbd2b7cc741f26238
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102127"
---
# <a name="asynchronous-rpc"></a>Asynchroner RPC

Bei asynchronem Remote Prozedur Aufruf (RPC) handelt es sich um eine Microsoft-Erweiterung, die verschiedene Einschränkungen des herkömmlichen RPC-Modells behandelt, wie von der Open Software Foundation – verteilten Computing-Umgebung (OSF-DCE) definiert. Der asynchrone RPC trennt einen Remote Prozedur Aufruf von seinem Rückgabewert, der die folgenden Einschränkungen von herkömmlichem, synchronem RPC auflöst:

-   **Mehrere ausstehende Aufrufe von einem Single Thread-Client.** Im herkömmlichen RPC-Modell wird ein Client in einem Remote Prozedur Aufruf blockiert, bis der Aufruf zurückgegeben wird. Dadurch wird verhindert, dass ein Client mehrere ausstehende Aufrufe hat, während der Thread weiterhin für andere Aufgaben verfügbar ist.
-   **Langsame oder verzögerte Clients.** Ein Client, der langsam Daten erzeugt, möchte möglicherweise einen Remote Prozedur Aufrufvorgang mit anfänglichen Daten ausführen und dann bei der Erstellung zusätzliche Daten bereitstellen. Dies ist bei herkömmlichem (synchronen) RPC nicht möglich.
-   **Langsame oder verzögerte Server.** Ein Remote Prozedur Aufruf, der lange Zeit in Anspruch nimmt, bindet den dispatchthread für die Dauer der Aufgabe ein. Mit dem asynchronen RPC kann der Server einen separaten (asynchronen) Vorgang starten, um die Anforderung zu verarbeiten und die Antwort zurücksenden, wenn Sie verfügbar ist. Der Server kann die Antwort auch inkrementell senden, wenn die Ergebnisse verfügbar werden, ohne dass ein Verteilungs Thread für die Dauer des Remote Aufrufes gebunden werden muss. Durch die asynchrone Client Anwendung können Sie verhindern, dass ein langsamer Server eine Client Anwendung unnötig bindet.
-   **Übertragung großer Datenmengen.** Bei der Übertragung großer Datenmengen zwischen Client und Server (vor allem über langsame Verbindungen) werden sowohl der Client Thread als auch der Server-Manager-Thread für die Dauer der Übertragung verbunden. Bei asynchronem RPC und Pipes kann die Datenübertragung inkrementell erfolgen, ohne dass der Client oder der Server andere Tasks ausführen muss.

Sie nutzen asynchrone RPC-Mechanismen, indem Sie Funktionen mit dem \[ [**Async**](/windows/desktop/Midl/async) -Attribut deklarieren \] . Da Sie diese Deklaration in einer Attribut Konfigurationsdatei (ACF) vornehmen, müssen Sie keine Änderungen an der IDL-Datei (Interface Definition Language) vornehmen. asynchronen RPC hat keine Auswirkung auf das Wire-Protokoll (wie die Daten zwischen Client und Server übertragen werden). Dies bedeutet, dass sowohl synchrone als auch asynchrone Clients mit einer asynchronen Serveranwendung kommunizieren können.

Dieser Abschnitt enthält eine Übersicht über die Entwicklung verteilter Anwendungen mit asynchronem RPC. Die Übersicht wird in den folgenden Abschnitten dargestellt:

-   [Deklarieren von asynchronen Funktionen](declaring-asynchronous-functions.md)
-   [Client seitiges asynchrones RPC](client-side-asynchronous-rpc.md)
-   [Server seitiges asynchrones RPC](server-side-asynchronous-rpc.md)
-   [Kausale Reihenfolge von asynchronen Aufrufen](causal-ordering-of-asynchronous-calls.md)
-   [Fehlerbehandlung](error-handling.md)
-   [Asynchroner RPC über das Named Pipe-Protokoll](asynchronous-rpc-over-the-named-pipe-protocol.md)
-   [Verwenden von asynchronem RPC mit DCE-Pipes](using-asynchronous-rpc-with-dce-pipes.md)
-   [Asynchroner DCOM](asynchronous-dcom.md)

 

 