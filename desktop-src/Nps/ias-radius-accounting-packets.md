---
title: Protokollierung mit dem Netzwerk Richtlinien Server
description: Protokollierung mit dem Netzwerk Richtlinien Server
ms.assetid: 903d89bd-c223-4f29-9eaf-1dc28d27a32a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5117ce15731ea656913b47525387a48a39aa414c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315837"
---
# <a name="logging-with-network-policy-server"></a><span data-ttu-id="6f753-103">Protokollierung mit dem Netzwerk Richtlinien Server</span><span class="sxs-lookup"><span data-stu-id="6f753-103">Logging With Network Policy Server</span></span>

> [!Note]  
> <span data-ttu-id="6f753-104">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="6f753-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="6f753-105">Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS.</span><span class="sxs-lookup"><span data-stu-id="6f753-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="6f753-106">Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="6f753-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="6f753-107">In der folgenden Tabelle werden nur die wichtigsten Aspekte der RADIUS-Buchhaltungs Pakete beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6f753-107">The following table describes only the most important aspects of the RADIUS accounting packets.</span></span> <span data-ttu-id="6f753-108">In der RADIUS-Buchhaltungs Anforderung für Kommentare ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) finden Sie ausführliche Informationen zu diesen Paketen.</span><span class="sxs-lookup"><span data-stu-id="6f753-108">The RADIUS Accounting Request for Comments document ([RFC 2866](https://www.ietf.org/rfc/rfc2866.txt)) provides detailed information on these packets.</span></span>

<span data-ttu-id="6f753-109">RADIUS-Buchhaltungs Pakete können in die folgenden Kategorien unterteilt werden.</span><span class="sxs-lookup"><span data-stu-id="6f753-109">RADIUS accounting packets can be divided into the following categories.</span></span>



| <span data-ttu-id="6f753-110">Buchhaltungs Paket</span><span class="sxs-lookup"><span data-stu-id="6f753-110">Accounting packet</span></span>  | <span data-ttu-id="6f753-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f753-111">Description</span></span>                                                                                                                                                                                                                |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f753-112">Accounting-On</span><span class="sxs-lookup"><span data-stu-id="6f753-112">Accounting-On</span></span>      | <span data-ttu-id="6f753-113">Wird vom Netzwerk Zugriffs Server (NAS) gesendet, um anzugeben, dass er neu gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="6f753-113">Sent by the Network Access Server (NAS) to indicate that it has restarted.</span></span><br/> <span data-ttu-id="6f753-114">Enthält NAS-Identifier/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="6f753-114">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                        |
| <span data-ttu-id="6f753-115">Accounting-Off</span><span class="sxs-lookup"><span data-stu-id="6f753-115">Accounting-Off</span></span>     | <span data-ttu-id="6f753-116">Wird vom NAS gesendet, um anzugeben, dass es heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="6f753-116">Sent by the NAS to indicate that it is being shutdown.</span></span><br/> <span data-ttu-id="6f753-117">Enthält NAS-Identifier/IPAddress.</span><span class="sxs-lookup"><span data-stu-id="6f753-117">Contains nas-identifier/ipaddress.</span></span><br/>                                                                                                            |
| <span data-ttu-id="6f753-118">Accounting-Start</span><span class="sxs-lookup"><span data-stu-id="6f753-118">Accounting-Start</span></span>   | <span data-ttu-id="6f753-119">Wird vom NAS gesendet, nachdem der Benutzer authentifiziert und autorisiert wurde, um den Start einer Benutzersitzung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6f753-119">Sent by the NAS, after the user was authenticated and authorized, to indicate the start of a user session.</span></span> <br/> <span data-ttu-id="6f753-120">Enthält UserID, NAS-Identifier/IPAddress sowie andere Informationen, die vom NAS empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="6f753-120">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/> |
| <span data-ttu-id="6f753-121">Accounting-Stop</span><span class="sxs-lookup"><span data-stu-id="6f753-121">Accounting-Stop</span></span>    | <span data-ttu-id="6f753-122">Wird vom NAS gesendet, um das Ende einer Benutzersitzung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="6f753-122">Sent by the NAS to indicate the end of a user session.</span></span><br/> <span data-ttu-id="6f753-123">Enthält UserID, NAS-Identifier/IPAddress sowie andere Informationen, die vom NAS empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="6f753-123">Contains userid, nas-identifier/ipaddress, plus other information received from the NAS.</span></span><br/>                                                      |
| <span data-ttu-id="6f753-124">Accounting-Interim</span><span class="sxs-lookup"><span data-stu-id="6f753-124">Accounting-Interim</span></span> | <span data-ttu-id="6f753-125">Kann in regelmäßigen Abständen vom NAS für jeden Benutzer gesendet werden, der beim NAS angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="6f753-125">Could be sent periodically by the NAS for each user that is logged on at the NAS.</span></span> <br/> <span data-ttu-id="6f753-126">Diese Funktion wird im Allgemeinen in neueren Versionen von NAS unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6f753-126">This feature is generally supported in newer versions of NAS.</span></span><br/>                                                     |



 

<span data-ttu-id="6f753-127">Beim Erfassen von Buchhaltungsinformationen, die über RADIUS verfügbar gemacht werden, sind folgende Punkte zu beachten:</span><span class="sxs-lookup"><span data-stu-id="6f753-127">The following issues are important to consider when collecting accounting information made available through RADIUS:</span></span>

-   <span data-ttu-id="6f753-128">In seltenen Fällen können Pakete während der Übertragung verloren gehen und den RADIUS-Server möglicherweise nie erreichen.</span><span class="sxs-lookup"><span data-stu-id="6f753-128">In rare cases, packets could be lost during transmission and may never reach the RADIUS server.</span></span>
-   <span data-ttu-id="6f753-129">Der RADIUS-Server wird nicht benachrichtigt, wenn das NAS abbricht.</span><span class="sxs-lookup"><span data-stu-id="6f753-129">The RADIUS server is not notified if the NAS aborts.</span></span>
-   <span data-ttu-id="6f753-130">ISDN unterstützt mehrere Sitzungen, und jede Sitzung generiert ein paar von Paketen, die eine Buchführung starten/beenden.</span><span class="sxs-lookup"><span data-stu-id="6f753-130">ISDN supports multiple sessions and each session generates an Accounting-Start/-Stop pair of packets.</span></span> <span data-ttu-id="6f753-131">Es gibt ein Buchhaltungs Attribut mit dem Namen "mehrfache Sitzungs Bezeichner", mit dem solche Pakete mit mehreren Sitzungen eindeutig identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6f753-131">There is an accounting attribute called multi-session identifier that clearly identifies such multi-session packets.</span></span> <span data-ttu-id="6f753-132">Überprüfen Sie zusätzlich zur Sitzungs-ID den Bezeichner für mehrere Sitzungen, um die Anzahl der Sitzungen zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="6f753-132">Check for the multi-session identifier in addition to the session identifier to calculate the number of sessions.</span></span>

## <a name="requests-logged-by-nps"></a><span data-ttu-id="6f753-133">Von NPS protokollierte Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f753-133">Requests Logged by NPS</span></span>

<span data-ttu-id="6f753-134">NPS protokolliert standardmäßig keine Daten.</span><span class="sxs-lookup"><span data-stu-id="6f753-134">By default, NPS does not log any data.</span></span> <span data-ttu-id="6f753-135">NPS kann mithilfe der NPS-Benutzeroberfläche (NPS. msc) konfiguriert werden, um die folgenden Anforderungen zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="6f753-135">NPS can be configured, using the NPS user interface (nps.msc), to log the following requests.</span></span>



| <span data-ttu-id="6f753-136">Protokolliertes Paket</span><span class="sxs-lookup"><span data-stu-id="6f753-136">Logged packet</span></span>          | <span data-ttu-id="6f753-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6f753-137">Description</span></span>                                                                                                                                  |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f753-138">Buchhaltungs Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f753-138">Accounting Request</span></span>     | <span data-ttu-id="6f753-139">Alle in der vorherigen Tabelle beschriebenen Buchhaltungs Pakete.</span><span class="sxs-lookup"><span data-stu-id="6f753-139">Any of the accounting packets described in the previous table.</span></span><br/>                                                                    |
| <span data-ttu-id="6f753-140">Authentifizierungsanforderung</span><span class="sxs-lookup"><span data-stu-id="6f753-140">Authentication Request</span></span> | <span data-ttu-id="6f753-141">Wird vom NAS im Auftrag des Benutzers gesendet, der eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="6f753-141">Sent by the NAS on behalf of the connecting user.</span></span><br/> <span data-ttu-id="6f753-142">Die Protokolleinträge enthalten nur eingehende Attribute.</span><span class="sxs-lookup"><span data-stu-id="6f753-142">The log entries contain only incoming attributes.</span></span><br/>                    |
| <span data-ttu-id="6f753-143">Authentifizierungs Annahme</span><span class="sxs-lookup"><span data-stu-id="6f753-143">Authentication Accept</span></span>  | <span data-ttu-id="6f753-144">Wird von NPS gesendet, um anzugeben, dass die Benutzer Verbindung akzeptiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f753-144">Sent by NPS to indicate that the user connection should be accepted.</span></span><br/> <span data-ttu-id="6f753-145">Die Protokolleinträge enthalten nur ausgehende Attribute.</span><span class="sxs-lookup"><span data-stu-id="6f753-145">The log entries contain only outgoing attributes.</span></span><br/> |
| <span data-ttu-id="6f753-146">Authentifizierung ablehnen</span><span class="sxs-lookup"><span data-stu-id="6f753-146">Authentication Reject</span></span>  | <span data-ttu-id="6f753-147">Wird von NPS gesendet, um anzugeben, dass die Benutzer Verbindung abgelehnt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f753-147">Sent by NPS to indicate that the user connection should be rejected.</span></span><br/> <span data-ttu-id="6f753-148">Die Protokolleinträge enthalten nur ausgehende Attribute.</span><span class="sxs-lookup"><span data-stu-id="6f753-148">The log entries contain only outgoing attributes.</span></span><br/> |



 

<span data-ttu-id="6f753-149">Daten, die von NPS protokolliert werden, können in eine Textdatei auf dem NPS-Server oder in eine zentrale SQL-Datenbank aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="6f753-149">Data logged by NPS can go to a text file on the NPS server or to a central SQL database.</span></span> <span data-ttu-id="6f753-150">Weitere Informationen zur NPS-SQL-Protokollierung finden Sie unter [SQL-Programmierbarkeit](sql-programmability.md).</span><span class="sxs-lookup"><span data-stu-id="6f753-150">For more information on NPS SQL logging, see [SQL Programmability](sql-programmability.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f753-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6f753-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f753-152">Internet Authentifizierungsdienst und Netzwerk Richtlinien Server</span><span class="sxs-lookup"><span data-stu-id="6f753-152">Internet Authentication Service and Network Policy Server</span></span>](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[<span data-ttu-id="6f753-153">RADIUS-Authentifizierung,-Autorisierung und-Kontoführung</span><span class="sxs-lookup"><span data-stu-id="6f753-153">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="6f753-154">Arbeiten mit einem Zustands Server</span><span class="sxs-lookup"><span data-stu-id="6f753-154">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

 

