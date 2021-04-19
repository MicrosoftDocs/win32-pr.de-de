---
title: Funktions Vergleich von Windows 2000 und RRAS Redistributable
description: Die RAS-API wird als Feature von Windows 2000 und neueren Betriebssystemen verteilt und ist als verteilbare Komponente für Windows NT 4,0 mit Service Pack 3 (SP3) und früher verfügbar.
ms.assetid: fd6c76b9-52e2-405e-b62e-055cfbdb5ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 745ad0c50654c8269c3e62b03629a7ae12a17476
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341683"
---
# <a name="function-comparison-windows-2000-vs-rras-redistributable"></a><span data-ttu-id="13ab4-103">Funktions Vergleich: Windows 2000 und RRAS Redistributable</span><span class="sxs-lookup"><span data-stu-id="13ab4-103">Function Comparison: Windows 2000 vs. RRAS Redistributable</span></span>

<span data-ttu-id="13ab4-104">Die RAS-API wird als Feature von Windows 2000 und neueren Betriebssystemen verteilt und ist als verteilbare Komponente für Windows NT 4,0 mit Service Pack 3 (SP3) und früher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="13ab4-104">The RAS API is distributed as a feature of Windows 2000 and later operating systems and is available as a redistributable for Windows NT 4.0 with Service Pack 3 (SP3) and earlier.</span></span> <span data-ttu-id="13ab4-105">RAS bietet die gleichen Funktionen in beiden Formularen, aber die verwendete Benennungs Konvention unterscheidet sich für die Verweis Elemente in jeder Version der RAS-API.</span><span class="sxs-lookup"><span data-stu-id="13ab4-105">RAS provides the same functionality in both of these forms but the naming convention that is used is different for the reference elements in each version of the RAS API.</span></span>

<span data-ttu-id="13ab4-106">Die RAS-Funktionen für Windows NT 4,0 mit SP3 und früher beginnen in der Regel mit dem Präfix "rasadmin".</span><span class="sxs-lookup"><span data-stu-id="13ab4-106">The RAS functions for Windows NT 4.0 with SP3 and earlier typically begin with the "RasAdmin" prefix.</span></span> <span data-ttu-id="13ab4-107">Die analogen Funktionen für den Routing-und RAS-Dienst (RRAS) beginnen mit dem Präfix "mpradmin".</span><span class="sxs-lookup"><span data-stu-id="13ab4-107">The analogous functions for Routing and Remote Access Service (RRAS) begin with the "MprAdmin" prefix.</span></span> <span data-ttu-id="13ab4-108">Beispielsweise stellt RAS eine Funktion mit dem Namen [**rasadminportgetinfo**](rasadminportgetinfo.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="13ab4-108">For example, RAS provides a function called [**RasAdminPortGetInfo**](rasadminportgetinfo.md).</span></span> <span data-ttu-id="13ab4-109">Die Analog-Funktion in RRAS heißt [**mpradminportgetinfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span><span class="sxs-lookup"><span data-stu-id="13ab4-109">The analogous function in RRAS is called [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo).</span></span> <span data-ttu-id="13ab4-110">In einem ähnlichen Beispiel stellt RAS die Rückruffunktion [**rasadmingetipaddressforuser**](rasadmingetipaddressforuser.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="13ab4-110">As a similar example, RAS provides the callback function [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span> <span data-ttu-id="13ab4-111">RRAS bietet eine ähnliche Rückruffunktion mit dem Namen [**mpradmingetipaddressforuser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span><span class="sxs-lookup"><span data-stu-id="13ab4-111">RRAS provides a similar callback function called [**MprAdminGetIpAddressForUser**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser).</span></span> <span data-ttu-id="13ab4-112">Ausnahmen für diese Regel sind [**rasadminportclearstatistics**](rasadminportclearstatistics.md), die unter RRAS den Wert [**mpradminportclearstats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)und [**rasadminfreebuffer**](rasadminfreebuffer.md)hat, der unter RRAS den Wert [**mpradminbufferfree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)aufweist.</span><span class="sxs-lookup"><span data-stu-id="13ab4-112">Exceptions to this rule are [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md), which under RRAS is [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats), and [**RasAdminFreeBuffer**](rasadminfreebuffer.md), which under RRAS is [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree).</span></span>

<span data-ttu-id="13ab4-113">In der folgenden Tabelle werden die Windows NT 4,0 SP3-RAS-Funktionen und die zugehörigen RRAS-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="13ab4-113">The following table lists the Windows NT 4.0 SP3 RAS functions and the corresponding RRAS functions.</span></span>



| <span data-ttu-id="13ab4-114">Windows NT 4,0-RAS</span><span class="sxs-lookup"><span data-stu-id="13ab4-114">Windows NT 4.0 RAS</span></span>                                                                   | <span data-ttu-id="13ab4-115">RRAS</span><span class="sxs-lookup"><span data-stu-id="13ab4-115">RRAS</span></span>                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="13ab4-116">**Rasadminakzeptnewconnection**</span><span class="sxs-lookup"><span data-stu-id="13ab4-116">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)                   | [<span data-ttu-id="13ab4-117">**Mpradminakzeptnewconnection**</span><span class="sxs-lookup"><span data-stu-id="13ab4-117">**MprAdminAcceptNewConnection**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection)                   |
| [<span data-ttu-id="13ab4-118">**Rasadminconnectionhangupnotification**</span><span class="sxs-lookup"><span data-stu-id="13ab4-118">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md) | [<span data-ttu-id="13ab4-119">**Mpradminconnectionhangupnotification**</span><span class="sxs-lookup"><span data-stu-id="13ab4-119">**MprAdminConnectionHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification) |
| [<span data-ttu-id="13ab4-120">**Rasadminfrebuffer**</span><span class="sxs-lookup"><span data-stu-id="13ab4-120">**RasAdminFreeBuffer**</span></span>](rasadminfreebuffer.md)                                     | [<span data-ttu-id="13ab4-121">**Mpradminbufferfree**</span><span class="sxs-lookup"><span data-stu-id="13ab4-121">**MprAdminBufferFree**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)                                     |
| [<span data-ttu-id="13ab4-122">**Rasadmingeterrorstring**</span><span class="sxs-lookup"><span data-stu-id="13ab4-122">**RasAdminGetErrorString**</span></span>](rasadmingeterrorstring.md)                             | [<span data-ttu-id="13ab4-123">**Mpradmingeterrorstring**</span><span class="sxs-lookup"><span data-stu-id="13ab4-123">**MprAdminGetErrorString**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)                             |
| [<span data-ttu-id="13ab4-124">**Rasadmingetipaddressforuser**</span><span class="sxs-lookup"><span data-stu-id="13ab4-124">**RasAdminGetIpAddressForUser**</span></span>](rasadmingetipaddressforuser.md)                   | [<span data-ttu-id="13ab4-125">**Mpradmingetipaddressforuser**</span><span class="sxs-lookup"><span data-stu-id="13ab4-125">**MprAdminGetIpAddressForUser**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetipaddressforuser)                   |
| [<span data-ttu-id="13ab4-126">**Rasadminportclearstatistics**</span><span class="sxs-lookup"><span data-stu-id="13ab4-126">**RasAdminPortClearStatistics**</span></span>](rasadminportclearstatistics.md)                   | [<span data-ttu-id="13ab4-127">**Mpradminportclearstats**</span><span class="sxs-lookup"><span data-stu-id="13ab4-127">**MprAdminPortClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)                             |
| [<span data-ttu-id="13ab4-128">**Rasadminportdisconnect**</span><span class="sxs-lookup"><span data-stu-id="13ab4-128">**RasAdminPortDisconnect**</span></span>](rasadminportdisconnect.md)                             | [<span data-ttu-id="13ab4-129">**Mpradminportdisconnect**</span><span class="sxs-lookup"><span data-stu-id="13ab4-129">**MprAdminPortDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)                             |
| [<span data-ttu-id="13ab4-130">**Rasadminportenum**</span><span class="sxs-lookup"><span data-stu-id="13ab4-130">**RasAdminPortEnum**</span></span>](rasadminportenum.md)                                         | [<span data-ttu-id="13ab4-131">**Mpradminportenum**</span><span class="sxs-lookup"><span data-stu-id="13ab4-131">**MprAdminPortEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)                                         |
| [<span data-ttu-id="13ab4-132">**Rasadminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="13ab4-132">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)                                   | [<span data-ttu-id="13ab4-133">**Mpradminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="13ab4-133">**MprAdminPortGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)                                   |
| [<span data-ttu-id="13ab4-134">**Rasadminreleaseipaddress**</span><span class="sxs-lookup"><span data-stu-id="13ab4-134">**RasAdminReleaseIpAddress**</span></span>](rasadminreleaseipaddress.md)                         | [<span data-ttu-id="13ab4-135">**Mpradminreleaseipaddress**</span><span class="sxs-lookup"><span data-stu-id="13ab4-135">**MprAdminReleaseIpAddress**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)                         |
| [<span data-ttu-id="13ab4-136">**Rasadminusergetinfo**</span><span class="sxs-lookup"><span data-stu-id="13ab4-136">**RasAdminUserGetInfo**</span></span>](rasadminusergetinfo.md)                                   | [<span data-ttu-id="13ab4-137">**Mpradminusergetinfo**</span><span class="sxs-lookup"><span data-stu-id="13ab4-137">**MprAdminUserGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)                                   |
| [<span data-ttu-id="13ab4-138">**Rasadminusereintinfo**</span><span class="sxs-lookup"><span data-stu-id="13ab4-138">**RasAdminUserSetInfo**</span></span>](rasadminusersetinfo.md)                                   | [<span data-ttu-id="13ab4-139">**Mpradminusereintinfo**</span><span class="sxs-lookup"><span data-stu-id="13ab4-139">**MprAdminUserSetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)                                   |



 

<span data-ttu-id="13ab4-140">Obwohl die RRAS-Funktionen Windows NT 4,0 mit SP3 und früheren RAS-Entsprechungen in der Funktionalität ähneln, nehmen RRAS-Funktionen häufig einen anderen Satz von Parametern auf.</span><span class="sxs-lookup"><span data-stu-id="13ab4-140">Although the RRAS functions are similar to their Windows NT 4.0 with SP3 and earlier RAS counterparts in functionality, RRAS functions often take a different set of parameters.</span></span> <span data-ttu-id="13ab4-141">Ausführliche Informationen zur Parameterliste der Funktion finden Sie auf der Referenzseite für eine bestimmte Funktion.</span><span class="sxs-lookup"><span data-stu-id="13ab4-141">See the reference page for a particular function for complete information on that function's parameter list.</span></span>

<span data-ttu-id="13ab4-142">Die weitervertreibbare RRAS-Version für Windows NT 4,0 mit SP3 und früher fügt die folgenden Funktionen hinzu, die keine RAS-Entsprechungen aufweisen:</span><span class="sxs-lookup"><span data-stu-id="13ab4-142">The RRAS redistributable for Windows NT 4.0 with SP3 and earlier adds the following functions, which have no RAS counterparts:</span></span>

[<span data-ttu-id="13ab4-143">**Mpradminakzeptnewlink**</span><span class="sxs-lookup"><span data-stu-id="13ab4-143">**MprAdminAcceptNewLink**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewlink)

[<span data-ttu-id="13ab4-144">**Mpradminconnectionclearstats**</span><span class="sxs-lookup"><span data-stu-id="13ab4-144">**MprAdminConnectionClearStats**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)

[<span data-ttu-id="13ab4-145">**Mpradminconnectionenum**</span><span class="sxs-lookup"><span data-stu-id="13ab4-145">**MprAdminConnectionEnum**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)

[<span data-ttu-id="13ab4-146">**Mpradminconnectiongetinfo**</span><span class="sxs-lookup"><span data-stu-id="13ab4-146">**MprAdminConnectionGetInfo**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)

[<span data-ttu-id="13ab4-147">**Mpradmingetpdcserver**</span><span class="sxs-lookup"><span data-stu-id="13ab4-147">**MprAdminGetPDCServer**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)

[<span data-ttu-id="13ab4-148">**Mpradminisservicerunning**</span><span class="sxs-lookup"><span data-stu-id="13ab4-148">**MprAdminIsServiceRunning**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)

[<span data-ttu-id="13ab4-149">**Mpradminlinkhangupnotification**</span><span class="sxs-lookup"><span data-stu-id="13ab4-149">**MprAdminLinkHangupNotification**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminlinkhangupnotification)

[<span data-ttu-id="13ab4-150">**Mpradminportreset**</span><span class="sxs-lookup"><span data-stu-id="13ab4-150">**MprAdminPortReset**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

[<span data-ttu-id="13ab4-151">**Mpradminserverconnect**</span><span class="sxs-lookup"><span data-stu-id="13ab4-151">**MprAdminServerConnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)

[<span data-ttu-id="13ab4-152">**Mpradminserverdisconnect**</span><span class="sxs-lookup"><span data-stu-id="13ab4-152">**MprAdminServerDisconnect**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

<span data-ttu-id="13ab4-153">Zusätzlich zu den oben genannten Funktionen fügen die Betriebssysteme Windows 2000 und höher die folgenden Funktionen hinzu:</span><span class="sxs-lookup"><span data-stu-id="13ab4-153">In addition to the preceding functions, Windows 2000 and later operating systems add the following functions:</span></span>

[<span data-ttu-id="13ab4-154">**Mpradminsendusermessage**</span><span class="sxs-lookup"><span data-stu-id="13ab4-154">**MprAdminSendUserMessage**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)

[<span data-ttu-id="13ab4-155">**MprAdminAcceptNewConnection2**</span><span class="sxs-lookup"><span data-stu-id="13ab4-155">**MprAdminAcceptNewConnection2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminacceptnewconnection2)

[<span data-ttu-id="13ab4-156">**MprAdminConnectionHangupNotification2**</span><span class="sxs-lookup"><span data-stu-id="13ab4-156">**MprAdminConnectionHangupNotification2**</span></span>](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionhangupnotification2)

 

 




