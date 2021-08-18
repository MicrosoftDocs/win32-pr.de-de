---
title: Entwicklung im Vergleich zur Bereitstellung im Netzwerk
description: Die meisten Entwickler schreiben und testen ihre Software in einem schnellen zuverlässigen LAN.
ms.assetid: 9458162c-1046-4554-bafa-b455f2957d58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ff9da31ecd80b9e0a699d9ec0eb450e885a423b9380b85e2015e9ef7c1af7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930620"
---
# <a name="development-vs-deployment-in-the-network"></a>Entwicklung im Vergleich zur Bereitstellung im Netzwerk

Die meisten Entwickler schreiben und testen ihre Software in einem schnellen zuverlässigen LAN. Client und Server befinden sich häufig im gleichen Netzwerksegment. In solchen Fällen reagiert das Netzwerk selten nicht, und die Konnektivität geht selten verloren. Bei der Bereitstellung in einer Kundenumgebung befinden sich Client und Server jedoch häufig in unterschiedlichen Netzwerksegmenten, möglicherweise geografisch remote, und der Server ist stark mit anderen Clients überlastet. Anders ausgedrückt: Die Reaktionsfähigkeit des Netzwerks kann nicht angenommen werden.

In diesem Artikel wird erläutert, wie Sie robuste Client-/Serverarchitekturen erstellen, wenn dies durch ein systeminternes unzuverlässiges Netzwerk und möglicherweise nicht verfügbare Server eingeführt wird.

 

 




