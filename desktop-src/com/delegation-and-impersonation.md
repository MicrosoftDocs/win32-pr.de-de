---
title: Delegierung und Identitätswechsel
description: In Client-/Serverszenarien ist es üblich, dass ein Server einen anderen Server aufruft, um eine Aufgabe im Auftrag eines Clients auszuführen. Die Situation, in der ein Server die Autorität erhält, im Auftrag eines Clients zu agieren, wird als Delegierung bezeichnet.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00f878c7bc0a37e7d60c246550ff404ed4d0c31312610ab63d1863b34aa52be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919475"
---
# <a name="delegation-and-impersonation"></a>Delegierung und Identitätswechsel

In Client-/Serverszenarien ist es üblich, dass ein Server einen anderen Server aufruft, um eine Aufgabe im Auftrag eines Clients auszuführen. Die Situation, in der ein Server die Autorität erhält, im Auftrag eines Clients zu agieren, wird als *Delegierung* bezeichnet.

Aus Sicherheitssicht ergeben sich zwei Probleme in Bezug auf die Delegierung:

-   Was sollte der Server tun dürfen, wenn er im Auftrag des Clients handelt?
-   Welche Identität wird vom Server angezeigt, wenn er andere Server im Namen eines Clients aufruft?

Um diese Probleme zu beheben, bietet COM die folgenden Funktionen. Der Client kann eine *Identitätswechselebene* festlegen, die bestimmt, in welchem Umfang der Server als Client fungieren kann. Wenn der Client dem Server genügend Autorität erteilt, kann der Server die *Identität* des Clients annehmen (so als ob er angenommen wird). Beim Annehmen der Clientidentität erhält der Server nur Zugriff auf die Objekte oder Ressourcen, für die der Client über die Berechtigung zum Verwenden verfügt. Der Server, der als Client fungiert, kann es auch *ermöglichen,* seine eigene Identität zu maskieren und die Identität des Clients in Aufrufen anderer COM-Komponenten zu pro projectieren.

![Diagramm, das zeigt, wie der Server, der als Client fungiert, die Verleumdung aktivieren kann.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

Betrachten Sie das in der obigen Abbildung dargestellte Szenario, in dem A und B Prozesse auf einem anderen Computer als C sind. Prozess A ruft B auf, und B ruft C auf. Client A legt die Identitätswechselebene fest. B legt die Verleumdungsfunktion fest. Wenn A eine Identitätswechselebene festlegt, die den Identitätswechsel zulässt, kann B die Identität von A annehmen, wenn C im Namen von A aufgerufen wird. Die Identität, die für die Verarbeitung von C angezeigt wird, ist entweder die Identität von A oder die Identität von B, je nachdem, ob die Verleumdung von B aktiviert wurde. Wenn die Verleumdung aktiviert ist, entspricht die identität, die für die Verarbeitung von C angezeigt wird, der Identität von A. Wenn die Verleumdung nicht aktiviert ist, wird die Identität von B in C angezeigt.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Identitätswechsel](impersonation.md)
-   [Identitätswechselebenen](impersonation-levels.md)
-   [Cloaking](cloaking.md)

 

 




