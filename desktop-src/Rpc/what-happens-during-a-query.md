---
title: Was geschieht während einer Abfrage?
description: In diesem Abschnitt wird beschrieben, wie das Netzwerk die Abfrage behandelt, wenn ein 32-Bit-Client in seiner eigenen Domäne nach einem Namen sucht.
ms.assetid: a8a88743-a245-4258-af05-9261c214ab50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e26fb9aaef0aac2ff66260d51f756725566dee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206816"
---
# <a name="what-happens-during-a-query"></a>Was geschieht während einer Abfrage?

In diesem Abschnitt wird beschrieben, wie das Netzwerk die Abfrage behandelt, wenn ein 32-Bit-Client in seiner eigenen Domäne nach einem Namen sucht.

Wenn Ihre Client Anwendung [**rpcnsbindingimportbegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)aufruft, versucht der Serverlocatorpunkt, der sich auf dem Client Computer befindet, diese Anforderung zu erfüllen. Wenn im Cache nichts vorhanden ist, wird die Anforderung von RPC an einen masterlocator weiterleiten. Wenn der Master Serverlocatorpunkt nichts im Cache findet, sendet er die Anforderung mithilfe einer e-Mail-Slot-Übertragung an alle Computer in der Domäne. Wenn eine Entsprechung vorliegt, antwortet der Serverlocatorpunkt auf jedem Computer durch einen gerichteten e-Mail-Slot. (Z. b. Wenn ein Prozess auf diesem Computer die Schnittstelle exportiert hat.) Die Antworten werden sortiert, und der RPC-Vorgang wird vom Prozess Locator des Clients abgeschlossen, der dem Client Prozess selbst antwortet.

In einer Domäne sucht der clientlocator an den folgenden Stellen nach einem hauptlocator:

-   Auf dem primären Domänen Controller
-   Auf jedem Sicherungs Domänen Controller

Wenn keine Entsprechung gefunden wird, deklariert sich der clientlocator als hauptlocator. Daher werden Abfragen gesendet, wenn Sie nicht lokal erfüllt werden können.

In einer Arbeitsgruppe behält der clientlocator einen Cache der Computer bei, deren Locators übertragen werden. Er verwendet den, der den längsten als hauptlocator ausgeführt hat. Wenn der Computer nicht verfügbar ist, wird der nächste, längste Broadcast Computer verwendet usw. Wenn der Client einen Master-Serverlocatorpunkt benötigt und der Cache leer ist, wird der Cache durch das Senden einer speziellen e-Mail-Slot-Übertragung aufgefüllt, die die Master-Locators anfordert, Antworten zu erhalten. Wenn keine Antworten vorhanden sind, deklariert sich der clientlocator als hauptlocator und sendet Abfragen, wenn Sie nicht lokal erfüllt werden können.

Dies ändert sich, wenn die Client Anwendung ein 16-Bit-oder MS-DOS-basiertes Programm ist. In diesem Fall wird kein Serverlocatorpunkt auf dem Client Computer ausgeführt, und Rpcns1.dll oder rpcnslm. RPC enthält den Code für die Suche nach einem masterlocator. Alle Anforderungen werden direkt an den masterlocator weitergeleitet.

Diese Richtlinien gelten für Namen in der Domäne des Clients, z. b. Namen für "/.:/ entryname ". Wenn der Client einen Namen aus einer anderen Domäne durch die Verwendung von "/.../Domain/entryname;" anfordert, leitet der clientlocator die Anforderung an die angegebene Domäne weiter, die Sie überträgt, wenn Sie nicht über die Antwort verfügt. Wenn die Domäne nicht ausgeführt wird oder tatsächlich eine Arbeitsgruppe ist, tritt bei der Anforderung ein Fehler auf.

> [!Note]  
> Beachten Sie beim Arbeiten mit Einträgen im Namensdienst Folgendes:

 

-   Ein Client kann die Syntax "/.../Domain/entryname" nicht verwenden, um einen Eintrag in seiner eigenen Domäne zu finden. Verwenden Sie die Syntax "/.:/ entryname ". Sie können jedoch "/.../Domain/entryname" verwenden, um einen Eintrag in einer anderen Domäne zu finden.
-   Der Domänen Name in "/.../Domain/entryname" muss in Großbuchstaben angegeben werden. Wenn Sie nach einer Entsprechung suchen, wird die Groß-/Kleinschreibung beachtet.
-   Bei Locator-Eintrags Namen wird ebenfalls die Groß-/Kleinschreibung beachtet
-   Wenn der Client "/.:/" verwendet. entryname "-Syntax, der Serverlocatorpunkt sucht nicht nach Einträgen in anderen Domänen, auch wenn Sie über eine Vertrauensstellung mit der Anmelde Domäne verfügen.
-   Sendungen überschreiten keine LAN-Segmente (z. b. Subnetze). Daher ist die Nützlichkeit des Locators in einer Organisation mit mehreren Subnetzen eingeschränkt.

 

 




