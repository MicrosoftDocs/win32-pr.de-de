---
description: Zusätzliche Windows-Ressourcenschutz zu Registrierungsschlüsseln
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Zusätzliche Windows-Ressourcenschutz zu Registrierungsschlüsseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1beeea49f06da182b5ebba38d09227134a6d92c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088778"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a><span data-ttu-id="9d4c1-103">Zusätzliche Windows-Ressourcenschutz zu Registrierungsschlüsseln</span><span class="sxs-lookup"><span data-stu-id="9d4c1-103">Additional Windows Resource Protection on Registry Keys</span></span>

## <a name="platform"></a><span data-ttu-id="9d4c1-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="9d4c1-104">Platform</span></span>

<span data-ttu-id="9d4c1-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="9d4c1-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="9d4c1-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9d4c1-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="9d4c1-107">Auswirkung von Features</span><span class="sxs-lookup"><span data-stu-id="9d4c1-107">Feature Impact</span></span>

<span data-ttu-id="9d4c1-108">**Schweregrad:** Mittel</span><span class="sxs-lookup"><span data-stu-id="9d4c1-108">**Severity** - Medium</span></span>  
<span data-ttu-id="9d4c1-109">**Häufigkeit** – Niedrig</span><span class="sxs-lookup"><span data-stu-id="9d4c1-109">**Frequency** - Low</span></span>  


## <a name="description"></a><span data-ttu-id="9d4c1-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d4c1-110">Description</span></span>

<span data-ttu-id="9d4c1-111">Zusätzliche Systemressourcen haben Windows-Ressourcenschutz (WRP)-Einstellungen in Windows 7 hinzugefügt, wodurch sie schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-111">Additional system resources have added Windows Resource Protection (WRP) settings in Windows 7, making them read-only settings.</span></span> <span data-ttu-id="9d4c1-112">Die große Mehrheit der Ressourcen, die zusätzlichen Schutz erhalten haben, sind COM-Systemserverschlüssel, obwohl einige Features einen gezielten Ressourcenschutz hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-112">The vast majority of resources that received added protection are system COM server keys, although some features have added targeted resource protection.</span></span> <span data-ttu-id="9d4c1-113">Microsoft hat diese Ressourcen geändert, um das System und andere Anwendungen vor dem Unterbrechen zu schützen und eine konsistente, stabile Plattform zu bieten, auf der Anwendungen zuverlässig ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-113">Microsoft changed these resources in order to protect the system and other applications from breaking each other and to provide a consistent, stable platform upon which applications can reliably run.</span></span> <span data-ttu-id="9d4c1-114">In der Vergangenheit konnten Anwendungen benutzerdefinierte Dateien bereitstellen und die ungeschützte COM-Registrierung verwenden, um das System zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-114">In the past, applications could provide custom files and use the unprotected COM registration to change the system.</span></span> <span data-ttu-id="9d4c1-115">Bei älteren Anwendungen kann dies systemlaufzeiten herabstufen oder die Schnittstelle ändern, auf der andere Anwendungen ordnungsgemäß funktionieren müssen.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-115">In the case of older applications, this can downgrade system runtimes or change the interface upon which other applications needed to work properly.</span></span> <span data-ttu-id="9d4c1-116">Im schlimmsten Fall können solche Installationen zu Einem Systemausfall oder einer Verschlechterung im Laufe der Zeit führen.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-116">In the worst case, such installations could cause system failure or degradation over time.</span></span> <span data-ttu-id="9d4c1-117">Um eine bessere Benutzererfahrung und eine stabilere Anwendungsplattform zu bieten, haben wir diese Registrierungen gesperrt, sodass nur Microsoft-Updates Systemkomponenten ändern können.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-117">To provide a better experience and a more stable application platform, we locked down these registrations so that only Microsoft updates could change system components.</span></span>

<span data-ttu-id="9d4c1-118">Da es sich bei den meisten geänderten Ressourcen um COM-Schlüssel handelt, die vom System verwendet werden, wirkt sich diese Änderung nicht auf die Mehrheit der Anwendungen aus.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-118">Since most resources changed are COM keys used by the system, this change will not affect the majority of applications.</span></span> <span data-ttu-id="9d4c1-119">Obwohl wir davon ausgehen, dass die meisten Anwendungen eine bessere Erfahrung unter Windows 7 als Folge dieser Änderungen haben, kann eine kleine Teilmenge der Anwendungen negativ beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-119">While we expect most applications to have a better experience on Windows 7 as a result of these changes, a small subset of applications may be negatively affected.</span></span> <span data-ttu-id="9d4c1-120">Die Anwendungskompatibilitätsebenen des Systems lösen Setupprobleme automatisch, indem sie der Anwendung immer mitzuteilen, dass es erfolgreich war, eine Einstellung zu ändern, auch wenn sie aufgrund einer geschützten Ressource nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-120">The system's application compatibility layers will automatically resolve setup problems by always telling the application that it succeeded in changing a setting, even if it failed due to it being a protected resource.</span></span> <span data-ttu-id="9d4c1-121">Dadurch wird verhindert, dass Anwendungssetups nicht funktionieren. Dies kann jedoch zu Problemen führen, wenn die Einstellung geändert werden muss, damit die Anwendung ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-121">This prevents application setups from breaking but may cause problems if the setting needed to be changed in order for the application to function properly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="9d4c1-122">Manifestation</span><span class="sxs-lookup"><span data-stu-id="9d4c1-122">Manifestation</span></span>

<span data-ttu-id="9d4c1-123">Anwendungen haben diese Einstellungen möglicherweise vor Windows 7 geändert.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-123">Applications may have modified these settings prior to Windows 7.</span></span> <span data-ttu-id="9d4c1-124">Nach der Installation unter Windows 7 können Anwendungen feststellen, dass bestimmte Features nicht mehr funktionieren, da die Einstellungen nicht den Erwartungen der Anwendung entsprechen.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-124">Upon installing on Windows 7, applications may find certain features no longer work because the settings did not reflect what the application expected.</span></span>

<span data-ttu-id="9d4c1-125">Es gibt zwei Szenarien, in denen Anwendungen probleme im Zusammenhang mit diesem hinzugefügten Schutz auftreten können:</span><span class="sxs-lookup"><span data-stu-id="9d4c1-125">There are two scenarios in which applications may encounter problems related to this added protection:</span></span>

-   <span data-ttu-id="9d4c1-126">Anwendungen, die die jetzt geschützten Einstellungen möglicherweise als Datenspeicher oder als seltenen oder unbeabsichtigten Erweiterungspunkt verwendet haben</span><span class="sxs-lookup"><span data-stu-id="9d4c1-126">Applications that may have been using the now-protected settings as a data store or as a rare or unintended extensibility point</span></span>
-   <span data-ttu-id="9d4c1-127">In seltenen Fällen erkennt der Erkennungsmechanismus, der zum Identifizieren von Anwendungssetups verwendet wird, möglicherweise kein bestimmtes Setup, sodass die Entschärfungsebene für die Anwendungskompatibilität möglicherweise nicht angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-127">In rare cases, the detection mechanism used to identify application setups may not recognize a particular setup and so the application compatibility mitigation layer may not be applied</span></span>

## <a name="mitigation"></a><span data-ttu-id="9d4c1-128">Minderung</span><span class="sxs-lookup"><span data-stu-id="9d4c1-128">Mitigation</span></span>

<span data-ttu-id="9d4c1-129">Die primäre Möglichkeit zur Risikominderung ist die Anwendungskompatibilitätsebene des Systems, die bei Erkennung automatisch auf Anwendungssetups angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-129">The primary means of mitigation is the system's application compatibility layer, which is automatically applied to application setups when detected.</span></span> <span data-ttu-id="9d4c1-130">Sie können sie auch manuell auf jede Anwendung anwenden, indem Sie die Registerkarte Kompatibilität in den Eigenschaften der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-130">You can also manually apply it to any application using the compatibility tab in the application's properties.</span></span>

<span data-ttu-id="9d4c1-131">Diese Ebene löst das Problem, indem Registrierungsvorgänge abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-131">This layer resolves the problem by intercepting registry operations.</span></span> <span data-ttu-id="9d4c1-132">Für den Fall, dass die Anwendung versucht hat, eine schreibgeschützte Einstellung (WRP) zu ändern, gibt die Ebene immer erfolglos zurück, obwohl die Einstellung nicht wirklich geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-132">In the case where the application was attempting to modify a read-only (WRP) setting, the layer always returns success, even though the setting was not really changed.</span></span> <span data-ttu-id="9d4c1-133">Für die meisten Anwendungen führt dies zu keinen Problemen.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-133">For most applications, this will cause no problems.</span></span> <span data-ttu-id="9d4c1-134">Es besteht jedoch die Möglichkeit, dass die Anwendung diese Einstellung benötigt, um ordnungsgemäß zu funktionieren. Dies ist das erste oben beschriebene Szenario.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-134">However, there is a possibility that the application needed that setting changed in order to function properly, which is the first scenario described above.</span></span>

## <a name="solution"></a><span data-ttu-id="9d4c1-135">Lösung</span><span class="sxs-lookup"><span data-stu-id="9d4c1-135">Solution</span></span>

<span data-ttu-id="9d4c1-136">Für die beiden oben genannten Szenarien:</span><span class="sxs-lookup"><span data-stu-id="9d4c1-136">For the two scenarios identified above:</span></span>

-   <span data-ttu-id="9d4c1-137">Wenn die Anwendung erfordert, dass der Schlüssel beschreibbar ist, um den Datenspeicher zu verwenden oder zu verwenden, gibt es keine andere Lösung als das Ändern der Anwendung, sodass sie nicht mehr an diesen Speicherort schreibt.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-137">If the application requires the key to be writable in order to function or use the data store, there is no solution other than changing the application so that it no longer writes to that location.</span></span>
-   <span data-ttu-id="9d4c1-138">Wenn die Kompatibilitätsschicht nicht auf ein Setup angewendet wurde, sollte der Setupfehler erkannt und angeboten werden, angewendet und erneut ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-138">If the compatibility layer was not applied to a setup, the setup failure should be detected and offered to be applied and re-run.</span></span> <span data-ttu-id="9d4c1-139">Anwendungen können auch im Kompatibilitätsmodus ausgeführt werden. In diesem Fall wird immer die Entschärfungsebene angewendet.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-139">Applications can also run in compatibility mode, in which case the mitigation layer is always applied.</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="9d4c1-140">Kompatibilitätstests</span><span class="sxs-lookup"><span data-stu-id="9d4c1-140">Compatibility Tests</span></span>

<span data-ttu-id="9d4c1-141">Ermitteln, ob auf eine Anwendung wrp-Entschärfung angewendet wurde:</span><span class="sxs-lookup"><span data-stu-id="9d4c1-141">How to detect if an application had WRP mitigation applied to it:</span></span>

-   <span data-ttu-id="9d4c1-142">Windows Installer ist WRP bekannt. Es ignoriert automatisch und automatisch Versuche, eine geschützte Ressource zu schreiben oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-142">Windows Installer is aware of WRP; it automatically and silently ignores attempts to write or modify a protected resource.</span></span> <span data-ttu-id="9d4c1-143">Wenn die Anwendung mit Windows Installer und die Protokollierung aktiviert wurde, wird für jeden Schreibvorgang des Registrierungsschlüssels eine Warnung protokolliert, die ignoriert wurde, da es sich um eine WRP-geschützte Ressource gab.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-143">If the application was installed with Windows Installer and logging was enabled, then a warning will be logged for each registry key write operation that was ignored due to its being a WRP-protected resource.</span></span>
-   <span data-ttu-id="9d4c1-144">Die WRP-API enthält SfCIsKeyProtected, das abfragen kann, ob ein Registrierungsschlüssel auf dem aktuellen System WRP-geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-144">The WRP API incorporates SfCIsKeyProtected, which can query if a registry key is WRP-protected on the current system.</span></span> <span data-ttu-id="9d4c1-145">Weitere Informationen zur Verwendung dieser API finden Sie unter dem WRP-Eintrag in MSDN unter den folgenden Links.</span><span class="sxs-lookup"><span data-stu-id="9d4c1-145">See the WRP entry in MSDN in the links below for additional information on using this API.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="9d4c1-146">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9d4c1-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="9d4c1-147">Windows-Ressourcenschutz</span><span class="sxs-lookup"><span data-stu-id="9d4c1-147">Windows Resource Protection</span></span>](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
