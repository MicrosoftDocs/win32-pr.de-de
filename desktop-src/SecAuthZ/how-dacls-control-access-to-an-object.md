---
description: Wenn ein Thread versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, gewährt oder verweigert das System den Zugriff.
ms.assetid: dc98b23e-ce42-4d4a-a285-c0b7b5e2a478
title: Funktionsweise von Access Check
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730cc8f63e7d69bf4cb38344f5eda60861d08a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559480"
---
# <a name="how-accesscheck-works"></a>Funktionsweise von Access Check

Wenn ein Thread versucht, auf ein Sicherungs fähiges Objekt zuzugreifen, gewährt oder verweigert das System den Zugriff. Wenn das Objekt nicht über eine freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) verfügt, gewährt das System Zugriff. Andernfalls sucht das System nach [Access Control Einträgen](access-control-entries.md) (ACEs) in der DACL des Objekts, die für den Thread gelten. Jeder ACE in der DACL des Objekts gibt die Zugriffsrechte [an, die](trustees.md)für einen Vertrauens nehmer zugelassen oder verweigert werden. dabei kann es sich um ein Benutzerkonto, ein Gruppenkonto oder eine [*Anmelde Sitzung*](/windows/desktop/SecGloss/l-gly)handeln.

## <a name="dacls"></a>DACLs

Das System vergleicht den Treuhänder in jedem ACE mit den im [Zugriffs Token](access-tokens.md)des Threads identifizierten Treuhändern. Ein Zugriffs Token enthält [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -IDs (SIDs), die den Benutzer und die Gruppenkonten identifizieren, zu denen der Benutzer gehört. Ein Token enthält auch eine [*Anmelde-SID*](/windows/desktop/SecGloss/l-gly) , die die aktuelle Anmelde Sitzung identifiziert. Während einer Zugriffs Überprüfung werden von dem System nicht aktivierte Gruppen-SIDs ignoriert. Weitere Informationen zu aktivierten, deaktivierten und verweigerten SIDs finden Sie unter [SID-Attribute in einem Zugriffs Token](sid-attributes-in-an-access-token.md).

In der Regel verwendet das System das [*primäre Zugriffs Token*](/windows/desktop/SecGloss/p-gly) des Threads, der Zugriff anfordert. Wenn der Thread jedoch die Identität eines anderen Benutzers annimmt, verwendet das System das Identitätswechsel [*Token*](/windows/desktop/SecGloss/i-gly)des Threads.

Das System prüft jeden ACE nacheinander, bis eines der folgenden Ereignisse eintritt:

-   Ein "Zugriff verweigert"-ACE verweigert allen angeforderten [Zugriffsrechten](access-rights-and-access-masks.md) explizit einen der Treuhänder, die im Zugriffs Token des Threads aufgeführt sind.
-   Mindestens ein Zugriffs zulässiger ACEs für Treuhänder, die im Zugriffs Token des Threads aufgeführt sind, gewährt explizit alle angeforderten Zugriffsrechte.
-   Alle Aces wurden geprüft, und es gibt noch mindestens ein angefordertes Zugriffsrecht, das nicht explizit zugelassen wurde. in diesem Fall wird der Zugriff implizit verweigert.

In der folgenden Abbildung wird gezeigt, wie die DACL eines Objekts den Zugriff auf einen Thread zulassen kann, während gleichzeitig der Zugriff verweigert wird.

![DACL, die unterschiedliche Zugriffsrechte für verschiedene Threads erteilt](images/accctrl1.png)

Bei Thread A liest das System ACE 1 und verweigert sofort den Zugriff, da der Zugriffs Verweigerungs-ACE für den Benutzer im Zugriffs Token des Threads gilt. In diesem Fall überprüft das System die Aces 2 und 3 nicht. Für Thread B trifft ACE 1 nicht zu, daher geht das System mit ACE 2 fort, das Schreibzugriff zulässt, und ACE 3, das Lese-und Ausführungs Zugriff ermöglicht.

Da das System die Überprüfung von ACEs beendet, wenn der angeforderte Zugriff explizit erteilt oder verweigert wird, ist die Reihenfolge der ACEs in einer DACL wichtig. Beachten Sie, dass das System möglicherweise den Zugriff auf Thread A erteilt hat, wenn sich die ACE-Reihenfolge im Beispiel unterscheidet. Bei System Objekten definiert das Betriebssystem eine bevorzugte [Reihenfolge von ACEs in einer DACL](order-of-aces-in-a-dacl.md).

 

 
