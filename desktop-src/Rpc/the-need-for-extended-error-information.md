---
title: Der Bedarf an erweiterten Fehlerinformationen
description: Eine wesentliche Schwierigkeit bei der Problembehandlung von RPC-Problemen ist die Zuordnung eines RPC-Fehlercodes zum zugrunde liegenden Problem.
ms.assetid: aef3bcd6-ecaa-4639-b765-da90db6ddf82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d82fbbcaf0fac427b2bf64fbacbf1e85aeb4d06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036700"
---
# <a name="the-need-for-extended-error-information"></a>Der Bedarf an erweiterten Fehlerinformationen

Eine wesentliche Schwierigkeit bei der Problembehandlung von RPC-Problemen ist die Zuordnung eines RPC-Fehlercodes zum zugrunde liegenden Problem. Ein Konfigurationsfehler oder ein Netzwerkproblem kann dazu führen, dass eine oder mehrere Arbeitsstationen RPC \_ S- \_ \* Fehler empfangen. diese Arbeitsstation kann jedoch nur den Fehler anzeigen, in eine Phrase schreiben oder Sie in einer Protokolldatei speichern. Je nachdem, welcher Ansatz verwendet wird, sind die Personen, die das Problem beheben, von wesentlichen Informationen ausgeschlossen:

-   Der Fehler ist aufgetreten. Dies ist möglicherweise auf dem lokalen Computer, auf einem Remote Computer, der vom lokalen Computer aufgerufen wurde, oder auf einem Remote Computer, der von einem anderen Remote Computer aufgerufen wurde, aufgetreten.
-   Der ursprüngliche Fehlercode, der das Problem verursacht hat. Um dem OSF-Standard zu entsprechen, ordnet MS RPC Fehlercodes RPC- \_ e- \_ \* Codes zu. RPC \_ \_ \* -e-Codes sind jedoch zu generisch und bieten wenig nützliche Informationen zur Problembehandlung.
-   Alle Kontextinformationen im Zusammenhang mit dem Auftreten des Problems. Bei nicht-RPC-Fehlern können debuggger den Prozess Abbrechen und den Kontext untersuchen, in dem der Fehler aufgetreten ist. RPC-Fehler werden oft von einem Remote Prozess oder Computer generiert, der die Verarbeitung nach dem Zurückgeben des Fehlers fortsetzt und jeden Kontext in Bezug auf den Fehler überschreibt.

 

 




