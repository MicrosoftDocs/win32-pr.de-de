---
description: Bei einer Zugriffsüberprüfung vergleicht das System die Sicherheitsinformationen im Threadzugriffstoken mit den Sicherheitsinformationen im Objektsicherheitsdeskriptor.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interaktion zwischen Threads und sicherungsfähige Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27ab85aa461892d0e6fdf6bdbd9adc8aa7b78a3d9bf1b3896d53ad8e2e236de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670815"
---
# <a name="interaction-between-threads-and-securable-objects"></a>Interaktion zwischen Threads und sicherungsfähige Objekte

Wenn ein Thread versucht, ein sicherungsfähiges Objekt zu [verwenden,](securable-objects.md)führt das System eine Zugriffsüberprüfung durch, bevor der Thread fortgesetzt werden kann. Bei einer Zugriffsüberprüfung vergleicht das System die Sicherheitsinformationen im Zugriffstoken des Threads mit den Sicherheitsinformationen im Sicherheitsdeskriptor [*des Objekts.*](/windows/desktop/SecGloss/s-gly) [](/windows/desktop/SecGloss/a-gly)

-   Das Zugriffstoken enthält [*Sicherheits-IDs*](/windows/desktop/SecGloss/s-gly) (SIDs), die den Benutzer identifizieren, der dem Thread zugeordnet ist.
-   Der Sicherheitsdeskriptor identifiziert den Besitzer des Objekts und enthält eine DACL [*(Discretionary Access Control List).*](/windows/desktop/SecGloss/d-gly) Die DACL enthält [*Zugriffssteuerungseinträge*](/windows/desktop/SecGloss/a-gly) (Access Control Entries, ACEs), die jeweils die Zugriffsrechte angeben, die einem bestimmten Benutzer oder einer bestimmten Gruppe erlaubt oder verweigert werden.

Das System überprüft die DACL des Objekts und sucht nach ACEs, die für die Benutzer- und Gruppen-SIDs aus dem Zugriffstoken des Threads gelten. Das System überprüft jeden ACE, bis der Zugriff gewährt oder verweigert wird oder bis keine aces mehr überprüft werden müssen. Möglicherweise könnte eine [*Zugriffssteuerungsliste*](/windows/desktop/SecGloss/a-gly) (Access Control List, ACL) mehrere ACEs enthalten, die für die SIDs des Tokens gelten. In diesem Fall sammeln sich die von jedem ACE gewährten Zugriffsrechte an. Wenn beispielsweise ein ACE Lesezugriff auf eine Gruppe und ein anderer ACE einem Benutzer, der Mitglied der Gruppe ist, Schreibzugriff gewährt, kann der Benutzer sowohl Lese- als auch Schreibzugriff auf das Objekt haben.

Die folgende Abbildung zeigt die Beziehung zwischen diesen Blöcken von Sicherheitsinformationen:

![Beziehungen zwischen Prozessen, Aces und Dacls](images/cssec-02.png)

 

 
