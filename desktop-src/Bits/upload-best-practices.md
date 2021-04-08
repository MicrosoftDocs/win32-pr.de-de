---
title: Bewährte Methoden für den Upload
description: Highloads können verschiedene Server Timeout-Bedingungen verursachen. Dies kann wiederum die Last erhöhen, wenn der Client den Vorgang wiederholt.
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036409"
---
# <a name="upload-best-practices"></a>Bewährte Methoden für den Upload

Highloads können verschiedene Server Timeout-Bedingungen verursachen. Dies kann wiederum die Last erhöhen, wenn der Client den Vorgang wiederholt. Außerdem verbraucht eine große Anzahl von ausstehenden Verbindungen mehr Server Ressourcen und macht die Situation schlechter. Wenn eine Back-End-APP nicht zur Behandlung von hohen Ladebedingungen geschrieben wird, kann dies zu einem Absturz oder einem anderen Verhalten führen. Die APP muss die folgenden Schritte ausführen, um die Last für das Back-End einzuschränken.

Wenn die Serveranwendung nicht zur Verarbeitung hoher Volumes geschrieben wird, treten möglicherweise Timeout Bedingungen auf, die wiederum die Last erhöhen, wenn der Client den Vorgang wiederholt. Außerdem verbraucht eine große Anzahl von ausstehenden Verbindungen mehr Server Ressourcen.

Testen Sie beim Testen der Serveranwendung mit der höchsten Auslastung. Sie sollten mehrere Client Computer verwenden, von denen jeder über mehrere gleichzeitige, Vordergrund-BITS-Aufträge verfügt, und den maximalen Durchsatz beim Back-End messen. Wenn der Durchsatz nicht gemessen werden kann, müssen Sie den Durchsatz schätzen.

Die Serveranwendung sollte sich in einer anderen URL als die uploadurl befinden (siehe die BITS-IIS-Eigenschaft, **bitsservernotificationurl**).

Es empfiehlt sich, die Last auf dem Anwendungsserver basierend auf bewährten Durchsatz Werten einzuschränken. Verwenden Sie die IIS-Eigenschaften " **MaxBandwidth** " und " **MaxConnections**", um die Auslastung des Anwendungs Servers einzuschränken.

 

 




