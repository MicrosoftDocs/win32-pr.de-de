---
title: Sicherheitsanbieter
description: Die Security Support Provider-Schnittstelle (Security Support Provider Interface, SSPI) bietet Unterstützung für die gegenseitige Authentifizierung und wird direkt über die SSPI-APIs und-Dienste, die in SSPI (einschließlich RPC
ms.assetid: 3aa64aa1-c707-489f-a0a3-08bf6ac151ec
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf033550c2a2da66b7eab05f23289ba988690e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036342"
---
# <a name="security-providers"></a>Sicherheitsanbieter

Die Security Support Provider-Schnittstelle (Security Support Provider Interface, SSPI) bietet Unterstützung für die gegenseitige Authentifizierung und wird direkt über die SSPI-APIs und-Dienste, die in SSPI (einschließlich RPC

Nicht alle für SSPI verfügbaren Sicherheitspakete unterstützen die gegenseitige Authentifizierung. Zum Abrufen der gegenseitigen Authentifizierung muss die Anwendung die gegenseitige Authentifizierung und ein Sicherheitspaket anfordern, das Sie unterstützt. Das Codebeispiel für die [gegenseitige Authentifizierung in einem Windows Sockets-Dienst mit einem Dienst](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) Verbindungspunkt verwendet beispielsweise das "Aushandlungs Paket" in Secur32.dll, das in Windows 2000 enthalten ist.

 

 




