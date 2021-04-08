---
title: Überwachung
description: Windows-Filter Plattform (WFP) ermöglicht die Überwachung von Firewall-und IPSec-bezogenen Ereignissen.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "103949283"
---
# <a name="auditing"></a><span data-ttu-id="4a931-103">Überwachung</span><span class="sxs-lookup"><span data-stu-id="4a931-103">Auditing</span></span>

<span data-ttu-id="4a931-104">Die Windows-Filter Plattform (WFP) ermöglicht die Überwachung von Firewall-und IPSec-bezogenen Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="4a931-104">The Windows Filtering Platform (WFP) provides auditing of firewall and IPsec related events.</span></span> <span data-ttu-id="4a931-105">Diese Ereignisse werden im System Sicherheitsprotokoll gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4a931-105">These events are stored in the system security log.</span></span>

<span data-ttu-id="4a931-106">Die überwachten Ereignisse lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="4a931-106">The audited events are as follows.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4a931-107">Kategorie "Überwachung"</span><span class="sxs-lookup"><span data-stu-id="4a931-107">Auditing category</span></span></th>
<th><span data-ttu-id="4a931-108">Überwachungsunterkategorie</span><span class="sxs-lookup"><span data-stu-id="4a931-108">Auditing subcategory</span></span></th>
<th><span data-ttu-id="4a931-109">Überwachte Ereignisse</span><span class="sxs-lookup"><span data-stu-id="4a931-109">Audited events</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4a931-110">Richtlinienänderung</span><span class="sxs-lookup"><span data-stu-id="4a931-110">Policy Change</span></span><br/> <span data-ttu-id="4a931-111">{6997984d-797a-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-111">{6997984D-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4a931-112">Filtern von Platt Form Richtlinien Änderungen</span><span class="sxs-lookup"><span data-stu-id="4a931-112">Filtering Platform Policy Change</span></span><br/> <span data-ttu-id="4a931-113">{0cce9233-69ae-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4a931-114">Die Zahlen stellen die Ereignis-IDs dar, die von Ereignisanzeige (eventvwr.exe) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4a931-114">The numbers represent the Event IDs as displayed by Event Viewer (eventvwr.exe).</span></span>
</blockquote>
<br/> <span data-ttu-id="4a931-115">Hinzufügen und Entfernen von WFP-Objekten:</span><span class="sxs-lookup"><span data-stu-id="4a931-115">WFP object addition and removal:</span></span><br/>
<ul>
<li><span data-ttu-id="4a931-116">5440 permanente Legende wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4a931-116">5440 Persistent callout added</span></span></li>
<li><span data-ttu-id="4a931-117">5441 Start-oder persistente Filter hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4a931-117">5441 Boot-time or persistent filter added</span></span></li>
<li><span data-ttu-id="4a931-118">5442 permanenter Anbieter hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4a931-118">5442 Persistent provider added</span></span></li>
<li><span data-ttu-id="4a931-119">5443 persistenter Anbieter Kontext hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4a931-119">5443 Persistent provider context added</span></span></li>
<li><span data-ttu-id="4a931-120">5444 persistente Unterebene hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4a931-120">5444 Persistent sub-layer added</span></span></li>
<li><span data-ttu-id="4a931-121">5446-Lauf Zeit Aufruf hinzugefügt oder entfernt</span><span class="sxs-lookup"><span data-stu-id="4a931-121">5446 Run-time callout added or removed</span></span></li>
<li><span data-ttu-id="4a931-122">5447-Lauf Zeitfilter hinzugefügt oder entfernt</span><span class="sxs-lookup"><span data-stu-id="4a931-122">5447 Run-time filter added or removed</span></span></li>
<li><span data-ttu-id="4a931-123">5448-Lauf Zeit Anbieter hinzugefügt oder entfernt</span><span class="sxs-lookup"><span data-stu-id="4a931-123">5448 Run-time provider added or removed</span></span></li>
<li><span data-ttu-id="4a931-124">5449-Lauf Zeit Anbieter Kontext hinzugefügt oder entfernt</span><span class="sxs-lookup"><span data-stu-id="4a931-124">5449 Run-time provider context added or removed</span></span></li>
<li><span data-ttu-id="4a931-125">5450-Lauf Zeit Unterschicht hinzugefügt oder entfernt</span><span class="sxs-lookup"><span data-stu-id="4a931-125">5450 Run-time sub-layer added or removed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a931-126">Objektzugriff</span><span class="sxs-lookup"><span data-stu-id="4a931-126">Object Access</span></span><br/> <span data-ttu-id="4a931-127">{6997984a-797a-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-127">{6997984A-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4a931-128">Filtern von Platt Form Paketen</span><span class="sxs-lookup"><span data-stu-id="4a931-128">Filtering Platform Packet Drop</span></span> <br/> <span data-ttu-id="4a931-129">{0cce9225-69ae-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4a931-130">Von WFP gelöschte Pakete:</span><span class="sxs-lookup"><span data-stu-id="4a931-130">Packets dropped by WFP:</span></span><br/>
<ul>
<li><span data-ttu-id="4a931-131">5152 Paket gelöscht</span><span class="sxs-lookup"><span data-stu-id="4a931-131">5152 Packet dropped</span></span></li>
<li><span data-ttu-id="4a931-132">5153 Paket wurde überprüft.</span><span class="sxs-lookup"><span data-stu-id="4a931-132">5153 Packet vetoed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a931-133">Objektzugriff</span><span class="sxs-lookup"><span data-stu-id="4a931-133">Object Access</span></span><br/></td>
<td><span data-ttu-id="4a931-134">Platt Form Verbindung wird gefiltert</span><span class="sxs-lookup"><span data-stu-id="4a931-134">Filtering Platform Connection</span></span> <br/> <span data-ttu-id="4a931-135">{0cce9226-69ae-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4a931-136">Zulässige und blockierte Verbindungen:</span><span class="sxs-lookup"><span data-stu-id="4a931-136">Allowed and blocked connections:</span></span><br/>
<ul>
<li><span data-ttu-id="4a931-137">5154 lauschen zulässig</span><span class="sxs-lookup"><span data-stu-id="4a931-137">5154 Listen permitted</span></span></li>
<li><span data-ttu-id="4a931-138">5155 lauschen blockiert</span><span class="sxs-lookup"><span data-stu-id="4a931-138">5155 Listen blocked</span></span></li>
<li><span data-ttu-id="4a931-139">5156 Verbindung zulässig</span><span class="sxs-lookup"><span data-stu-id="4a931-139">5156 Connection permitted</span></span></li>
<li><span data-ttu-id="4a931-140">5157 Verbindung blockiert</span><span class="sxs-lookup"><span data-stu-id="4a931-140">5157 Connection blocked</span></span></li>
<li><span data-ttu-id="4a931-141">5158 Bindung zulässig</span><span class="sxs-lookup"><span data-stu-id="4a931-141">5158 Bind permitted</span></span></li>
<li><span data-ttu-id="4a931-142">5159 Bindung blockiert</span><span class="sxs-lookup"><span data-stu-id="4a931-142">5159 Bind blocked</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="4a931-143">Zulässige Verbindungen überwachen nicht immer die ID des zugeordneten Filters.</span><span class="sxs-lookup"><span data-stu-id="4a931-143">Permitted connections do not always audit the ID of the associated filter.</span></span> <span data-ttu-id="4a931-144">Die Filter-ID für TCP ist 0, es sei denn, es wird eine Teilmenge dieser Filterbedingungen verwendet: UserID, AppID, Protocol, Remoteport.</span><span class="sxs-lookup"><span data-stu-id="4a931-144">The FilterID for TCP will be 0 unless a subset of these filtering conditions are used: UserID, AppID, Protocol, Remote Port.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a931-145">Objektzugriff</span><span class="sxs-lookup"><span data-stu-id="4a931-145">Object Access</span></span><br/></td>
<td><span data-ttu-id="4a931-146">Andere Objekt Zugriffsereignisse</span><span class="sxs-lookup"><span data-stu-id="4a931-146">Other Object Access Events</span></span><br/> <span data-ttu-id="4a931-147">{0cce9227-69ae-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="4a931-148">Diese Unterkategorie ermöglicht viele Überwachungen.</span><span class="sxs-lookup"><span data-stu-id="4a931-148">This subcategory enables many audits.</span></span> <span data-ttu-id="4a931-149">Die folgenden WFP-Überwachungen sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a931-149">WFP specific audits are listed below.</span></span>
</blockquote>
<br/> <span data-ttu-id="4a931-150">Denial-of-Service-Schutzstatus:</span><span class="sxs-lookup"><span data-stu-id="4a931-150">Denial of Service prevention status:</span></span><br/>
<ul>
<li><span data-ttu-id="4a931-151">5148 WFP-DOS-Präventions Modus wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="4a931-151">5148 WFP DoS prevention mode started</span></span></li>
<li><span data-ttu-id="4a931-152">5149 der WFP-DOS-Präventions Modus wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="4a931-152">5149 WFP DoS prevention mode stopped</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a931-153">Anmeldung/Abmeldung</span><span class="sxs-lookup"><span data-stu-id="4a931-153">Logon/Logoff</span></span><br/> <span data-ttu-id="4a931-154">{69979849-797a-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-154">{69979849-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4a931-155">IPSec-Hauptmodus</span><span class="sxs-lookup"><span data-stu-id="4a931-155">IPsec Main Mode</span></span><br/> <span data-ttu-id="4a931-156">{0cce9218-69ae-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4a931-157">IKE-und AuthIP-Hauptmodusaushandlung:</span><span class="sxs-lookup"><span data-stu-id="4a931-157">IKE and AuthIP Main Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="4a931-158">4650, 4651 Sicherheits Zuordnung eingerichtet</span><span class="sxs-lookup"><span data-stu-id="4a931-158">4650, 4651 Security association established</span></span></li>
<li><span data-ttu-id="4a931-159">4652, 4653-Aushandlung fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="4a931-159">4652, 4653 Negotiation failed</span></span></li>
<li><span data-ttu-id="4a931-160">4655 Sicherheits Zuordnung beendet</span><span class="sxs-lookup"><span data-stu-id="4a931-160">4655 Security association ended</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a931-161">Anmeldung/Abmeldung</span><span class="sxs-lookup"><span data-stu-id="4a931-161">Logon/Logoff</span></span><br/></td>
<td><span data-ttu-id="4a931-162">IPSec-Schnellmodus</span><span class="sxs-lookup"><span data-stu-id="4a931-162">IPsec Quick Mode</span></span> <br/> <span data-ttu-id="4a931-163">{0cce9219-69ae-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4a931-164">IKE-und AuthIP-Schnellmodus-Aushandlung:</span><span class="sxs-lookup"><span data-stu-id="4a931-164">IKE and AuthIP Quick Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="4a931-165">5451 Sicherheits Zuordnung eingerichtet</span><span class="sxs-lookup"><span data-stu-id="4a931-165">5451 Security association established</span></span></li>
<li><span data-ttu-id="4a931-166">5452 Sicherheits Zuordnung beendet</span><span class="sxs-lookup"><span data-stu-id="4a931-166">5452 Security association ended</span></span></li>
<li><span data-ttu-id="4a931-167">4654 Aushandlung fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="4a931-167">4654 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a931-168">Anmeldung/Abmeldung</span><span class="sxs-lookup"><span data-stu-id="4a931-168">Logon/Logoff</span></span> <br/></td>
<td><span data-ttu-id="4a931-169">Erweiterter IPSec-Modus</span><span class="sxs-lookup"><span data-stu-id="4a931-169">IPsec Extended Mode</span></span><br/> <span data-ttu-id="4a931-170">{0cce921a-69ae-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4a931-171">AuthIP-Aushandlung im erweiterten Modus:</span><span class="sxs-lookup"><span data-stu-id="4a931-171">AuthIP Extended Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="4a931-172">4978 ungültiges Aushandlungs Paket.</span><span class="sxs-lookup"><span data-stu-id="4a931-172">4978 Invalid negotiation packet</span></span></li>
<li><span data-ttu-id="4a931-173">4979, 4980, 4981, 4982 Sicherheits Zuordnung eingerichtet</span><span class="sxs-lookup"><span data-stu-id="4a931-173">4979, 4980, 4981, 4982 Security association established</span></span></li>
<li><span data-ttu-id="4a931-174">4983, 4984-Aushandlung fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="4a931-174">4983, 4984 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a931-175">System</span><span class="sxs-lookup"><span data-stu-id="4a931-175">System</span></span><br/> <span data-ttu-id="4a931-176">{69979848-797a-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-176">{69979848-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4a931-177">IPSec-Treiber</span><span class="sxs-lookup"><span data-stu-id="4a931-177">IPsec Driver</span></span><br/> <span data-ttu-id="4a931-178">{0cce9213-69ae-11d9-bed3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="4a931-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="4a931-179">Vom IPSec-Treiber gelöschte Pakete:</span><span class="sxs-lookup"><span data-stu-id="4a931-179">Packets dropped by the IPsec driver:</span></span><br/>
<ul>
<li><span data-ttu-id="4a931-180">4963 eingehender Klartext-Paket wurde gelöscht</span><span class="sxs-lookup"><span data-stu-id="4a931-180">4963 Inbound clear text packet dropped</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4a931-181">Standardmäßig ist die Überwachung für WFP deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4a931-181">By default, auditing for WFP is disabled.</span></span>

<span data-ttu-id="4a931-182">Die Überwachung kann auf kategoriebasis entweder über das MMC-Snap-in Gruppenrichtlinienobjekt-Editor, über das MMC-Snap-in "lokale Sicherheitsrichtlinie" oder über den auditpol.exe-Befehl aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="4a931-182">Auditing can be enabled on a per-category basis through either the Group Policy Object Editor MMC snap-in, the Local Security Policy MMC snap-in, or the auditpol.exe command.</span></span>

<span data-ttu-id="4a931-183">Wenn Sie z. b. die Überwachung von Richtlinien Änderungs Ereignissen aktivieren möchten, können Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="4a931-183">For example, to enable the auditing of Policy Change events you may:</span></span>

-   <span data-ttu-id="4a931-184">Verwenden Sie die Gruppenrichtlinienobjekt-Editor</span><span class="sxs-lookup"><span data-stu-id="4a931-184">Use the Group Policy Object Editor</span></span>

    1.  <span data-ttu-id="4a931-185">Führen Sie **gpeer dit. msc** aus.</span><span class="sxs-lookup"><span data-stu-id="4a931-185">Run **gpedit.msc**.</span></span>
    2.  <span data-ttu-id="4a931-186">Erweitern Sie lokale Computer Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4a931-186">Expand Local Computer Policy.</span></span>
    3.  <span data-ttu-id="4a931-187">Erweitern Sie Computer Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4a931-187">Expand Computer Configuration.</span></span>
    4.  <span data-ttu-id="4a931-188">Erweitern Sie Windows-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="4a931-188">Expand Windows Settings.</span></span>
    5.  <span data-ttu-id="4a931-189">Erweitern Sie Sicherheitseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="4a931-189">Expand Security Settings.</span></span>
    6.  <span data-ttu-id="4a931-190">Erweitern Sie lokale Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="4a931-190">Expand Local Policies.</span></span>
    7.  <span data-ttu-id="4a931-191">Klicken Sie auf Überwachungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="4a931-191">Click Audit Policy.</span></span>
    8.  <span data-ttu-id="4a931-192">Doppelklicken Sie auf Überwachungs Richtlinien Änderung, um das Dialogfeld Eigenschaften zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4a931-192">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    9.  <span data-ttu-id="4a931-193">Aktivieren Sie die Kontrollkästchen erfolgreich und Fehler.</span><span class="sxs-lookup"><span data-stu-id="4a931-193">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="4a931-194">Lokale Sicherheitsrichtlinie verwenden</span><span class="sxs-lookup"><span data-stu-id="4a931-194">Use the Local Security Policy</span></span>

    1.  <span data-ttu-id="4a931-195">Führen Sie **secpol. msc** aus.</span><span class="sxs-lookup"><span data-stu-id="4a931-195">Run **secpol.msc**.</span></span>
    2.  <span data-ttu-id="4a931-196">Erweitern Sie lokale Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="4a931-196">Expand Local Policies.</span></span>
    3.  <span data-ttu-id="4a931-197">Klicken Sie auf Überwachungsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="4a931-197">Click Audit Policy.</span></span>
    4.  <span data-ttu-id="4a931-198">Doppelklicken Sie auf Überwachungs Richtlinien Änderung, um das Dialogfeld Eigenschaften zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4a931-198">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    5.  <span data-ttu-id="4a931-199">Aktivieren Sie die Kontrollkästchen erfolgreich und Fehler.</span><span class="sxs-lookup"><span data-stu-id="4a931-199">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="4a931-200">Verwenden des Befehls "auditpol.exe"</span><span class="sxs-lookup"><span data-stu-id="4a931-200">Use the auditpol.exe command</span></span>

    -   <span data-ttu-id="4a931-201">**Auditpol/Set/Category: "Richtlinien Änderung"/Success: enable/Failure: enable**</span><span class="sxs-lookup"><span data-stu-id="4a931-201">**auditpol /set /category:"Policy Change" /success:enable /failure:enable**</span></span>

<span data-ttu-id="4a931-202">Die Überwachung kann nur über den auditpol.exe Befehl auf der Basis einer einzelnen Unterkategorie aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="4a931-202">Auditing can be enabled on a per-subcategory basis only through the auditpol.exe command.</span></span>

<span data-ttu-id="4a931-203">Die Kategorien "Auditing" und "SubCategory" sind lokalisiert.</span><span class="sxs-lookup"><span data-stu-id="4a931-203">The auditing category and subcategory names are localized.</span></span> <span data-ttu-id="4a931-204">Um die Lokalisierung für das Überwachen von Skripts zu vermeiden, können die entsprechenden GUIDs anstelle der Namen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a931-204">To avoid localization for auditing scripts, the corresponding GUIDs may be used in place of the names.</span></span>

<span data-ttu-id="4a931-205">Beispielsweise können Sie einen der folgenden Befehle verwenden, um die Überwachung von Richtlinien Änderungs Ereignissen für Filter Plattformen zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="4a931-205">For example, to enable the auditing of Filtering Platform Policy Change events you may use either one of the following commands:</span></span>

-   <span data-ttu-id="4a931-206">**Auditpol/Set/SubCategory: "Filtern von Platt Form Richtlinien ändern"/Success: enable/Failure: enable**</span><span class="sxs-lookup"><span data-stu-id="4a931-206">**auditpol /set /subcategory:"Filtering Platform Policy Change" /success:enable /failure:enable**</span></span>
-   <span data-ttu-id="4a931-207">**Auditpol/Set/SubCategory: "{0cce9233-69ae-11d9-bed3-505054503030}"/Success: enable/Failure: enable**</span><span class="sxs-lookup"><span data-stu-id="4a931-207">**auditpol /set /subcategory:"{0CCE9233-69AE-11D9-BED3-505054503030}" /success:enable /failure:enable**</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a931-208">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a931-208">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4a931-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="4a931-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="4a931-210">[Ereignisprotokoll](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4a931-210">[Event Log](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="4a931-211">Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="4a931-211">Group Policy</span></span>](/windows/deployment/deploy-whats-new)
</dt> </dl>

