---
title: Ändern des Bereichs oder Typs einer Gruppe
description: In diesem Thema wird gezeigt, wie der Bereich einer Gruppe oder der Typ in Domänen im einheitlichen Modus geändert wird.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- Gruppen anzeigen, Ändern des Gültigkeits Bereichs oder des Typs einer Gruppe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707206"
---
# <a name="changing-a-groups-scope-or-type"></a>Ändern des Bereichs oder Typs einer Gruppe

Das Ändern eines Gruppen Bereichs oder Typs ist in Domänen mit gemischtem Modus nicht zulässig. Die folgenden Konvertierungen sind jedoch in Domänen im einheitlichen Modus zulässig:

Globale Gruppe in universelle Gruppe: Dies ist nur zulässig, wenn die globale Gruppe nicht Mitglied einer anderen globalen Gruppe ist.

Lokale Domänen Gruppe zu universeller Gruppe: die zu konvertierende lokale Domänen Gruppe darf keine andere lokale Domänen Gruppe enthalten.

Universelle Gruppe in globale oder lokale Domänen Gruppe: für die Konvertierung in eine globale Gruppe kann die zu konvertierende universelle Gruppe keine Benutzer oder globalen Gruppen aus einer anderen Domäne enthalten. Bei der Konvertierung in eine lokale Domänen Gruppe kann die zu konvertierende universelle Gruppe nicht Mitglied einer universellen Gruppe oder einer lokalen Gruppe einer Domäne aus einer anderen Domäne sein.

Im einheitlichen Modus kann ein Gruppentyp zwischen Sicherheitsgruppen und Verteiler Gruppen frei konvertiert werden.

Beachten Sie, dass eine Änderung des Bereichs oder Typs die Zugriffs Steuerungs Einträge (ACEs), die diese Gruppe enthalten, beeinträchtigen kann, wenn eine Gruppe zum Festlegen der Zugriffs Steuerung verwendet wird. Das Sicherheitssystem ignoriert ACEs, die Gruppen enthalten, die keine Sicherheitsgruppen sind.

 

 




