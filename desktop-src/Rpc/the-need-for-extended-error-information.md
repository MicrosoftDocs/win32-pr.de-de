---
title: Notwendigkeit erweiterter Fehlerinformationen
description: Ein Hauptproblem bei der Problembehandlung von RPC-Problemen ist die Zuordnung eines RPC-Fehlercodes zum zugrunde liegenden Problem.
ms.assetid: aef3bcd6-ecaa-4639-b765-da90db6ddf82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce13e2cb30c7cd9f2db4d7f518eb0a747cd15b2ba1ff7962cf5f41fbc9cf552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016800"
---
# <a name="the-need-for-extended-error-information"></a>Notwendigkeit erweiterter Fehlerinformationen

Ein Hauptproblem bei der Problembehandlung von RPC-Problemen ist die Zuordnung eines RPC-Fehlercodes zum zugrunde liegenden Problem. Ein Konfigurationsfehler oder Netzwerkproblem kann dazu führen, dass mindestens eine Arbeitsstation \_ RPC-S-Fehler empfängt. Auf \_ \* dieser Arbeitsstation kann der Fehler jedoch nur angezeigt, paraphrasiert oder in einer Protokolldatei gespeichert werden. Unabhängig davon, welcher Ansatz verwendet wird, erhält die Person, die das Problem behandeln soll, wichtige Informationen:

-   Die Stelle, an der der Fehler aufgetreten ist. Dies kann auf dem lokalen Computer, auf einem Remotecomputer, der vom lokalen Computer aufgerufen wird, oder auf einem Remotecomputer aufgetreten sein, der von einem anderen Remotecomputer aufgerufen wird.
-   Der ursprüngliche Fehlercode, der das Problem verursacht hat. Um dem OSF-Standard zu entsprechen, ordnet MS RPC Fehlercodes \_ RPC-S-Codes \_ \* zu. \_ \_ \* RPC-S-Codes sind jedoch zu generisch und bieten wenig nützliche Informationen zur Problembehandlung.
-   Alle Kontextinformationen im Zusammenhang mit dem Auftreten des Problems. Bei Nicht-RPC-Fehlern können Debugger den Prozess beenden und den Kontext untersuchen, in dem der Fehler aufgetreten ist. RPC-Fehler werden häufig von einem Remoteprozess oder Computer generiert, der die Verarbeitung nach der Rückgabe des Fehlers fortsetzt und alle Kontexte überschreibt, die sich auf den Fehler beziehen.

 

 




