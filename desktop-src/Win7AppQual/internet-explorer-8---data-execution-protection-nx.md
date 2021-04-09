---
description: .
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: Internet Explorer 8-Datenausführungsschutz/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bf23ba40be518e3d4c1421012e6b46fdb7b5e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865975"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a><span data-ttu-id="302c1-103">Internet Explorer 8-Datenausführungsschutz/NX</span><span class="sxs-lookup"><span data-stu-id="302c1-103">Internet Explorer 8 - Data Execution Protection/NX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="302c1-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="302c1-104">Affected Platforms</span></span>

 <span data-ttu-id="302c1-105">**Clients** -Windows XP \| Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="302c1-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="302c1-106">**Server** -Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="302c1-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










> [!Note]  
> <span data-ttu-id="302c1-107">Internet Explorer 8 aktiviert den DEP/NX-Schutz, wenn er unter einem Betriebssystem mit der neuesten Service Pack ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="302c1-107">Internet Explorer 8 will enable DEP/NX protection when run on an operating system with the latest service pack.</span></span> <span data-ttu-id="302c1-108">Für Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 und Windows Server 2008 ist DEP/NX in Internet Explorer 8 standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="302c1-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1, and Windows Server 2008 all have DEP/NX enabled by default in Internet Explorer 8.</span></span>

 

## <a name="feature-impact"></a><span data-ttu-id="302c1-109">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="302c1-109">Feature Impact</span></span>

<span data-ttu-id="302c1-110">**Schweregrad** -Mittel</span><span class="sxs-lookup"><span data-stu-id="302c1-110">**Severity** - Medium</span></span>  
<span data-ttu-id="302c1-111">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="302c1-111">**Frequency** - Low</span></span>  

> [!Note]  
> <span data-ttu-id="302c1-112">In der Regel stürzt jede Anwendung, die in Internet Explorer ausgeführt wird und nicht mit DEP/NX kompatibel ist, beim Start ab und funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="302c1-112">Typically, any application that runs in Internet Explorer and is not compatible with DEP/NX will crash on startup and will not function.</span></span> <span data-ttu-id="302c1-113">Internet Explorer stürzt beim Starten ab, wenn Add-ons, die nicht mit DEP/NX kompatibel sind, installiert sind.</span><span class="sxs-lookup"><span data-stu-id="302c1-113">Internet Explorer may crash on startup if add-ons that are not compatible with DEP/NX are installed.</span></span>

 

## <a name="description"></a><span data-ttu-id="302c1-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="302c1-114">Description</span></span>

<span data-ttu-id="302c1-115">DEP/NX ist ein Sicherheits Feature, mit dem speicherbezogene Sicherheitsrisiken verringert werden können.</span><span class="sxs-lookup"><span data-stu-id="302c1-115">DEP/NX is a security feature that helps mitigate memory-related vulnerabilities.</span></span> <span data-ttu-id="302c1-116">Ab Internet Explorer 8 aktivieren alle Internet Explorer-Prozesse die DEP/NX-Funktion standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="302c1-116">As of Internet Explorer 8, all Internet Explorer processes enable the DEP/NX feature by default.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="302c1-117">Erscheinung der Auswirkung</span><span class="sxs-lookup"><span data-stu-id="302c1-117">Manifestation of Impact</span></span>

<span data-ttu-id="302c1-118">Der Windows-Kernel überwacht die Ausführung eines Programms.</span><span class="sxs-lookup"><span data-stu-id="302c1-118">The Windows Kernel monitors a program's execution.</span></span> <span data-ttu-id="302c1-119">Wenn der Kernel einen Versuch erkennt, Code auf einer Speicherseite auszuführen, der nicht als ausführbare Datei gekennzeichnet ist, stoppt der Kernel die Ausführung des Programms, was zu einem Absturz führt.</span><span class="sxs-lookup"><span data-stu-id="302c1-119">If the Kernel detects an attempt to run code from a memory page that is not marked executable, the Kernel halts execution of the program, resulting in a "crash."</span></span> <span data-ttu-id="302c1-120">Dies ist eine Sicherheitsmaßnahme, mit der sichergestellt wird, dass speicherbezogene Sicherheitsrisiken (z. b. Pufferüberläufe) in der Anwendung nicht ausgenutzt werden können, um beliebigen Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="302c1-120">This is a security measure to help ensure that memory-related vulnerabilities (for example, buffer overflows) in the application cannot be exploited in order to execute arbitrary code.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="302c1-121">End-User Entschärfung</span><span class="sxs-lookup"><span data-stu-id="302c1-121">End-User Mitigation</span></span>

-   <span data-ttu-id="302c1-122">Installieren Sie eine neuere Version des Add-on oder Frameworks, das mit DEP/NX kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="302c1-122">Install a later version of the add-on or framework that is DEP/NX compatible.</span></span>
-   <span data-ttu-id="302c1-123">Führen Sie Internet Explorer mit erhöhten Rechten als Administrator aus, und deaktivieren Sie DEP/NX mithilfe des Kontrollkästchens **Speicherschutz aktivieren, um Online Angriffe zu** minimieren auf der Registerkarte "Erweiterte **Internet Optionen**"  /   .</span><span class="sxs-lookup"><span data-stu-id="302c1-123">Run Internet Explorer elevated as Administrator, and then disable DEP/NX using the **Enable memory protection to help mitigate online attacks** check box on the **Internet Options** / **Advanced** tab.</span></span>

## <a name="developer-solution"></a><span data-ttu-id="302c1-124">Entwickler Lösung</span><span class="sxs-lookup"><span data-stu-id="302c1-124">Developer Solution</span></span>

<span data-ttu-id="302c1-125">Kompilieren Sie Anwendungen mithilfe der neuesten Versionen von Frameworks, die mit DEP kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="302c1-125">Compile applications by using the latest versions of frameworks that are DEP compatible.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="302c1-126">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="302c1-126">Leveraging Feature Capabilities</span></span>

-   <span data-ttu-id="302c1-127">Verwenden der/NXCOMPAT-Linkeroption zum Angeben der DEP/NX-Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="302c1-127">Use the /NXCOMPAT linker option to indicate DEP/NX compatibility</span></span>
-   <span data-ttu-id="302c1-128">Wählen Sie Ihren Code in andere verfügbare Schutzmaßnahmen wie Stack Defense (/GS), sichere Ausnahmebehandlung (/SAFESEH) und ASLR (/DynamicBase) aus.</span><span class="sxs-lookup"><span data-stu-id="302c1-128">Opt your code into other available defenses like stack defense (/GS), safe exception handling (/SafeSEH), and ASLR (/DynamicBase)</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="302c1-129">Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit</span><span class="sxs-lookup"><span data-stu-id="302c1-129">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="302c1-130">Testen Sie Ihren Code mit DEP/NX, der mithilfe der neuesten Version von Internet Explorer unter Windows Vista SP1 oder höher aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="302c1-130">Test your code with DEP/NX enabled by using latest released Internet Explorer version on Windows Vista SP1 or later.</span></span>
-   <span data-ttu-id="302c1-131">Testen Sie mit Internet Explorer 7 unter Windows Vista nach dem Aktivieren der DEP/NX-Option.</span><span class="sxs-lookup"><span data-stu-id="302c1-131">Test with Internet Explorer 7 on Windows Vista after enabling the DEP/NX option.</span></span> <span data-ttu-id="302c1-132">Um DEP/NX für Internet Explorer 7 zu aktivieren, führen Sie Internet Explorer als Administrator aus, und legen Sie dann das entsprechende Kontrollkästchen auf der Registerkarte Extras > Internet Optionen > erweitert fest.</span><span class="sxs-lookup"><span data-stu-id="302c1-132">To enable DEP/NX for Internet Explorer 7, run Internet Explorer as an administrator, then set the appropriate check box in the Tools > Internet Options > Advanced tab.</span></span>
-   <span data-ttu-id="302c1-133">Führen Sie das Internet Explorer Compatibility Test Tool (iectt) aus, das mit dem Anwendungskompatibilitäts-Toolkit (Act) bereitgestellt wird, um mögliche Probleme aufgrund von DEP/NX-Änderungen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="302c1-133">Run the Internet Explorer Compatibility Test Tool (IECTT), provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to the DEP/NX changes.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="302c1-134">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="302c1-134">Links to Other Resources</span></span>

-   [<span data-ttu-id="302c1-135">Internet Explorer 8 Sicherheitsteil I: DEP/NX-Speicherschutz</span><span class="sxs-lookup"><span data-stu-id="302c1-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="302c1-136">Datenausführungsverhinderung</span><span class="sxs-lookup"><span data-stu-id="302c1-136">Data Execution Prevention</span></span>](../memory/data-execution-prevention.md)
-   [<span data-ttu-id="302c1-137">Neue NX-APIs, die zu Windows Vista SP1, Windows XP SP3 und Windows Server 2008 R2 hinzugefügt wurden</span><span class="sxs-lookup"><span data-stu-id="302c1-137">New NX APIs added to Windows Vista SP1, Windows XP SP3 and Windows Server 2008 R2</span></span>](/archive/blogs/michael_howard/)
-   [<span data-ttu-id="302c1-138">Anwendungskompatibilitäts-Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="302c1-138">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="302c1-139">[Bekannte Probleme mit der Internet Explorer-Sicherheitsfunktion](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="302c1-139">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
