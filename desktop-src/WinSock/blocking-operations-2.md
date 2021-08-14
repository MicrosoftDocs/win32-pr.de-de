---
description: Das Konzept der Blockierung in einer Windows war in der Vergangenheit sehr wichtig.
ms.assetid: bd2ede96-34a4-4912-b9d2-ef11d37d2292
title: Blockierende Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d130de2322e10de15bc73e9901b7d55764b34cfbb609e2e25942fb55a3cf445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322435"
---
# <a name="blocking-operations"></a>Blockierende Vorgänge

Das Konzept der Blockierung in einer Windows war in der Vergangenheit sehr wichtig. In Windows Sockets 1.1-Umgebungen wurde von blockierenden Aufrufen abgeraten, da sie dazu tendierten, die laufende Interaktion mit dem System zu deaktivieren. Darüber hinaus verwenden sie eine Pseudoblockierungstechnik, die aus verschiedenen Gründen nicht immer wie beabsichtigt funktioniert. In präemptiv geplanten Windows-Umgebungen sind blockierende Aufrufe jedoch viel sinnvoller, können von nativen Betriebssystemdiensten implementiert werden und sind tatsächlich ein im Allgemeinen bevorzugter Mechanismus. Die Winsock 2-API unterstützt psuedoblocking nicht mehr, aber da die Windows Sockets 1.1-Kompatibilitätss shims dieses Verhalten weiterhin emulieren müssen, müssen Dienstanbieter dies wie im Folgenden beschrieben unterstützen.

 

 



