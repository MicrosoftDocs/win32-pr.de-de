---
title: Beispiele für inkompatible Änderungen
description: Bei inkompatiblen Änderungen lautet die Faustregel, dass jede Änderung abwärtskompatibel sein kann, es sei denn, sie ist sehr gut verstanden.
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0a8736093e8189570026489bc1753145b941b7429b704e2c9c68783ddefef0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930039"
---
# <a name="examples-of-incompatible-changes"></a>Beispiele für inkompatible Änderungen

Beim Umgang mit inkompatiblen Änderungen lautet die Faustregel: Jede Änderung kann abwärtskompatibel sein, es sei denn, sie ist sehr gut verstanden. Diese Regel erfordert Kenntnisse der NDR-Regeln. Wenn Sie nicht wissen, was der NDR ist, nehmen Sie keine Änderungen vor. Beispiele für Änderungen, die in der Regel zu einer Zugriffsverletzung in der Anwendung führen, oder eine BAD STUB DATA EXCEPTION, die von der Marshalling-Engine ausgelöst \_ \_ \_ wird, sind:

-   Hinzufügen einer neuen Methode in der Mitte der alten Methoden.
-   Hinzufügen oder Entfernen von Parametern aus einer Methode.
-   Ändern eines Attributs, z. B. eines Zeigerattributs: Ändern \[ von ref in unique oder \] \[ \] \[ ptr oder \] umgekehrt. Jeder Zeigertyp verfügt über eine andere Wire-Darstellung.
-   Ändern der Größe der Daten: von short in long, von char in wchar t (Unicode), Hinzufügen eines Felds zu einer Struktur, Ändern der Größe eines Arrays \_ mit fester Größe.
-   Hinzufügen von Union-Arms zu einer Union mit einer Standardklausel.

Einige unvorsichtige Änderungen oder unbeabsichtigte Nichtübereinstimmungen zwischen einem Client und einem Server können wie folgt auftreten:

-   Ändern eines Members eines zusammengesetzten Typs, z. B. einer Struktur oder eines Arrays. Wenn sich beispielsweise eine CLIENT-ID von einem integralen in eine GUID ändert, wird eine CLIENT RECORD-Struktur mit \_ \_ dem Feld \_ CLIENT-ID inkompatibel. Dies kann schwierig zu erkennen sein, wenn es durch mehrere Ebenen der Einbettung in einen tatsächlichen Remoteparametertyp kaskadiert wird.
-   Ändern eines importierten Typs. Der Typ kann von einer anderen Komponente kommen, die nicht direkt remote ist, daher wurde die Änderung als kompatibel angenommen.
-   Die Verwendung von ifdef in einer IDL-Datei ist eine schlechte Idee, wenndef-Typdefinitionen in einer IDL-Datei verwendet werden– es wird auf einen Notfall \# gewartet. Aufgrund von Build- oder anderen Störungen wird ein Client mit einem anderen Satz von Definitionen als der Server kompiliert und ist am Ende nicht kompatibel.

 

 




