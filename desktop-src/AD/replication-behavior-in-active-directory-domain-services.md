---
title: Replikations Verhalten in Active Directory Domain Services
description: Replikations Verhalten ist konsistent und vorhersagbar. Wenn ein bestimmtes Replikat eine Reihe von Änderungen enthält, kann das Ergebnis vorhergesagt werden 8212; die Änderungen werden an alle anderen Replikate weitergegeben.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, Replikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41009a733f99366e499a25baca989f4f28794aea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855387"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a>Replikations Verhalten in Active Directory Domain Services

Replikations Verhalten ist konsistent und vorhersagbar. Wenn ein bestimmtes Replikat eine Reihe von Änderungen enthält, kann das Ergebnis vorhergesagt werden – die Änderungen werden an alle anderen Replikate weitergegeben. Die Entwicklung eines zuverlässigen allgemeinen Modells für die Vorhersage, wann die Änderungen auf alle anderen Replikate oder auf ein bestimmtes Replikat angewendet werden, ist nicht möglich, da der zukünftige Status des verteilten Systems als Ganzes nicht bekannt ist. Dies wird als "nicht deterministische Latenz" bezeichnet, und Anwendungen, die das Verzeichnis verwenden, müssen es verstehen und zulassen.

Die Situation ist nicht so komplex, dass Sie möglicherweise angezeigt wird. Es gibt nur drei Zustände, die eine Anwendung erfüllen muss:

-   Versions Schiefe: keine der Änderungen, die auf ein bestimmtes Quell Replikat angewendet werden, wurde an ein bestimmtes Ziel Replikat weitergegeben. Eine Anwendung, die das Quell Replikat liest, sieht die neue Version der Informationen, während eine Anwendung, die das Ziel liest, die alte Version sieht (oder nichts, wenn die neuen Informationen zum ersten Mal hinzugefügt wurden). Die Versions Neigung gilt für alle Verzeichnis Dienstanbieter.
-   Teilweises Update: einige der Änderungen, die auf ein bestimmtes Quell Replikat angewendet werden, wurden an ein bestimmtes Ziel Replikat weitergegeben. Bei einer Anwendung, die das Quell Replikat liest, werden die neuen Informationen angezeigt, während eine Anwendung, die das Ziel liest, eine Mischung aus alten und neuen Informationen (oder nur einige der neuen Informationen) sieht, wenn die neuen Informationen zum ersten Mal hinzugefügt wurden. Teil Updates gelten für Verzeichnis Dienstanbieter, die zwei oder mehr verwandte Objekte zum Speichern Ihrer Informationen verwenden.
-   Vollständig replizierter Status: alle Änderungen, die auf ein bestimmtes Quell Replikat angewendet werden, wurden an ein bestimmtes Ziel Replikat weitergegeben. Anwendungen an den Quell-und Ziel Replikaten sehen die gleichen Informationen.

 

 




