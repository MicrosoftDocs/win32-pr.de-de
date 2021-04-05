---
title: Beispiele für inkompatible Änderungen
description: 'Beim Umgang mit nicht kompatiblen Änderungen ist die bedauerliche Faustregel wie folgt: jede Änderung kann rückwärts inkompatibel sein, es sei denn, Sie ist gut verständlich.'
ms.assetid: 5b893d79-b81d-4ede-8d49-71d85219c497
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9498e5c71c7ce9690da0969f234fbb9d094eca50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037117"
---
# <a name="examples-of-incompatible-changes"></a>Beispiele für inkompatible Änderungen

Beim Umgang mit nicht kompatiblen Änderungen ist die unglücklichste Faustregel wie folgt: jede Änderung kann rückwärts inkompatibel sein, es sei denn, Sie ist gut verständlich. Diese Regel erfordert Kenntnisse der NDR-Regeln. Wenn Sie nicht wissen, was der NDR ist, nehmen Sie keine Änderungen vor. Beispiele für Änderungen, die normalerweise zu einer Zugriffsverletzung in der Anwendung führen, oder eine fehlerhafte \_ \_ Stubdaten \_ Ausnahme, die von der Mars Hall-Engine ausgelöst wird, lauten wie folgt:

-   Hinzufügen einer neuen Methode in der Mitte der alten Methoden.
-   Hinzufügen oder Entfernen von Parametern aus einer Methode.
-   Ändern eines Attributs, z. b. eines Zeiger Attributs: ändern \[ \] von Ref in \[ Unique \] oder \[ ptr \] oder umgekehrt. Jeder Zeigertyp weist eine andere Wire-Darstellung auf.
-   Ändern der Größe der Daten: von "Short" zu "Long", von "char" zu "WCHAR \_ t" (Unicode), durch Hinzufügen eines Felds zu einer Struktur, Ändern der Größe eines Arrays mit fester Größe.
-   Hinzufügen von Union-Waffen zu einer Union mit einer DEFAULT-Klausel.

Einige fehlerhafte Änderungen oder unbeabsichtigte Konflikte zwischen einem Client und einem Server können wie folgt auftreten:

-   Ändern eines Members eines Verbund Typs, wie z. b. einer Struktur oder eines Arrays. Wenn sich z. b. eine Client- \_ ID von einer Ganzzahl in eine GUID ändert, wird eine Client \_ Daten Satzstruktur mit dem Feld "Client-ID" nicht \_ kompatibel. Dies ist möglicherweise schwierig zu erkennen, wenn Sie über mehrere Ebenen der Einbettung in einen tatsächlichen Remote Parametertyp kaskadiert werden.
-   Ändern eines importierten Typs. Der Typ stammt möglicherweise aus einer anderen Komponente, die nicht direkt Remote ist. Daher wurde die Änderung als kompatibel betrachtet.
-   \#Die Verwendung von ifdef in einer IDL-Datei ist eine gute Idee für die Verwendung von ifdef-Typdefinitionen in einer IDL-Datei – es wird ein Notfall darauf gewartet. Aufgrund von Builds oder anderen Störungen wird ein Client unweigerlich mit einem anderen Satz von Definitionen kompiliert als der Server, und er ist schließlich inkompatibel.

 

 




