---
description: Sowohl C++-Anbieter als auch Client Anwendungen müssen viele der gleichen Vorgänge ausführen, um die WMI-Sicherheit aufrechtzuerhalten.
ms.assetid: 0199f469-2666-4794-b364-36c54aa360a8
ms.tgt_platform: multiple
title: Sichern von C++-Clients und-Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac93ee88f710bf17a2b6199b3a9b2e89279b4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347320"
---
# <a name="securing-c-clients-and-providers"></a><span data-ttu-id="cccf0-103">Sichern von C++-Clients und-Anbietern</span><span class="sxs-lookup"><span data-stu-id="cccf0-103">Securing C++ Clients and Providers</span></span>

<span data-ttu-id="cccf0-104">Sowohl C++-Anbieter als auch Client Anwendungen müssen viele der gleichen Vorgänge ausführen, um die WMI-Sicherheit aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="cccf0-104">Both C++ providers and client applications must perform many of the same operations to maintain WMI security.</span></span>

<span data-ttu-id="cccf0-105">Client Anwendungen müssen den [DCOM-](setting-the-default-process-security-level-using-c-.md) Identitätswechsel und die [Authentifizierungs](setting-authentication-in-wmi.md) Ebenen beim Herstellen einer Verbindung mit WMI ordnungsgemäß festlegen.</span><span class="sxs-lookup"><span data-stu-id="cccf0-105">Client applications must set DCOM [impersonation](setting-the-default-process-security-level-using-c-.md) and [authentication](setting-authentication-in-wmi.md) levels correctly when connecting to WMI.</span></span> <span data-ttu-id="cccf0-106">[Rückrufe von asynchronen Aufrufen](setting-security-on-an-asynchronous-call.md) haben Sicherheitsrisiken, sodass Client Anwendungen [Zugriffs Überprüfungen durchführen](performing-access-checks.md) müssen, um sicherzustellen, dass der Rückruf von einer vertrauenswürdigen Quelle aus erfolgt.</span><span class="sxs-lookup"><span data-stu-id="cccf0-106">Callbacks from [asynchronous calls](setting-security-on-an-asynchronous-call.md) have security risks, so client applications must [perform access checks](performing-access-checks.md) to ensure the callback is from a trusted source.</span></span> <span data-ttu-id="cccf0-107">Clients müssen [temporäre und permanente Ereignisconsumer](securing-wmi-events.md)sichern.</span><span class="sxs-lookup"><span data-stu-id="cccf0-107">Clients need to secure both [temporary and permanent event consumers](securing-wmi-events.md).</span></span>

<span data-ttu-id="cccf0-108">Ein Anbieter kann [Zugriffs Überprüfungen durchführen](performing-access-checks.md) , um sicherzustellen, dass auf die erstellten Ressourcen nur von den entsprechenden Clients zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="cccf0-108">A provider may [perform access checks](performing-access-checks.md) to ensure that the resources it creates are only accessed by appropriate clients.</span></span>

<span data-ttu-id="cccf0-109">Sowohl Anbieter als auch Clients können die Sicherheit für eine [bestimmte Proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) Verbindung festlegen.</span><span class="sxs-lookup"><span data-stu-id="cccf0-109">Both providers and clients also can set the security on a [specific proxy](setting-the-security-on-iwbemservices-and-other-proxies.md) connection.</span></span> <span data-ttu-id="cccf0-110">Beide können auch [Berechtigungen](executing-privileged-operations.md)aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cccf0-110">Both can also enable [privileges](executing-privileged-operations.md).</span></span> <span data-ttu-id="cccf0-111">Ein Ereignis Anbieter muss sicherstellen, dass der clientconsumer über Berechtigungen zum [empfangen eines angeforderten Ereignisses](providing-events-securely.md)verfügt.</span><span class="sxs-lookup"><span data-stu-id="cccf0-111">An event provider must ensure that the client consumer has privileges to [receive a requested event](providing-events-securely.md).</span></span>

<span data-ttu-id="cccf0-112">Ein Client oder Anbieter muss möglicherweise eine Remote Verbindung herstellen, die einen anderen Authentifizierungsdienst erfordert, z. b. NTLM anstelle von Kerberos.</span><span class="sxs-lookup"><span data-stu-id="cccf0-112">Either a client or provider may need to make a remote connection that requires a different authentication service, NTLM instead of Kerberos for example.</span></span>

 

 



