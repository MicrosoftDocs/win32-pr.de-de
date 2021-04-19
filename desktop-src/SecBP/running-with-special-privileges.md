---
description: Einige Funktionen erfordern spezielle Berechtigungen, um ordnungsgemäß auszuführen.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Ausführen mit besonderen Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be662d187ef27c7afc12b031f2d8de225d34c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369043"
---
# <a name="running-with-special-privileges"></a>Ausführen mit besonderen Berechtigungen

Einige Funktionen erfordern spezielle [Berechtigungen](/windows/desktop/SecAuthZ/privileges) , um ordnungsgemäß auszuführen. In einigen Fällen kann die Funktion nur von bestimmten Benutzern oder von Mitgliedern bestimmter Gruppen ausgeführt werden. Die häufigste Anforderung ist, dass der Benutzer ein lokaler Administrator ist. Für andere Funktionen ist es erforderlich, dass das Konto des Benutzers über bestimmte Berechtigungen verfügt.

Um die Möglichkeit zu verringern, dass nicht autorisierter Code die Kontrolle erhält, sollte das System mit den geringsten Berechtigungen ausgeführt werden. Anwendungen, die Funktionen anrufen müssen, die besondere Berechtigungen erfordern, können das System für Angriffe durch Hacker offenlegen. Solche Anwendungen sollten so konzipiert sein, dass Sie für kurze Zeiträume ausgeführt werden und den Benutzer über die betroffenen Sicherheitsrisiken informieren.

Informationen dazu, wie Sie unterschiedliche Benutzer ausführen und Berechtigungen in Ihrer Anwendung aktivieren, finden Sie in den folgenden Themen:<dl>

[Ausführen mit Administrator Rechten](running-with-administrator-privileges.md)  
[Benutzer werden zur Anmelde Informationen aufgefordert](asking-the-user-for-credentials.md)  
[Ändern von Berechtigungen in einem Token](changing-privileges-in-a-token.md)  
[Zuweisen von Berechtigungen zu einem Konto](assigning-privileges-to-an-account.md)  
</dl>

 

 
