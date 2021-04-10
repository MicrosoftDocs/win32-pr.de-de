---
title: Internet Authentifizierungsdienst & Netzwerk Richtlinien Server
description: Der Internet Authentifizierungsdienst (IAS) wurde umbenannt in Netzwerk Richtlinien Server (Network Policy Server, NPS).
ms.assetid: c7c6d1a3-d0c8-469e-ae1e-a848ef7fee2b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca657da17e823caa51e8401905a8a0a3e307e975
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104039757"
---
# <a name="internet-authentication-service--network-policy-server"></a><span data-ttu-id="fe31b-103">Internet Authentifizierungsdienst & Netzwerk Richtlinien Server</span><span class="sxs-lookup"><span data-stu-id="fe31b-103">Internet Authentication Service & Network Policy Server</span></span>

<span data-ttu-id="fe31b-104">Der Internet Authentifizierungsdienst (IAS) wurde umbenannt in Netzwerk Richtlinien Server (Network Policy Server, NPS).</span><span class="sxs-lookup"><span data-stu-id="fe31b-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS).</span></span>

## <a name="internet-authentication-service"></a><span data-ttu-id="fe31b-105">Internetauthentifizierungsdienst</span><span class="sxs-lookup"><span data-stu-id="fe31b-105">Internet Authentication Service</span></span>

<span data-ttu-id="fe31b-106">Der Internet Authentifizierungsdienst ist die Microsoft-Implementierung eines RADIUS-Servers und-Proxys.</span><span class="sxs-lookup"><span data-stu-id="fe31b-106">Internet Authentication Service is the Microsoft implementation of a RADIUS server and proxy.</span></span>

<span data-ttu-id="fe31b-107">Der Internet Authentifizierungsdienst unterstützt zwei API-Sätze: API- [Erweiterungen für Netzwerk Richtlinien Server](ias-extensions.md) und [Server Data Objects-API](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="fe31b-107">Internet Authentication Service supports two API sets: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="fe31b-108">Weitere Informationen zu IAS finden Sie unter [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="fe31b-108">See [TechNet: Internet Authentication Service](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on IAS.</span></span>

## <a name="network-policy-server"></a><span data-ttu-id="fe31b-109">Netzwerkrichtlinienserver</span><span class="sxs-lookup"><span data-stu-id="fe31b-109">Network Policy Server</span></span>

<span data-ttu-id="fe31b-110">Der Netzwerk Richtlinien Server ist die Microsoft-Implementierung eines RADIUS-Servers und-Proxys und ist ab Windows Server 2008 auf Windows-Servern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe31b-110">Network Policy Server is the Microsoft implementation of a RADIUS server and proxy and it is available on Windows servers starting with Windows Server 2008.</span></span>

<span data-ttu-id="fe31b-111">NPS unterstützt die gleichen zwei API-Sätze wie die IAS: API für [Netzwerk Richtlinien Server-Erweiterungen](ias-extensions.md) und [Server Data Objects-API](server-data-objects.md).</span><span class="sxs-lookup"><span data-stu-id="fe31b-111">NPS supports the same two API sets as IAS: [Network Policy Server Extensions API](ias-extensions.md) and [Server Data Objects API](server-data-objects.md).</span></span>

<span data-ttu-id="fe31b-112">Außerdem enthält NPS eine Reihe neuer Features, mit denen die IAS-Funktionen erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="fe31b-112">In addition, NPS contains a set of new features that expand the IAS capabilities.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe31b-113">Funktion</span><span class="sxs-lookup"><span data-stu-id="fe31b-113">Feature</span></span></th>
<th><span data-ttu-id="fe31b-114">Neues für NPS</span><span class="sxs-lookup"><span data-stu-id="fe31b-114">What's new for NPS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe31b-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">Netzwerk Zugriffsschutz (Network Access Protection, NAP)</a></span><span class="sxs-lookup"><span data-stu-id="fe31b-115"><a href="/windows/desktop/NAP/network-access-protection-start-page">Network Access Protection (NAP)</a></span></span><br/></td>
<td><span data-ttu-id="fe31b-116">NPS ist der zentrale Server für den Netzwerk Zugriffsschutz.</span><span class="sxs-lookup"><span data-stu-id="fe31b-116">NPS is the central server of Network Access Protection.</span></span><br/> <span data-ttu-id="fe31b-117">NPS unterstützt das Erstellen von Richtlinien unter Verwendung der folgenden zusätzlichen Bedingungen:</span><span class="sxs-lookup"><span data-stu-id="fe31b-117">NPS supports policy authoring using the following additional conditions:</span></span><br/>
<ul>
<li><span data-ttu-id="fe31b-118">Ablauf der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="fe31b-118">Policy expiration.</span></span></li>
<li><span data-ttu-id="fe31b-119">Betriebssystemversion.</span><span class="sxs-lookup"><span data-stu-id="fe31b-119">Operating system version.</span></span></li>
<li><span data-ttu-id="fe31b-120">Zugriffs Client-IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="fe31b-120">Access client IP address.</span></span></li>
<li><span data-ttu-id="fe31b-121">Integritäts Richtlinien</span><span class="sxs-lookup"><span data-stu-id="fe31b-121">Health policies.</span></span></li>
<li><span data-ttu-id="fe31b-122">Zulässige EAP-Typen.</span><span class="sxs-lookup"><span data-stu-id="fe31b-122">Allowed EAP types.</span></span></li>
<li><span data-ttu-id="fe31b-123">HCAP.</span><span class="sxs-lookup"><span data-stu-id="fe31b-123">HCAP.</span></span></li>
</ul>
<span data-ttu-id="fe31b-124">NPS unterstützt die Richtlinien Erstellung mithilfe der folgenden zusätzlichen Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="fe31b-124">NPS supports policy authoring using the following additional settings:</span></span><br/>
<ul>
<li><span data-ttu-id="fe31b-125">Mend.</span><span class="sxs-lookup"><span data-stu-id="fe31b-125">Probation.</span></span></li>
<li><span data-ttu-id="fe31b-126">Eingeschränkter Zugriff.</span><span class="sxs-lookup"><span data-stu-id="fe31b-126">Limited access.</span></span></li>
<li><span data-ttu-id="fe31b-127">Erweiterter Status für eingeschränkten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="fe31b-127">Extended state for limited access.</span></span></li>
</ul>
<span data-ttu-id="fe31b-128">NPS über NAP interagiert mit Cisco NAC.</span><span class="sxs-lookup"><span data-stu-id="fe31b-128">NPS, through NAP, interoperates with CISCO NAC.</span></span><br/> <span data-ttu-id="fe31b-129">IAS unterstützt NAP nicht.</span><span class="sxs-lookup"><span data-stu-id="fe31b-129">IAS does not support NAP.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe31b-130"><a href="/windows/win32/eap/eap-start-page">EAP</a> Unterstützung von Richtlinien und <a href="/windows/win32/eaphost/portal">EAPHost</a></span><span class="sxs-lookup"><span data-stu-id="fe31b-130"><a href="/windows/win32/eap/eap-start-page">EAP</a> Policy and <a href="/windows/win32/eaphost/portal">EAPHost</a> Support</span></span><br/></td>
<td><span data-ttu-id="fe31b-131">NPS verwendet EAPHost für die Erweiterbarkeit von EAP-Methoden.</span><span class="sxs-lookup"><span data-stu-id="fe31b-131">NPS uses EAPHost for EAP method extensibility.</span></span> <span data-ttu-id="fe31b-132">Darüber hinaus können Administratoren die Netzwerk Zugriffs Richtlinie für EAP konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="fe31b-132">Additionally, administrators may configure network access policy for EAP.</span></span><br/> <span data-ttu-id="fe31b-133">IAS unterstützt keine EAPHost-Integration oder EAP-Typfilter Bedingungen für Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="fe31b-133">IAS does not support EAPHost integration, or EAP type filter conditions for policies.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe31b-134">IPv6-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="fe31b-134">IPv6 Support</span></span><br/></td>
<td><span data-ttu-id="fe31b-135">NPS unterstützt die Bereitstellung in IPv6-Umgebungen.</span><span class="sxs-lookup"><span data-stu-id="fe31b-135">NPS supports deployment in IPv6 environments.</span></span><br/> <span data-ttu-id="fe31b-136">IAS unterstützt keine IPv6-Netzwerkadressen.</span><span class="sxs-lookup"><span data-stu-id="fe31b-136">IAS does not support IPv6 network addresses.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe31b-137">XML-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="fe31b-137">XML Configuration</span></span><br/></td>
<td><span data-ttu-id="fe31b-138">Die NPS-Konfiguration kann im XML-Format importiert und exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="fe31b-138">NPS configuration can be imported and exported in XML format.</span></span><br/> <span data-ttu-id="fe31b-139">IAS verwendet eine Jet-Datenbank zum Speichern der Dienst Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="fe31b-139">IAS is using a Jet database for storing service configuration.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe31b-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Allgemeine Kriterien</a> Förder</span><span class="sxs-lookup"><span data-stu-id="fe31b-140"><a href="https://www.niap-ccevs.org/cc-scheme/">Common Criteria</a> Support</span></span><br/></td>
<td><span data-ttu-id="fe31b-141">NPS wurde aktualisiert, um die Bereitstellung in Umgebungen zu unterstützen, die die Common Criteria-Sicherheitsstandards erfüllen müssen.</span><span class="sxs-lookup"><span data-stu-id="fe31b-141">NPS has been updated to support its deployment in environments that must meet the Common Criteria security standards.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe31b-142"><a href="ias-extensions.md">NPS-Erweiterungs-API</a></span><span class="sxs-lookup"><span data-stu-id="fe31b-142"><a href="ias-extensions.md">NPS Extensions API</a></span></span><br/></td>
<td><span data-ttu-id="fe31b-143">Die NPS-Erweiterungs-DLLs werden in einem separaten Prozess als der NPS-Dienst ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fe31b-143">The NPS extension DLLs run in a separate process from the NPS service.</span></span> <span data-ttu-id="fe31b-144">Wenn eine Erweiterungs-DLL abstürzen soll, wird NPS weiterhin ausgeführt, und zukünftige Anforderungen werden abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="fe31b-144">Should an extension DLL crash, NPS will keep running and future requests will be rejected.</span></span><br/> <span data-ttu-id="fe31b-145">Die IAS-Erweiterungs-DLLs werden in demselben Prozess wie der IAS-Dienst ausgeführt und können sich negativ auf den Dienst auswirken.</span><span class="sxs-lookup"><span data-stu-id="fe31b-145">The IAS extension DLLs run in the same process as the IAS service and may adversely affect the service.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe31b-146">Verwaltungs Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="fe31b-146">Management User Interface</span></span><br/></td>
<td><span data-ttu-id="fe31b-147">Die NPS-Verwaltungskonsole (NPS. msc) verfügt über ein neues Erscheinungsbild, eine verbesserte Benutzerfreundlichkeit und deckt alle neuen Funktionen ab, die NPS hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fe31b-147">The NPS management console (nps.msc) has a new look, improved usability, and covers all the new functionality added to NPS.</span></span><br/> <span data-ttu-id="fe31b-148">IAS verwendet die IAS. msc-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="fe31b-148">IAS uses the ias.msc management console.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe31b-149">Rollen Verwaltungs Tool und Server-Manager Integration</span><span class="sxs-lookup"><span data-stu-id="fe31b-149">Role Management Tool and Server Manager Integration</span></span><br/></td>
<td><span data-ttu-id="fe31b-150">NPS ist in die Server-Manager und das Rollen Verwaltungs Tool integriert.</span><span class="sxs-lookup"><span data-stu-id="fe31b-150">NPS is integrated with the Server Manager and the Role Management Tool.</span></span> <span data-ttu-id="fe31b-151">Durch diese Integration wird die Konfiguration und Verwaltung von NPS und verwandten Szenarien vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="fe31b-151">This integration facilitates the configuration and management of NPS and related scenarios.</span></span><br/> <span data-ttu-id="fe31b-152">Server-Manager ist auf Computern, auf denen IAS ausgeführt wird, nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe31b-152">Server Manager is not available on computers running IAS.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe31b-153">Aktualisierte Befehlszeilen Skripts mit <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">netsh</a>.</span><span class="sxs-lookup"><span data-stu-id="fe31b-153">Updated Command Line Scripting with <a href="/previous-versions/windows/it-pro/windows-server-2003/cc785383(v=ws.10)">Netsh</a>.</span></span><br/></td>
<td><span data-ttu-id="fe31b-154">NPS unterstützt die &quot; netsh NPS- &quot; Befehlszeilenschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fe31b-154">NPS supports the &quot;Netsh nps&quot; command line interface.</span></span> <span data-ttu-id="fe31b-155">&quot;Netsh NPS &quot; enthält neue Befehle, mit denen NPS vollständig konfiguriert werden kann, einschließlich NAP-Features.</span><span class="sxs-lookup"><span data-stu-id="fe31b-155">&quot;Netsh nps&quot; contains new commands that permit to fully configure NPS, including NAP features.</span></span><br/> <span data-ttu-id="fe31b-156">IAS unterstützt die &quot; Netsh AAAA- &quot; Befehlszeilenschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="fe31b-156">IAS supports the &quot;Netsh aaaa&quot; command line interface.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe31b-157">Richtlinien Isolation</span><span class="sxs-lookup"><span data-stu-id="fe31b-157">Policy Isolation</span></span><br/></td>
<td><span data-ttu-id="fe31b-158">NPS ermöglicht die Implementierung der Richtlinien Isolation durch Festlegen der Netzwerk Richtlinien Quelle.</span><span class="sxs-lookup"><span data-stu-id="fe31b-158">NPS enables the implementation of policy isolation by setting the Network Policy Source.</span></span> <span data-ttu-id="fe31b-159">Richtlinien können so konfiguriert werden, dass Sie nur auf einen vordefinierten NAS-Typ anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="fe31b-159">Policies can be configured that are applicable only to a predetermined NAS type.</span></span><br/> <span data-ttu-id="fe31b-160">IAS unterstützt keine Richtlinien Isolation.</span><span class="sxs-lookup"><span data-stu-id="fe31b-160">IAS does not support policy isolation.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fe31b-161">Weitere Informationen zu NPS finden Sie unter [TechNet: Netzwerk Richtlinien Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="fe31b-161">See [TechNet: Network Policy Server](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/hh831683(v=ws.11)) for more information on NPS.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe31b-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fe31b-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe31b-163">RADIUS-Authentifizierung,-Autorisierung und-Kontoführung</span><span class="sxs-lookup"><span data-stu-id="fe31b-163">RADIUS Authentication, Authorization, and Accounting</span></span>](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[<span data-ttu-id="fe31b-164">Protokollierung mit dem Netzwerk Richtlinien Server</span><span class="sxs-lookup"><span data-stu-id="fe31b-164">Logging With Network Policy Server</span></span>](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> <dt>

[<span data-ttu-id="fe31b-165">Arbeiten mit einem Zustands Server</span><span class="sxs-lookup"><span data-stu-id="fe31b-165">Working with a State Server</span></span>](/windows/desktop/Nps/ias-working-with-a-state-server)
</dt> </dl>

