---
title: Überprüfen Sie, ob der Server, den er als
description: Es empfiehlt sich, die gegenseitige Authentifizierung zu verwenden und so die Identität des Servers zu überprüfen.
ms.assetid: 6636a865-0e3b-4e52-81bb-0df48285e928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3e16ae6a87134a9fbc783d35216a1c4df56ce2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710577"
---
# <a name="verify-the-server-is-who-it-claims-to-be"></a>Überprüfen Sie, ob der Server, den er als

Es empfiehlt sich, die gegenseitige Authentifizierung zu verwenden und so die Identität des Servers zu überprüfen. Ein Beispiel für einen allgemeinen Fehler, bei dem dies nicht der Fall ist, sind Anwendungen mit einem lokalen Dienst, der von den Clients aufgerufen wird. In manchen Konfigurationen kann ein Administrator entscheiden, dass der Systemdienst nicht wirklich nützlich ist und ihn möglicherweise beendet. Ein erfinderischer Angreifer auf einem Terminal Server Computer kann einen Prozess starten, der auf demselben Endpunkt lauscht, und wenn ein Client eine Verbindung mit einem Endpunkt herstellt, sodass der Identitätswechsel auf dem Server ohne gegenseitige Authentifizierung des Servers möglich ist, kann der Angreifer die Identität des Clients annehmen und auf die Daten des Clients zugreifen oder im Auftrag des Clients Netzwerk Aufrufe durchführen. Die meisten Systemdienste werden unter einem bekannten Konto ausgeführt, z. b. "localsysyem", "LocalService" oder "Network Service", das mithilfe der gegenseitigen Authentifizierung überprüft werden kann.

 

 




