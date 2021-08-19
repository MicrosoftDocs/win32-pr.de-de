---
title: Gegenseitige Authentifizierung in Windows Sockets-Anwendungen
description: Microsoft Windows Sockets-Dienste können die Registrierungs- und Auflösungs-APIs (RnR) verwenden, um Dienste zu veröffentlichen, oder sie können Dienstverbindungspunkte verwenden.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Gegenseitige Authentifizierung in Windows Sockets-Anwendungen
- Active Directory mit gegenseitiger Authentifizierung in Windows Socketanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a7267159f826d572a8efd101ab86338f5a24c6966b8d2af3a260e1f4af6244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025748"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a>Gegenseitige Authentifizierung in Windows Sockets-Anwendungen

Microsoft Windows Sockets-Dienste können die Registrierungs- und Auflösungs-APIs (RnR) verwenden, um Dienste zu veröffentlichen, oder sie können Dienstverbindungspunkte verwenden.

Weitere Informationen und ein Codebeispiel, das zeigt, wie die gegenseitige Authentifizierung für einen Windows Sockets-Dienst ausgeführt wird, der mithilfe eines Dienstverbindungspunkts veröffentlicht wird, finden Sie unter [Gegenseitige Authentifizierung in einem Windows Sockets Service mit einem SCP.](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) In diesem Codebeispiel wird ein SSPI-Sicherheitspaket verwendet, um die Authentifizierung zwischen einem Client und dem WinSock-Dienst zu verwalten.

Ein WinSock RnR-Dienst kann ähnlichen Code verwenden, um die gegenseitige Authentifizierung mithilfe eines SSPI-Pakets durchzuführen. In diesem Fall erstellt der Dienst seine SPNs unter Verwendung des Distinguished Name des Diensteintrags im WinsockServices-Container im Verzeichnis.

Wenn sich der Dienst beispielsweise mit dem Namen "WinSockRnRSampleService" registriert, würden Sie den SPN des Diensts aus dem folgenden Distinguished Name zusammensetzen:


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




