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
# <a name="security-providers"></a><span data-ttu-id="1469c-103">Sicherheitsanbieter</span><span class="sxs-lookup"><span data-stu-id="1469c-103">Security Providers</span></span>

<span data-ttu-id="1469c-104">Die Security Support Provider-Schnittstelle (Security Support Provider Interface, SSPI) bietet Unterstützung für die gegenseitige Authentifizierung und wird direkt über die SSPI-APIs und-Dienste, die in SSPI (einschließlich RPC</span><span class="sxs-lookup"><span data-stu-id="1469c-104">The Security Support Provider Interface (SSPI) provides support for mutual authentication and is exposed directly through the SSPI APIs and services layered on SSPI, including RPC.</span></span>

<span data-ttu-id="1469c-105">Nicht alle für SSPI verfügbaren Sicherheitspakete unterstützen die gegenseitige Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="1469c-105">Not all security packages available to SSPI support mutual authentication.</span></span> <span data-ttu-id="1469c-106">Zum Abrufen der gegenseitigen Authentifizierung muss die Anwendung die gegenseitige Authentifizierung und ein Sicherheitspaket anfordern, das Sie unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1469c-106">To obtain mutual authentication, the application must request mutual authentication and a security package that supports it.</span></span> <span data-ttu-id="1469c-107">Das Codebeispiel für die [gegenseitige Authentifizierung in einem Windows Sockets-Dienst mit einem Dienst](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) Verbindungspunkt verwendet beispielsweise das "Aushandlungs Paket" in Secur32.dll, das in Windows 2000 enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1469c-107">For example, the code example in [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md) uses the "negotiate" package in Secur32.dll, which is included with Windows 2000.</span></span>

 

 




