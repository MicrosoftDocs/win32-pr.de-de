---
description: Bei einer Zugriffs Überprüfung vergleicht das System die Sicherheitsinformationen im Thread Zugriffs Token mit den Sicherheitsinformationen in der Sicherheits Beschreibung des Objekts.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interaktion zwischen Threads und Sicherungs fähigen Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3e2b18f707ece4d651eeca1c6897bb67aad334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867808"
---
# <a name="interaction-between-threads-and-securable-objects"></a>Interaktion zwischen Threads und Sicherungs fähigen Objekten

Wenn ein Thread versucht, ein Sicherungs [fähiges Objekt](securable-objects.md)zu verwenden, führt das System eine Zugriffs Überprüfung durch, bevor der Thread fortgesetzt werden kann. Bei einer Zugriffs Überprüfung vergleicht das System die Sicherheitsinformationen im [*Zugriffs Token*](/windows/desktop/SecGloss/a-gly) des Threads mit den Sicherheitsinformationen in der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)des Objekts.

-   Das Zugriffs Token enthält [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (Security Identifier, SIDs), die den dem Thread zugeordneten Benutzer identifizieren.
-   Die Sicherheits Beschreibung identifiziert den Besitzer des Objekts und enthält eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL). Die DACL enthält [*Zugriffs Steuerungs Einträge (Access Control Entries*](/windows/desktop/SecGloss/a-gly) , ACEs), von denen jede die Zugriffsrechte angibt, die einem bestimmten Benutzer oder einer Gruppe gewährt oder verweigert werden.

Das System überprüft die DACL des Objekts und sucht nach ACEs, die für die Benutzer-und Gruppen-SIDs aus dem Zugriffs Token des Threads gelten. Das System prüft jeden ACE, bis der Zugriff gewährt oder verweigert wird oder wenn keine weiteren ACEs zum Überprüfen vorhanden sind. Eine [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/a-gly) (ACL) kann mehrere ACEs enthalten, die für die SIDs des Tokens gelten. Wenn dies der Fall ist, häufen sich die von den einzelnen ACE gewährten Zugriffsrechte an. Wenn ein ACE z. b. Lesezugriff auf eine Gruppe gewährt und ein anderer ACE Schreibzugriff für einen Benutzer gewährt, der Mitglied der Gruppe ist, kann der Benutzer sowohl Lese-als auch Schreibzugriff auf das Objekt haben.

In der folgenden Abbildung wird die Beziehung zwischen diesen Sicherheitsinformationen angezeigt:

![Beziehungen zwischen Prozessen, ACEs und DACLs](images/cssec-02.png)

 

 
