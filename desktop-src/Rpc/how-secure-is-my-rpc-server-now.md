---
title: Wie sicher ist der RPC-Server jetzt?
description: Nach der in diesem Abschnitt beschriebenen Sicherheit, die an anderer Stelle im RPC SDK bereitgestellt wird und in der Regel als ordnungsgemäße Sicherheitspraktiken akzeptiert wird, führt dies zu einem Server, der sehr sicher ist. Solche Server sind vor Penetrations Angriffen oder Datenschutzverletzungen geschützt.
ms.assetid: 528ff35c-f37c-43d8-8cc1-dbc36a9a826c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34279e4fb8899db6b7e980a0e868e91c6edb8166
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947767"
---
# <a name="how-secure-is-my-rpc-server-now"></a><span data-ttu-id="3b954-104">Wie sicher ist jetzt der RPC-Server?</span><span class="sxs-lookup"><span data-stu-id="3b954-104">How Secure is My RPC Server Now?</span></span>

<span data-ttu-id="3b954-105">Nach der in diesem Abschnitt beschriebenen Sicherheit, die an anderer Stelle im RPC SDK bereitgestellt wird und in der Regel als ordnungsgemäße Sicherheitspraktiken akzeptiert wird, führt dies zu einem Server, der sehr sicher ist.</span><span class="sxs-lookup"><span data-stu-id="3b954-105">Following the security outlined in this section, provided elsewhere in the RPC SDK, and generally accepted as proper security practices, will result in a server that is very secure.</span></span> <span data-ttu-id="3b954-106">Solche Server sind vor Penetrations Angriffen oder Datenschutzverletzungen geschützt.</span><span class="sxs-lookup"><span data-stu-id="3b954-106">Such servers are protected from penetration attacks or privacy breaches.</span></span>

<span data-ttu-id="3b954-107">Wenn der Status zwischen RPC-Aufrufen beibehalten wird, stellen Sie sicher, dass ein einzelner Client nicht die Zuordnung von übermäßigen Ressourcen verursacht, wodurch der Dienst für andere Clients möglicherweise verweigert wird.</span><span class="sxs-lookup"><span data-stu-id="3b954-107">If state is kept between RPC calls, make sure a single client does not cause the allocation of excessive resources, which could potentially deny service to other clients.</span></span>

 

 




