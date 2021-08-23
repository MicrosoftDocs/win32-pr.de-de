---
title: Replikationsverhalten in Active Directory Domain Services
description: Das Replikationsverhalten ist konsistent und vorhersagbar. Bei einer Reihe von Änderungen an einem bestimmten Replikat kann das Ergebnis \8212 vorhergesagt werden. Die Änderungen werden an alle anderen Replikate propagiert.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, Replikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7548ecf146f1d23b97b9db6a0307b21a6c39d359576c2de02285331d165fad4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025138"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a>Replikationsverhalten in Active Directory Domain Services

Das Replikationsverhalten ist konsistent und vorhersagbar. Bei einer Reihe von Änderungen an einem bestimmten Replikat kann das Ergebnis vorhergesagt werden– die Änderungen werden an alle anderen Replikate propagiert. Die Entwicklung eines zuverlässigen allgemeinen Modells zur Vorhersage, wann die Änderungen auf alle anderen Replikate oder auf einem bestimmten Replikat angewendet werden, ist unmöglich, da der zukünftige Zustand des verteilten Systems als Ganzes nicht bekannt ist. Dies wird als "nicht deterministische Latenz" bezeichnet, und Anwendungen, die das Verzeichnis verwenden, müssen dies verstehen und zulassen.

Die Situation ist möglicherweise nicht so komplex. Es gibt nur drei Zustände, die eine Anwendung aufnehmen muss:

-   Versionsveränderung: Keine der Änderungen, die auf ein bestimmtes Quellreplikat angewendet werden, wurde an ein bestimmtes Zielreplikat propagiert. Eine Anwendung, die das Quellreplikat liest, sieht die neue Version der Informationen, während eine Anwendung, die das Ziel liest, die alte Version erkennt (oder nichts, wenn die neuen Informationen zum ersten Mal hinzugefügt wurden). Die Versionsfähnung gilt für alle Verzeichnisdienstverbraucher.
-   Teilaktualisierung: Einige der Änderungen, die auf ein bestimmtes Quellreplikat angewendet werden, wurden an ein bestimmtes Zielreplikat propagiert. Eine Anwendung, die das Quellreplikat liest, sieht die neuen Informationen, während eine Anwendung, die das Ziel liest, eine Mischung aus alten und neuen Informationen erkennt (oder nur einige der neuen Informationen, wenn die neuen Informationen zum ersten Mal hinzugefügt wurden). Die partielle Aktualisierung gilt für Verzeichnisdienstverbraucher, die zwei oder mehr verwandte Objekte verwenden, um ihre Informationen zu speichern.
-   Vollständig replizierter Zustand: Alle Änderungen, die auf ein bestimmtes Quellreplikat angewendet werden, wurden an ein bestimmtes Zielreplikat propagiert. Anwendungen auf den Quell- und Zielreplikaten sehen die gleichen Informationen.

 

 




