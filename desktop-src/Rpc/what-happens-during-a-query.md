---
title: Was geschieht während einer Abfrage?
description: In diesem Abschnitt wird beschrieben, wie das Netzwerk die Abfrage verarbeitet, wenn ein 32-Bit-Client in seiner eigenen Domäne nach einem Namen sucht.
ms.assetid: a8a88743-a245-4258-af05-9261c214ab50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7377df4ced562bc166fedbf489724a2a4a042855391db45841b5de5cf5af906
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010428"
---
# <a name="what-happens-during-a-query"></a>Was geschieht während einer Abfrage?

In diesem Abschnitt wird beschrieben, wie das Netzwerk die Abfrage verarbeitet, wenn ein 32-Bit-Client in seiner eigenen Domäne nach einem Namen sucht.

Wenn Ihre Clientanwendung [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)aufruft, versucht der Locator, der sich auf Ihrem Clientcomputer befindet, diese Anforderung zu erfüllen. Wenn im Cache nichts vorhanden ist, wird die Anforderung von RPC an einen Masterlocator weitergeleitet. Wenn der Masterlocator nichts im Cache findet, sendet er die Anforderung mithilfe einer Mailslotübertragung an alle Computer in der Domäne. Wenn eine Übereinstimmung vorliegt, antwortet der Locator auf jedem Computer durch einen gerichteten E-Mail-Slot. (Beispiel: Ein Prozess auf diesem Computer hat die Schnittstelle exportiert.) Die Antworten werden sortiert, und der RPC wird über den Prozesslocator des Clients abgeschlossen, der auf den Clientprozess selbst antwortet.

In einer Domäne sucht der Clientlocator an den folgenden Stellen nach einem Masterlocator:

-   Auf dem primären Domänencontroller
-   Auf jedem Sicherungsdomänencontroller

Wenn keine Übereinstimmung gefunden wird, deklariert sich der Clientlocator selbst als Masterlocator. Daher werden Abfragen übertragen, wenn sie lokal nicht erfüllt werden können.

In einer Arbeitsgruppe verwaltet der Clientlocator einen Cache der Computer, deren Locators übertragen wurden. Sie verwendet die , die am längsten als Masterlocator ausgeführt wurde. Wenn dieser Computer nicht verfügbar ist, wird der nächste Computer mit der längsten Übertragung verwendet usw. Wenn der Client einen Masterlocator benötigt und der Cache leer ist, füllt er den Cache auf, indem er eine spezielle E-Mail-Slotübertragung sendet, die Masterlocators anfordert, um zu antworten. Wenn keine Antworten vorhanden sind, deklariert sich der Clientlocator selbst als Masterlocator und überträgt Abfragen, wenn sie lokal nicht erfüllt werden können.

Dies ändert sich, wenn ihre Clientanwendung ein 16-Bit- oder MS-DOS-basiertes Programm ist. In diesem Fall wird kein Locator auf dem Clientcomputer ausgeführt, und Rpcns1.dll oder Rpcnslm.rpc enthält den Code zum Suchen eines Masterlocators. Alle Anforderungen werden direkt an den Masterlocator weitergeleitet.

Diese Richtlinien gelten für Namen in der Domäne des Clients, z. B. Namen für "/.:/". entryname". Wenn der Client mithilfe von "/.../DOMAIN/entryname;" einen Namen von einer anderen Domäne anfordert, leitet der Clientlocator die Anforderung an die angegebene Domäne weiter, die sie überträgt, wenn sie nicht über die Antwort verfügt. Wenn die Domäne ausfällt oder tatsächlich eine Arbeitsgruppe ist, schlägt die Anforderung fehl.

> [!Note]  
> Beachten Sie Folgendes, wenn Sie mit Einträgen im Namensdienst arbeiten:

 

-   Ein Client kann die Syntax "/.../DOMAIN/entryname" nicht verwenden, um einen Eintrag in seiner eigenen Domäne zu finden. Verwenden Sie die Syntax "/.:/". entryname". Sie können jedoch "/.../DOMAIN/entryname" verwenden, um einen Eintrag in einer anderen Domäne zu suchen.
-   Der Domänenname in "/.../DOMAIN/entryname" muss groß geschrieben werden. Bei der Suche nach einer Übereinstimmung wird beim Locator die Groß-/Kleinschreibung beachtet.
-   Bei Locator-Eintragsnamen wird auch die Groß-/Kleinschreibung beachtet, es darf jedoch kein Groß-/Kleinschreibung sein.
-   Wenn der Client "/.:/" verwendet entryname"-Syntax, sucht der Locator nicht nach Einträgen in anderen Domänen, auch wenn sie über eine Vertrauensstellung mit der Anmeldedomäne verfügen.
-   Broadcasts sind nicht lanübergreifend segmentübergreifend (z. B. Subnetze). Daher ist die Nützlichkeit des Locators in einer Organisation mit mehreren Subnetzen eingeschränkt.

 

 




