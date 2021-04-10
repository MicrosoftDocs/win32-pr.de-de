---
title: Konfigurieren der anwendungsspezifischen Timeouts
description: .
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Konfigurieren der anwendungsspezifischen Timeouts http
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35827b797ad6c9f19b728064f6fe65b0d89b2a3b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036901"
---
# <a name="configuring-the-application-specific-timeouts"></a><span data-ttu-id="068bb-104">Konfigurieren der anwendungsspezifischen Timeouts</span><span class="sxs-lookup"><span data-stu-id="068bb-104">Configuring the Application Specific Timeouts</span></span>

<span data-ttu-id="068bb-105">Die HTTP-Server-API-weiten Einstellungen gelten für alle Server Sitzungen und URL-Gruppen auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="068bb-105">The HTTP Server API-wide settings apply to all the server sessions and URL groups on the computer.</span></span> <span data-ttu-id="068bb-106">Diese Konfigurationen können von der Anwendung überschrieben werden, indem die anwendungsspezifischen Timeout Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="068bb-106">These configurations can be overridden by the application by setting the application-specific timeout values.</span></span> <span data-ttu-id="068bb-107">Die Timeouts der Server Sitzung überschreiben die API-weiten Timeouts für die HTTP-Server und gelten für alle unter Ihnen erstellten URL-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="068bb-107">The server session timeouts override the HTTP Server API-wide timeouts and apply to all the URL groups created under them.</span></span> <span data-ttu-id="068bb-108">Wenn Sie die Timeouts-Eigenschaft für eine URL-Gruppe konfigurieren, werden die Timeouts der Server Sitzung für alle URLs in der Gruppe überschrieben.</span><span class="sxs-lookup"><span data-stu-id="068bb-108">Configuring the timeouts property on a URL group overrides the server session timeouts for all the URLs in the group.</span></span>

<span data-ttu-id="068bb-109">Das Angeben von NULL für einen der Timer in der [**Informationsstruktur http- \_ Timeout \_ Limit \_**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) für eine URL-Gruppe bewirkt, dass die HTTP-Server-API die Timeout Werte der Server Sitzung wiederherstellt, wenn Sie vorhanden sind, oder die Standardeinstellungen der HTTP-Server-API, wenn die Server Sitzungs Timeouts nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="068bb-109">Specifying zero for any of the timers in the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure for a URL group causes the HTTP Server API to revert to the server session timeouts, if they exist, or the HTTP Server API default settings if the server session timeouts do not exist.</span></span> <span data-ttu-id="068bb-110">Wenn z. b. die Server Timeout-Eigenschaft in einer URL-Gruppe vorhanden ist und der **entityBody** -Timer 0 (null) ist, wird das Timeout der Server Sitzung verwendet.</span><span class="sxs-lookup"><span data-stu-id="068bb-110">For example, when the server timeout property is present on a URL group and the **EntityBody** timer is zero, the server session timeout is used.</span></span> <span data-ttu-id="068bb-111">Wenn die Eigenschaft Timeouts für eine Server Sitzung nicht festgelegt ist, wird die Standardkonfiguration der HTTP-Server-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="068bb-111">If the timeouts property is not set on a server session, the HTTP Server API default configuration is used.</span></span> <span data-ttu-id="068bb-112">Um einen Timer zu deaktivieren, legen Sie den Wert auf **maxushort** fest, mit Ausnahme des **minsendrate** -Timers, der auf **MAXULONG** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="068bb-112">To disable a timer, set the value to **MAXUSHORT**, except for the **MinSendRate** timer which is set to **MAXULONG**.</span></span>

<span data-ttu-id="068bb-113">Von der HTTP-Server-API können nur die anwendungsspezifischen **Header Wait** und die **idleconnection** -Timer nur wirksam werden, nachdem die erste Anforderung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="068bb-113">The HTTP Server API can only configure the application-specific **HeaderWait** and the **IdleConnection** timers are only effective after the first request has been received.</span></span> <span data-ttu-id="068bb-114">Bevor die erste Anforderung empfangen wird, werden die HTTP-Server-API-weiten Timeout Werte erzwungen.</span><span class="sxs-lookup"><span data-stu-id="068bb-114">Before the first request is received, the HTTP Server API-wide timeout values are enforced.</span></span> <span data-ttu-id="068bb-115">Nachdem die erste Anforderung eingeht und einer Anforderungs Warteschlange zugeordnet ist, können die anwendungsspezifischen **Header Wait** und **idleconnection** angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="068bb-115">After the first request arrives and is associated with a request queue, the application-specific **HeaderWait** and **IdleConnection** timers can be applied.</span></span> <span data-ttu-id="068bb-116">Die anwendungsspezifischen Timer werden auf alle nachfolgenden Anforderungen angewendet, die für eine Keep-Alive-Verbindung in der Anforderungs Warteschlange eintreffen.</span><span class="sxs-lookup"><span data-stu-id="068bb-116">The application-specific timers are applied to all subsequent requests that arrive on the request queue for a keep-alive connection.</span></span>

<span data-ttu-id="068bb-117">Weitere Informationen zum Konfigurieren von Timern finden Sie in den Themen [Konfigurieren der URL-Gruppe](configuring-the-url-group.md) und [Konfigurieren der Server Sitzung](configuring-the-server-session.md) .</span><span class="sxs-lookup"><span data-stu-id="068bb-117">For more information about configuring timers, see the [Configuring the URL Group](configuring-the-url-group.md) and [Configuring the Server Session](configuring-the-server-session.md) topics.</span></span>

 

 




