---
title: Gegenseitige Authentifizierung in Windows Sockets-Anwendungen
description: Microsoft Windows Sockets-Dienste können die Registrierungs-und Auflösungs-APIs (RNR) zum Veröffentlichen von Diensten verwenden, oder Sie können Dienst Verbindungspunkte verwenden.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Gegenseitige Authentifizierung in Windows Sockets-Anwendungen
- Active Directory mithilfe der gegenseitigen Authentifizierung in Windows Sockets-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29062fa5c9fa7b9b003f1c3aa6f8bc384a785f83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206257"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a>Gegenseitige Authentifizierung in Windows Sockets-Anwendungen

Microsoft Windows Sockets-Dienste können die Registrierungs-und Auflösungs-APIs (RNR) zum Veröffentlichen von Diensten verwenden, oder Sie können Dienst Verbindungspunkte verwenden.

Weitere Informationen und ein Codebeispiel, das zeigt, wie die gegenseitige Authentifizierung für einen Windows Sockets-Dienst durchgeführt wird, der mithilfe eines Dienst Verbindungs Punkts veröffentlicht wird, finden Sie unter [gegenseitige Authentifizierung in einem Windows Sockets Service mit einem SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md). In diesem Codebeispiel wird ein SSPI-Sicherheitspaket verwendet, um die Authentifizierungs Verhandlungen zwischen einem Client und dem Winsock-Dienst zu verwalten.

Ein Winsock RNR-Dienst kann ähnlichen Code verwenden, um die gegenseitige Authentifizierung mithilfe eines SSPI-Pakets auszuführen. In diesem Fall würde der Dienst seine SPNs mithilfe des Distinguished Name des Dienst Eintrags im winsockservices-Container im Verzeichnis zusammenstellen.

Wenn sich der Dienst beispielsweise mit dem Namen "winsockrnrsampleservice" registriert, würden Sie den Dienst Prinzipal Namen aus dem folgenden Distinguished Name verfassen:


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




