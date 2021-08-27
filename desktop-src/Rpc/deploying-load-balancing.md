---
title: Bereitstellen des Lastenausgleichs
description: Bereitstellen des Lastenausgleichs
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36d1ba29aedd5e94c29095d18fb84790ec4b76956ea20bc2ffd584b5a6a179f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021844"
---
# <a name="deploying-load-balancing"></a>Bereitstellen des Lastenausgleichs

Die typische Bereitstellungsumgebung und der Anwendungsfall, in dem der RPC-Lastenausgleich verwendet wird, sind unten dargestellt:![RPC-Lastenausgleich](images/rpc-load-balancing.png)

1.  Der RPC-Client stellt eine RPC/HTTP-Verbindung mit der Serverfarm her.
2.  Die Verbindung wird über das Netzwerk an einen Front-End-Lastenausgleich weitergeleitet.
3.  Der Front-End-Lastenausgleich wählt einen Server für die Anforderung aus. In diesem Beispiel leitet der Front-End-Lastenausgleich die Verbindung an Server 1 weiter.
4.  Der RPC-Lastenausgleichsdienst vermittelt die Verbindung. Sie ermittelt, dass dies die erste Verbindung vom Client ist, und ordnet die Verbindung dem lokalen Server Server 1 zu.
5.  Der Client stellt eine zweite RPC/HTTP-Anforderung.
6.  Die Anforderung wird über das Netzwerk an den Front-End-Lastenausgleich weitergeleitet.
7.  Der Front-End-Lastenausgleich wählt einen Server für die Anforderung aus. In diesem Fall wählt der Front-End-Lastenausgleich Server 2 aus, um die Anforderung zu bedienen.
8.  Der RPC-Load Balancer-Dienst vermittelt die Verbindung. Er erkennt, dass Verbindungen von diesem Client von Server 1 bedient werden.
9.  Die Verbindung wird an Server 1 weitergeleitet.

 

 




