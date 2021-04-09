---
title: Entwicklung und Bereitstellung im Netzwerk
description: Die meisten Entwickler schreiben und testen Ihre Software auf einem schnellen zuverlässigen LAN.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a83210db66133329d6c6b38b67ec7ecb29c0595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036838"
---
# <a name="development-vs-deployment-in-the-network"></a>Entwicklung und Bereitstellung im Netzwerk

Die meisten Entwickler schreiben und testen Ihre Software auf einem schnellen zuverlässigen LAN. Client und Server befinden sich häufig in demselben Netzwerksegment. Unter solchen Umständen reagiert das Netzwerk selten nicht, und die Konnektivität geht selten verloren. Bei der Bereitstellung in einer Kundenumgebung befinden sich Client und Server häufig in verschiedenen Netzwerksegmenten, die möglicherweise geografisch Remote sind, und der Server ist stark mit anderen Clients ausgelastet. Anders ausgedrückt: die Reaktionsfähigkeit des Netzwerks kann nicht angenommen werden.

In diesem Artikel wird erläutert, wie robuste Client-/Serverarchitekturen erstellt werden, wenn die Unsicherheit durch ein intrinsisch unzuverlässiges Netzwerk und potenziell nicht verfügbare Server verursacht wird.

 

 




