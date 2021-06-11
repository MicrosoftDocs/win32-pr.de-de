---
title: Internetauthentifizierungsdienst & Netzwerkrichtlinienserver
description: Erfahren Sie mehr über den Internetauthentifizierungsdienst und den Netzwerkrichtlinienserver. Internet Authentication Service (IAS) wurde in Network Policy Server (NPS) umbenannt.
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd62a50021c485c7bf51cdc9caff4360e4cc863
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989425"
---
# <a name="internet-authentication-service--network-policy-server"></a><span data-ttu-id="d12c5-104">Internetauthentifizierungsdienst & Netzwerkrichtlinienserver</span><span class="sxs-lookup"><span data-stu-id="d12c5-104">Internet Authentication Service & Network Policy Server</span></span>

<span data-ttu-id="d12c5-105">Internet Authentication Service (IAS) wurde in Network Policy Server (NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="d12c5-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span>

## <a name="internet-authentication-service"></a><span data-ttu-id="d12c5-106">Internetauthentifizierungsdienst</span><span class="sxs-lookup"><span data-stu-id="d12c5-106">Internet Authentication Service</span></span>

<span data-ttu-id="d12c5-107">Der Internetauthentifizierungsdienst ist die Microsoft-Implementierung eines RADIUS-Servers und -Proxys.</span><span class="sxs-lookup"><span data-stu-id="d12c5-107">Internet Authentication Service is the Microsoft implementation of a RADIUS server and proxy.</span></span>

<span data-ttu-id="d12c5-108">Der Internetauthentifizierungsdienst unterstützt zwei API-Sätze: [DIE API für Netzwerkrichtlinienservererweiterungen](ias-extensions.md) und [die Serverdatenobjekt-API.](server-data-objects.md)</span><span class="sxs-lookup"><span data-stu-id="d12c5-108">Internet Authentication Service supports two API sets: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="d12c5-109">Weitere Informationen zu IAS finden Sie unter [TechNet: Internet Authentication Service.](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="d12c5-109">See [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on IAS.</span></span>

## <a name="network-policy-server"></a><span data-ttu-id="d12c5-110">Netzwerkrichtlinienserver</span><span class="sxs-lookup"><span data-stu-id="d12c5-110">Network Policy Server</span></span>

<span data-ttu-id="d12c5-111">Der Netzwerkrichtlinienserver ist die Microsoft-Implementierung eines RADIUS-Servers und -Proxys und ab Windows Server 2008 auf Windows-Servern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d12c5-111">Network Policy Server is the Microsoft implementation of a RADIUS server and proxy and it is available on Windows servers starting with Windows Server 2008.</span></span>

<span data-ttu-id="d12c5-112">NPS unterstützt dieselben beiden API-Sätze wie IAS: API für [Netzwerkrichtlinienservererweiterungen](ias-extensions.md) und [Serverdatenobjekt-API.](server-data-objects.md)</span><span class="sxs-lookup"><span data-stu-id="d12c5-112">NPS supports the same two API sets as IAS: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="d12c5-113">Darüber hinaus enthält NPS eine Reihe neuer Features, die die IAS-Funktionen erweitern.</span><span class="sxs-lookup"><span data-stu-id="d12c5-113">In addition, NPS contains a set of new features that expand the IAS capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d12c5-114">Feature</span><span class="sxs-lookup"><span data-stu-id="d12c5-114">Feature</span></span></th>
<th><span data-ttu-id="d12c5-115">Neues für NPS</span><span class="sxs-lookup"><span data-stu-id="d12c5-115">What's new for NPS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d12c5-116"><a href="/windows/desktop/NAP/network-access-protection-start-page">Netzwerkzugriffsschutz (NETWORK Access Protection, NAP)</a></span><span class="sxs-lookup"><span data-stu-id="d12c5-116"><a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection (NAP)</a></span></span><br/></td>
<td><span data-ttu-id="d12c5-117">NPS ist der zentrale Server für den Netzwerkzugriffsschutz.</span><span class="sxs-lookup"><span data-stu-id="d12c5-117">NPS is the central server of Network Access Protection.</span></span><br/> <span data-ttu-id="d12c5-118">NPS unterstützt die Richtlinienerstellung mit den folgenden zusätzlichen Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="d12c5-118">NPS supports policy authoring using the following additional conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="d12c5-119">Ablauf der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d12c5-119">Policy expiration.</span></span></li>
<li><span data-ttu-id="d12c5-120">Betriebssystemversion.</span><span class="sxs-lookup"><span data-stu-id="d12c5-120">Operating system version.</span></span></li>
<li><span data-ttu-id="d12c5-121">Greifen Sie auf die Client-IP-Adresse zu.</span><span class="sxs-lookup"><span data-stu-id="d12c5-121">Access client IP address.</span></span></li>
<li><span data-ttu-id="d12c5-122">Integritätsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="d12c5-122">Health policies.</span></span></li>
<li><span data-ttu-id="d12c5-123">Zulässige EAP-Typen.</span><span class="sxs-lookup"><span data-stu-id="d12c5-123">Allowed EAP types.</span></span></li>
<li><span data-ttu-id="d12c5-124">Hcap.</span><span class="sxs-lookup"><span data-stu-id="d12c5-124">HCAP.</span></span></li>
</ul>
<span data-ttu-id="d12c5-125">NPS unterstützt die Richtlinienerstellung mit den folgenden zusätzlichen Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="d12c5-125">NPS supports policy authoring using the following additional settings:</span></span><br/>
<ul>
<li><span data-ttu-id="d12c5-126">Bewährung.</span><span class="sxs-lookup"><span data-stu-id="d12c5-126">Probation.</span></span></li>
<li><span data-ttu-id="d12c5-127">Eingeschränkter Zugriff.</span><span class="sxs-lookup"><span data-stu-id="d12c5-127">Limited access.</span></span></li>
<li><span data-ttu-id="d12c5-128">Erweiterter Zustand für eingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="d12c5-128">Extended state for limited access.</span></span></li>
</ul>
<span data-ttu-id="d12c5-129">NPS über NAP interoperiert mit CISCO NAC.</span><span class="sxs-lookup"><span data-stu-id="d12c5-129">NPS, through NAP, interoperates with CISCO NAC.</span></span><br/> <span data-ttu-id="d12c5-130">IAS unterstützt NAP nicht.</span><span class="sxs-lookup"><span data-stu-id="d12c5-130">IAS does not support NAP.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d12c5-131"><a href="/windows/win32/eap/eap-start-page">EAP</a> Richtlinien- und <a href="/windows/win32/eaphost/portal">EAPHost-Unterstützung</a></span><span class="sxs-lookup"><span data-stu-id="d12c5-131"><a href="/windows/win32/eap/eap-start-page">EAP</a> Policy and <a href="/windows/win32/eaphost/portal">EAPHost</a> Support</span></span><br/></td>
<td><span data-ttu-id="d12c5-132">NPS verwendet EAPHost für die Erweiterbarkeit von EAP-Methoden.</span><span class="sxs-lookup"><span data-stu-id="d12c5-132">NPS uses EAPHost for EAP method extensibility.</span></span> <span data-ttu-id="d12c5-133">Darüber hinaus können Administratoren netzwerkzugriffsrichtlinie für EAP konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d12c5-133">Additionally, administrators may configure network access policy for EAP.</span></span><br/> <span data-ttu-id="d12c5-134">IAS unterstützt keine EAPHost-Integration oder Filterbedingungen für Richtlinien vom Typ EAP.</span><span class="sxs-lookup"><span data-stu-id="d12c5-134">IAS does not support EAPHost integration, or EAP type filter conditions for policies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d12c5-135">IPv6-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d12c5-135">IPv6 Support</span></span><br/></td>
<td><span data-ttu-id="d12c5-136">NPS unterstützt die Bereitstellung in IPv6-Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="d12c5-136">NPS supports deployment in IPv6 environments.</span></span><br/> <span data-ttu-id="d12c5-137">IAS unterstützt keine IPv6-Netzwerkadressen.</span><span class="sxs-lookup"><span data-stu-id="d12c5-137">IAS does not support IPv6 network addresses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d12c5-138">XML-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d12c5-138">XML Configuration</span></span><br/></td>
<td><span data-ttu-id="d12c5-139">Die NPS-Konfiguration kann im XML-Format importiert und exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="d12c5-139">NPS configuration can be imported and exported in XML format.</span></span><br/> <span data-ttu-id="d12c5-140">IAS verwendet eine Jet-Datenbank zum Speichern der Dienstkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="d12c5-140">IAS is using a Jet database for storing service configuration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d12c5-141"><a href="https://www.niap-ccevs.org/cc-scheme/">Allgemeine Kriterien</a> Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d12c5-141"><a href="https://www.niap-ccevs.org/cc-scheme/">Common Criteria</a> Support</span></span><br/></td>
<td><span data-ttu-id="d12c5-142">NPS wurde aktualisiert, um die Bereitstellung in Umgebungen zu unterstützen, die die Common Criteria-Sicherheitsstandards erfüllen müssen.</span><span class="sxs-lookup"><span data-stu-id="d12c5-142">NPS has been updated to support its deployment in environments that must meet the Common Criteria security standards.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d12c5-143"><a href="ias-extensions.md">NPS-Erweiterungs-API</a></span><span class="sxs-lookup"><span data-stu-id="d12c5-143"><a href="ias-extensions.md">NPS Extensions API</a></span></span><br/></td>
<td><span data-ttu-id="d12c5-144">Die NPS-Erweiterungs-DLLs werden in einem separaten Prozess als der NPS-Dienst ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d12c5-144">The NPS extension DLLs run in a separate process from the NPS service.</span></span> <span data-ttu-id="d12c5-145">Sollte eine Erweiterungs-DLL abstürzen, wird NPS weiterhin ausgeführt, und zukünftige Anforderungen werden abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="d12c5-145">Should an extension DLL crash, NPS will keep running and future requests will be rejected.</span></span><br/> <span data-ttu-id="d12c5-146">Die DLLs der IAS-Erweiterung werden im gleichen Prozess wie der IAS-Dienst ausgeführt und können sich negativ auf den Dienst auswirken.</span><span class="sxs-lookup"><span data-stu-id="d12c5-146">The IAS extension DLLs run in the same process as the IAS service and may adversely affect the service.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d12c5-147">Verwaltungs Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d12c5-147">Management User Interface</span></span><br/></td>
<td><span data-ttu-id="d12c5-148">Die NPS-Verwaltungskonsole (nps.msc) hat ein neues Aussehen, verbesserte Benutzerfreundlichkeit und deckt alle neuen Funktionen ab, die NPS hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="d12c5-148">The NPS management console (nps.msc) has a new look, improved usability, and covers all the new functionality added to NPS.</span></span><br/> <span data-ttu-id="d12c5-149">IAS verwendet die verwaltungskonsole "ias.msc".</span><span class="sxs-lookup"><span data-stu-id="d12c5-149">IAS uses the ias.msc management console.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d12c5-150">Rollenverwaltungstool und Server-Manager Integration</span><span class="sxs-lookup"><span data-stu-id="d12c5-150">Role Management Tool and Server Manager Integration</span></span><br/></td>
<td><span data-ttu-id="d12c5-151">NPS ist in das Server-Manager und das Rollenverwaltungstool integriert.</span><span class="sxs-lookup"><span data-stu-id="d12c5-151">NPS is integrated with the Server Manager and the Role Management Tool.</span></span> <span data-ttu-id="d12c5-152">Diese Integration erleichtert die Konfiguration und Verwaltung von NPS und verwandten Szenarien.</span><span class="sxs-lookup"><span data-stu-id="d12c5-152">This integration facilitates the configuration and management of NPS and related scenarios.</span></span><br/> <span data-ttu-id="d12c5-153">Server-Manager ist auf Computern mit IAS nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d12c5-153">Server Manager is not available on computers running IAS.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d12c5-154">Die Befehlszeilenskripterstellung mit <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh wurde aktualisiert.</a></span><span class="sxs-lookup"><span data-stu-id="d12c5-154">Updated Command Line Scripting with <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>.</span></span><br/></td>
<td><span data-ttu-id="d12c5-155">NPS unterstützt die &quot; Netsh &quot; nps-Befehlszeilenschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d12c5-155">NPS supports the &quot;Netsh nps&quot; command line interface.</span></span> <span data-ttu-id="d12c5-156">&quot;Netsh nps enthält neue Befehle, mit denen NPS vollständig konfiguriert werden &quot; kann, einschließlich NAP-Features.</span><span class="sxs-lookup"><span data-stu-id="d12c5-156">&quot;Netsh nps&quot; contains new commands that permit to fully configure NPS, including NAP features.</span></span><br/> <span data-ttu-id="d12c5-157">IAS unterstützt die &quot; Netsh &quot; aaaa-Befehlszeilenschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d12c5-157">IAS supports the &quot;Netsh aaaa&quot; command line interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d12c5-158">Richtlinienisolation</span><span class="sxs-lookup"><span data-stu-id="d12c5-158">Policy Isolation</span></span><br/></td>
<td><span data-ttu-id="d12c5-159">NPS ermöglicht die Implementierung der Richtlinienisolation durch Festlegen der Netzwerkrichtlinienquelle.</span><span class="sxs-lookup"><span data-stu-id="d12c5-159">NPS enables the implementation of policy isolation by setting the Network Policy Source.</span></span> <span data-ttu-id="d12c5-160">Es können Richtlinien konfiguriert werden, die nur für einen vordefinierten NAS-Typ gelten.</span><span class="sxs-lookup"><span data-stu-id="d12c5-160">Policies can be configured that are applicable only to a predetermined NAS type.</span></span><br/> <span data-ttu-id="d12c5-161">IAS unterstützt keine Richtlinienisolation.</span><span class="sxs-lookup"><span data-stu-id="d12c5-161">IAS does not support policy isolation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d12c5-162">Weitere Informationen zu NPS finden Sie unter [TechNet:](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) Netzwerkrichtlinienserver.</span><span class="sxs-lookup"><span data-stu-id="d12c5-162">See [TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on NPS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d12c5-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d12c5-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d12c5-164">RADIUS-Authentifizierung, -Autorisierung und -Kontoführung</span><span class="sxs-lookup"><span data-stu-id="d12c5-164">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="d12c5-165">Protokollierung mit Netzwerkrichtlinienserver</span><span class="sxs-lookup"><span data-stu-id="d12c5-165">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="d12c5-166">Arbeiten mit einem Zustandsserver</span><span class="sxs-lookup"><span data-stu-id="d12c5-166">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

