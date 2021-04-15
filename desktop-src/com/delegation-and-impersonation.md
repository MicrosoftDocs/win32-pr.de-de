---
title: Delegierung und Identitätswechsel
description: In Client-/Serverszenarien ist es üblich, dass ein Server einen anderen Server aufruft, um eine Aufgabe im Auftrag eines Clients auszuführen. Die Situation, in der ein Server die Autorität erhält, im Auftrag eines Clients zu agieren, wird als Delegierung bezeichnet.
ms.assetid: 245bff1a-31d3-49ce-847e-c37d0c96f9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 356708008274bdeb2aa80631bec777fbd02fd38d
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104550047"
---
# <a name="delegation-and-impersonation"></a>Delegierung und Identitätswechsel

In Client-/Serverszenarien ist es üblich, dass ein Server einen anderen Server aufruft, um eine Aufgabe im Auftrag eines Clients auszuführen. Die Situation, in der ein Server die Autorität erhält, im Auftrag eines Clients zu agieren, wird als *Delegierung* bezeichnet.

Aus Sicht der Sicherheit ergeben sich zwei Probleme im Hinblick auf die Delegierung:

-   Was soll der Server tun, wenn er im Auftrag des Clients agiert?
-   Welche Identität wird vom Server angezeigt, wenn er andere Server im Auftrag eines Clients aufruft?

Um diese Probleme zu beheben, bietet com die folgenden Funktionen. Vom Client kann eine Identitätswechsel *Ebene* festgelegt werden, die festlegt, in welchem Umfang der Server als Client fungieren kann. Wenn der Client dem Server genügend Berechtigungen gewährt *, kann der* Server den Client als Identitätswechsel durchsetzen. Beim Annehmen der Identität des Clients erhält der Server Zugriff auf nur die Objekte oder Ressourcen, für die der Client über die Berechtigung verfügt. Der Server, der als Client fungiert, kann auch das *ausblenden aktivieren,* um seine eigene Identität zu maskieren und die Identität des Clients in Aufrufen anderer com-Komponenten zu projizieren.

![Diagramm, das zeigt, wie der Server, der als Client fungiert, das Cloaking aktivieren kann.](images/172e04f7-568d-450b-9785-2c1a2b40e549.png)

Sehen Sie sich das Szenario an, das in der obigen Abbildung veranschaulicht wird. a und b sind Prozesse auf einem anderen Computer als C. verarbeiten a-Aufrufe b und b C. Client A legt die Identitätswechsel Ebene fest. B legt die Funktionsfähigkeit fest. Wenn eine eine Identitätswechsel Ebene festlegt, die den Identitätswechsel zulässt, kann B die Identität eines annehmen, wenn C in einem Auftrag aufgerufen wird. Die Identität, die für Prozess C dargestellt wird, ist entweder eine Identität oder die Identität des b, abhängig davon, ob das Cloaking durch B aktiviert wurde. Wenn das Cloaking aktiviert ist, ist die für Prozess C vorgelegte Identität die eines. Wenn das Cloaking nicht aktiviert ist, wird die Identität von B in C angezeigt.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Identitätswechsel](impersonation.md)
-   [Identitätswechsel Ebenen](impersonation-levels.md)
-   [Cloaking](cloaking.md)

 

 




