---
title: IP-Abhörliste
description: Die HTTP-Server-APIs werden nicht an IP-Adressen und TCP-Port Paare gebunden, bis ein Benutzer ein URLPrefix registriert.
ms.assetid: f2f51e6c-9114-4ba9-a37c-1d1d1f0b444f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba085112c800d7845c76467c4dd2fdc3f5f0b00a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948040"
---
# <a name="ip-listen-list"></a>IP-Abhörliste

Die HTTP-Server-APIs werden nicht an IP-Adressen und TCP-Port Paare gebunden, bis ein Benutzer ein URLPrefix registriert. Wenn eine Registrierung in der Anforderungs Warteschlange eingegeben wird, bindet die HTTP-Server-API standardmäßig eine Bindung an den Port, der im URLPrefix (z. b. Port 80) für alle \_ \_ auf dem Computer verfügbaren IP-Adressen (inaddr any oder INADDR6 any) angegeben ist. Probleme treten auf, wenn Anwendungen von Drittanbietern (nicht die HTTP-Server-APIs) an die IP-Adresse und die Port 80-Paare auf dem Computer gebunden werden. Die HTTP-Server-API bietet eine Möglichkeit zum Konfigurieren der Liste der IP-Adressen, die Sie bindet, und löst dieses Koexistenzproblem. Der Systemadministrator Ruft die [**httpsetserviceconfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) -Funktion auf, wobei der Parameter *ConfigID* auf den Wert httpserviceconmegiplistenlist festgelegt ist, um die IP-Abhörliste anzugeben. Der Liste können sowohl IPv4-als auch IPv6-Adressen hinzugefügt werden. Die eingegebenen IP-Adressen gelten für alle Anwendungen auf dem Computer, die die HTTP-Server-API verwenden und über die Neustarts des Computers hinweg beibehalten werden. Alle Änderungen an der Konfiguration der IP-Abhörliste werden jedoch nicht dynamisch durchgeführt. in den meisten Fällen ist möglicherweise ein Systemneustart erforderlich.

 

 




