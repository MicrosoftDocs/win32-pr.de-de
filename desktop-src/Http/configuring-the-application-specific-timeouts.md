---
title: Konfigurieren der anwendungsspezifischen Timeouts
description: Konfigurieren der anwendungsspezifischen Timeouts
ms.assetid: 24526320-4174-4fc7-b45a-c1ec605e1666
keywords:
- Konfigurieren des HTTP-Ausdrucks für anwendungsspezifische Timeouts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca1cbcdb0b0796820282673c41507f6bfcc0ebd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109738"
---
# <a name="configuring-the-application-specific-timeouts"></a><span data-ttu-id="7c9cb-104">Konfigurieren der anwendungsspezifischen Timeouts</span><span class="sxs-lookup"><span data-stu-id="7c9cb-104">Configuring the Application Specific Timeouts</span></span>

<span data-ttu-id="7c9cb-105">Die API-weiten HTTP-Servereinstellungen gelten für alle Serversitzungen und URL-Gruppen auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="7c9cb-105">The HTTP Server API-wide settings apply to all the server sessions and URL groups on the computer.</span></span> <span data-ttu-id="7c9cb-106">Diese Konfigurationen können von der Anwendung überschrieben werden, indem die anwendungsspezifischen Timeoutwerte gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7c9cb-106">These configurations can be overridden by the application by setting the application-specific timeout values.</span></span> <span data-ttu-id="7c9cb-107">Die Serversitzungs-Timeouts überschreiben die HTTP Server-API-weiten Timeouts und gelten für alle URL-Gruppen, die unter ihnen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="7c9cb-107">The server session timeouts override the HTTP Server API-wide timeouts and apply to all the URL groups created under them.</span></span> <span data-ttu-id="7c9cb-108">Durch das Konfigurieren der Timeouteigenschaft für eine URL-Gruppe werden die Serversitzungs-Timeouts für alle URLs in der Gruppe überschrieben.</span><span class="sxs-lookup"><span data-stu-id="7c9cb-108">Configuring the timeouts property on a URL group overrides the server session timeouts for all the URLs in the group.</span></span>

<span data-ttu-id="7c9cb-109">Die Angabe von 0 (null) für einen der Timer in der [**HTTP \_ TIMEOUT \_ LIMIT \_ INFO-Struktur**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) für eine URL-Gruppe bewirkt, dass die HTTP-Server-API auf die Serversitzungs-Timeouts zurückgesetzt wird, sofern diese vorhanden sind, oder die Standardeinstellungen der HTTP-Server-API, wenn die Serversitzungs-Timeouts nicht vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="7c9cb-109">Specifying zero for any of the timers in the [**HTTP\_TIMEOUT\_LIMIT\_INFO**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) structure for a URL group causes the HTTP Server API to revert to the server session timeouts, if they exist, or the HTTP Server API default settings if the server session timeouts do not exist.</span></span> <span data-ttu-id="7c9cb-110">Wenn beispielsweise die Serverzeitüberschreitungseigenschaft in einer URL-Gruppe vorhanden ist und der **EntityBody-Timer** 0 (null) ist, wird das Serversitzungs-Timeout verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c9cb-110">For example, when the server timeout property is present on a URL group and the **EntityBody** timer is zero, the server session timeout is used.</span></span> <span data-ttu-id="7c9cb-111">Wenn die Timeouteigenschaft nicht für eine Serversitzung festgelegt ist, wird die Standardkonfiguration der HTTP-Server-API verwendet.</span><span class="sxs-lookup"><span data-stu-id="7c9cb-111">If the timeouts property is not set on a server session, the HTTP Server API default configuration is used.</span></span> <span data-ttu-id="7c9cb-112">Um einen Timer zu deaktivieren, legen Sie den Wert auf **MAXUSHORT fest,** mit Ausnahme des **MinSendRate-Timers,** der auf **MAXULONG festgelegt ist.**</span><span class="sxs-lookup"><span data-stu-id="7c9cb-112">To disable a timer, set the value to **MAXUSHORT**, except for the **MinSendRate** timer which is set to **MAXULONG**.</span></span>

<span data-ttu-id="7c9cb-113">Die HTTP-Server-API kann nur den anwendungsspezifischen **HeaderWait** konfigurieren, und die **IdleConnection-Timer** sind erst wirksam, nachdem die erste Anforderung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="7c9cb-113">The HTTP Server API can only configure the application-specific **HeaderWait** and the **IdleConnection** timers are only effective after the first request has been received.</span></span> <span data-ttu-id="7c9cb-114">Bevor die erste Anforderung empfangen wird, werden die HTTP Server-API-weiten Timeoutwerte erzwungen.</span><span class="sxs-lookup"><span data-stu-id="7c9cb-114">Before the first request is received, the HTTP Server API-wide timeout values are enforced.</span></span> <span data-ttu-id="7c9cb-115">Nachdem die erste Anforderung eintrifft und einer Anforderungswarteschlange zugeordnet ist, können die anwendungsspezifischen **Timer HeaderWait** und **IdleConnection** angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c9cb-115">After the first request arrives and is associated with a request queue, the application-specific **HeaderWait** and **IdleConnection** timers can be applied.</span></span> <span data-ttu-id="7c9cb-116">Die anwendungsspezifischen Timer werden auf alle nachfolgenden Anforderungen angewendet, die in der Anforderungswarteschlange für eine Keep-Alive-Verbindung eintreffen.</span><span class="sxs-lookup"><span data-stu-id="7c9cb-116">The application-specific timers are applied to all subsequent requests that arrive on the request queue for a keep-alive connection.</span></span>

<span data-ttu-id="7c9cb-117">Weitere Informationen zum Konfigurieren von Timern finden Sie in den Themen [Konfigurieren der URL-Gruppe](configuring-the-url-group.md) und [Konfigurieren der Serversitzung.](configuring-the-server-session.md)</span><span class="sxs-lookup"><span data-stu-id="7c9cb-117">For more information about configuring timers, see the [Configuring the URL Group](configuring-the-url-group.md) and [Configuring the Server Session](configuring-the-server-session.md) topics.</span></span>

 

 




