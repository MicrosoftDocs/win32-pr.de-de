---
title: Antischadsoftware-Frühstart
description: Antischadsoftware-Frühstart
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c3e51d7fb009ffa0e85a59990b321fb38ad196
ms.sourcegitcommit: a93d3abaf4d6d45a6f0b87faed3f576b222b1745
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104050650"
---
# <a name="early-launch-antimalware"></a><span data-ttu-id="f6049-103">Antischadsoftware-Frühstart</span><span class="sxs-lookup"><span data-stu-id="f6049-103">Early launch antimalware</span></span>

## <a name="platforms"></a><span data-ttu-id="f6049-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="f6049-104">Platforms</span></span>

 <span data-ttu-id="f6049-105">**Clients** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="f6049-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="f6049-106">**Server** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f6049-106">**Servers** - Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="f6049-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6049-107">Description</span></span>

<span data-ttu-id="f6049-108">Da Antischadsoftware (am) bei der Erkennung von Lauf Zeit Schadsoftware besser und besser geeignet ist, sind Angreifer auch besser in der Erstellung von Rootkits, die von der Erkennung ausblenden können.</span><span class="sxs-lookup"><span data-stu-id="f6049-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="f6049-109">Das Erkennen von Schadsoftware, die früh im Start Zyklen gestartet wird, ist eine Herausforderung, die die meisten Anbieter sorgfältig beantworten.</span><span class="sxs-lookup"><span data-stu-id="f6049-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="f6049-110">In der Regel erstellen Sie System-Hacks, die vom Host Betriebssystem nicht unterstützt werden, und können dazu führen, dass der Computer in einen instabilen Zustand versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f6049-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="f6049-111">Bis zu diesem Punkt hat Windows keine gute Möglichkeit bereitgestellt, diese frühen Start Bedrohungen zu erkennen und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f6049-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span>

<span data-ttu-id="f6049-112">Windows 8 führt ein neues Feature mit dem Namen "sicherer Start" ein, das die Windows-Startkonfiguration und-Komponenten schützt und einen Early Launch Anti-Malware-Treiber (Elam) lädt.</span><span class="sxs-lookup"><span data-stu-id="f6049-112">Windows 8 introduces a new feature called Secure Boot, which protects the Windows boot configuration and components, and loads an Early Launch Anti-malware (ELAM) driver.</span></span> <span data-ttu-id="f6049-113">Dieser Treiber startet vor anderen Start Start Treibern und ermöglicht die Auswertung dieser Treiber und unterstützt den Windows-Kernel bei der Entscheidung, ob Sie initialisiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f6049-113">This driver starts before other boot-start drivers and enables the evaluation of those drivers and helps the Windows kernel decide whether they should be initialized.</span></span>

## <a name="manifestation"></a><span data-ttu-id="f6049-114">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="f6049-114">Manifestation</span></span>

<span data-ttu-id="f6049-115">Da Elam zuerst durch den Kernel gestartet wird, wird er vor allen Drittanbieter Software gestartet und kann daher im Startprozess Schadsoftware erkennen und die Initialisierung verhindern.</span><span class="sxs-lookup"><span data-stu-id="f6049-115">By being launched first by the kernel, ELAM is ensured to be launched before any third-party software, and is therefore able to detect malware in the boot process and prevent it from initializing.</span></span>

## <a name="mitigation"></a><span data-ttu-id="f6049-116">Minderung</span><span class="sxs-lookup"><span data-stu-id="f6049-116">Mitigation</span></span>

<span data-ttu-id="f6049-117">Start Treiber werden basierend auf der Klassifizierung initialisiert, die vom Elam-Treiber gemäß einer Initialisierungs Richtlinie zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f6049-117">Boot drivers are initialized based on the classification that is returned from the ELAM driver according to an initialization policy.</span></span> <span data-ttu-id="f6049-118">Standardmäßig initialisiert die Richtlinie bekannte, gute und unbekannte Treiber, initialisiert jedoch keine bekannten fehlerhaften Treiber.</span><span class="sxs-lookup"><span data-stu-id="f6049-118">By default, the policy initializes known good and unknown drivers, but will not initialize known bad drivers.</span></span> <span data-ttu-id="f6049-119">Ein Systemadministrator kann über Gruppenrichtlinie eine benutzerdefinierte Richtlinie angeben, die verhindern kann, dass unbekannte Treiber initialisiert werden, oder Treiber, die für den Startprozess wichtig sind, aber manipuliert wurden, damit der Start initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="f6049-119">A system administrator can specify a custom policy through Group Policy that can prevent unknown drivers from initializing or can enable drivers that are critical to the boot process, but have been tampered with, boot to be initialized.</span></span>

## <a name="solution"></a><span data-ttu-id="f6049-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="f6049-120">Solution</span></span>

<span data-ttu-id="f6049-121">Ein Elam-Treiber muss sich für Kernel Rückrufe registrieren, um beim Initialisieren Informationen zu den einzelnen Start Start Treibern zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f6049-121">An ELAM driver must register for kernel callbacks to get info about each boot-start driver as it is initializing.</span></span> <span data-ttu-id="f6049-122">Der Elam-Treiber kann dann für jeden Treiber eine Klassifizierung zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f6049-122">The ELAM driver can then return a classification for each driver.</span></span> <span data-ttu-id="f6049-123">Diese Funktionen sind erforderlich:</span><span class="sxs-lookup"><span data-stu-id="f6049-123">These functions are required:</span></span>

-   [<span data-ttu-id="f6049-124">Ioregisterbootdrivercallback</span><span class="sxs-lookup"><span data-stu-id="f6049-124">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="f6049-125">Iounregisterbootdrivercallback</span><span class="sxs-lookup"><span data-stu-id="f6049-125">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

<span data-ttu-id="f6049-126">Ein Elam-Treiber kann auch für Registrierungs Rückrufe registriert werden.</span><span class="sxs-lookup"><span data-stu-id="f6049-126">An ELAM driver can also register for registry callbacks.</span></span> <span data-ttu-id="f6049-127">Dies ermöglicht es dem Elam-Treiber, die Konfigurationsdaten zu überprüfen, die von jedem Start Treiber verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6049-127">Doing so enables the ELAM driver to inspect the configuration data that is used by each boot-start driver.</span></span> <span data-ttu-id="f6049-128">Der Elam-Treiber kann die Daten dann blockieren oder ändern, bevor Sie von den Start-Start Treibern verwendet werden, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f6049-128">The ELAM driver can then block or modify the data before it is used by the boot-start drivers, if necessary.</span></span> <span data-ttu-id="f6049-129">Diese Funktionen sind erforderlich:</span><span class="sxs-lookup"><span data-stu-id="f6049-129">These functions are required:</span></span>

-   [<span data-ttu-id="f6049-130">Cmregistercallbackex</span><span class="sxs-lookup"><span data-stu-id="f6049-130">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="f6049-131">Cmunregistercallback</span><span class="sxs-lookup"><span data-stu-id="f6049-131">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

<span data-ttu-id="f6049-132">Weitere Informationen zu den Elam-Treiber Anforderungen und zur API-Verwendung finden Sie unter [Antischadsoftware-Frühstart](/windows-hardware/drivers/install/early-launch-antimalware).</span><span class="sxs-lookup"><span data-stu-id="f6049-132">For more details about ELAM driver requirements and API usage, see [Early Launch Antimalware](/windows-hardware/drivers/install/early-launch-antimalware).</span></span>

## <a name="tests"></a><span data-ttu-id="f6049-133">Tests</span><span class="sxs-lookup"><span data-stu-id="f6049-133">Tests</span></span>

<span data-ttu-id="f6049-134">Elam-Treiber müssen von Microsoft speziell signiert werden, um sicherzustellen, dass Sie früh im Startprozess vom Windows-Kernel gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="f6049-134">ELAM drivers must be specially signed by Microsoft to ensure they are started by the Windows kernel early in the boot process.</span></span> <span data-ttu-id="f6049-135">Zum erhalten der Signatur müssen Elam-Treiber eine Reihe von Zertifizierungstests durchlaufen, um Leistung und anderes Verhalten zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f6049-135">To get the signature, ELAM drivers must pass a set of certification tests to verify performance and other behavior.</span></span> <span data-ttu-id="f6049-136">Diese Tests sind im Windows-hardwarezertifizierungskit enthalten.</span><span class="sxs-lookup"><span data-stu-id="f6049-136">These tests are included in the Windows Hardware Certification Kit.</span></span>

## <a name="resources"></a><span data-ttu-id="f6049-137">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f6049-137">Resources</span></span>

-   [<span data-ttu-id="f6049-138">Antischadsoftware-Frühstart</span><span class="sxs-lookup"><span data-stu-id="f6049-138">Early Launch Antimalware</span></span>](/windows-hardware/drivers/install/early-launch-antimalware)
-   [<span data-ttu-id="f6049-139">Cmregistercallbackex</span><span class="sxs-lookup"><span data-stu-id="f6049-139">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="f6049-140">Cmunregistercallback</span><span class="sxs-lookup"><span data-stu-id="f6049-140">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [<span data-ttu-id="f6049-141">Ioregisterbootdrivercallback</span><span class="sxs-lookup"><span data-stu-id="f6049-141">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="f6049-142">Iounregisterbootdrivercallback</span><span class="sxs-lookup"><span data-stu-id="f6049-142">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [<span data-ttu-id="f6049-143">Zertifizierung von Hardware mit der Windows-Hardware Zertifizierung Build Conference Presentation</span><span class="sxs-lookup"><span data-stu-id="f6049-143">Certifying hardware with the Windows Hardware Certification Kit Build Conference presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [<span data-ttu-id="f6049-144">Herunterladen von Kits und Tools</span><span class="sxs-lookup"><span data-stu-id="f6049-144">Download Kits and Tools</span></span>](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
