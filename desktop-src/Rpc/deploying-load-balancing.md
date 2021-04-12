---
title: Bereitstellen des Lasten Ausgleichs
description: Bereitstellen des Lasten Ausgleichs
ms.assetid: d80b8999-16c9-4fc8-a1cb-35a65f434884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc00430e8e93334c04dc74c57fc8b50db7d3c899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206550"
---
# <a name="deploying-load-balancing"></a>Bereitstellen des Lasten Ausgleichs

Die typische Bereitstellungs Umgebung und der Anwendungsfall, in der der RPC-Lastenausgleich verwendet wird, finden Sie unten:![RPC-Lastenausgleich](images/rpc-load-balancing.png)

1.  Der RPC-Client stellt eine RPC/HTTP-Verbindung mit der Serverfarm her.
2.  Die Verbindung wird über das Netzwerk an ein Front-End-Lasten Ausgleichs Modul weitergeleitet.
3.  Der Front-End-Load Balancer wählt einen Server aus, um die Anforderung zu bedienen. In diesem Beispiel leitet der Front-End-Load Balancer die Verbindung an Server 1 weiter.
4.  Der RPC-Lasten Ausgleichs Dienst gibt die Verbindung aus. Dabei wird festgelegt, dass es sich hierbei um die erste Verbindung vom Client handelt, und die Verbindung wird dem lokalen Server Server 1 zugeordnet.
5.  Der Client sendet eine zweite RPC/HTTP-Anforderung.
6.  Die Anforderung wird über das Netzwerk an das Front-End-Lasten Ausgleichs Modul weitergeleitet.
7.  Der Front-End-Load Balancer wählt einen Server aus, um die Anforderung zu bedienen. In diesem Fall wählt der Front-End-Lastenausgleich Server 2 aus, um die Anforderung zu bedienen.
8.  Der RPC-Load Balancer Dienst gibt die Verbindung aus. Es wird erkannt, dass Verbindungen von diesem Client von Server 1 bedient werden.
9.  Die Verbindung wird an Server 1 weitergeleitet.

 

 




