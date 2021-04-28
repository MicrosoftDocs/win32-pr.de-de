---
description: 'Internet Explorer 8: Schutz der Datenausführung/NX'
ms.assetid: 56a4889c-5dcf-416f-b46e-5c48277d5636
title: 'Internet Explorer 8: Schutz der Datenausführung/NX'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0208cc20e78c30f42b09af78460990be20b002
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088248"
---
# <a name="internet-explorer-8---data-execution-protectionnx"></a><span data-ttu-id="4b6c5-103">Internet Explorer 8: Schutz der Datenausführung/NX</span><span class="sxs-lookup"><span data-stu-id="4b6c5-103">Internet Explorer 8 - Data Execution Protection/NX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4b6c5-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="4b6c5-104">Affected Platforms</span></span>

 <span data-ttu-id="4b6c5-105">**Clients:** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="4b6c5-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="4b6c5-106">**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4b6c5-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  










> [!Note]  
> <span data-ttu-id="4b6c5-107">Internet Explorer 8 aktiviert den DEP-/NX-Schutz, wenn er auf einem Betriebssystem mit dem neuesten Service Pack ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-107">Internet Explorer 8 will enable DEP/NX protection when run on an operating system with the latest service pack.</span></span> <span data-ttu-id="4b6c5-108">Für Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1 und Windows Server 2008 ist DEP/NX standardmäßig in Internet Explorer 8 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-108">Windows XP SP3, Windows Server 2003 SP3, Windows Vista SP1, and Windows Server 2008 all have DEP/NX enabled by default in Internet Explorer 8.</span></span>

 

## <a name="feature-impact"></a><span data-ttu-id="4b6c5-109">Auswirkungen auf Features</span><span class="sxs-lookup"><span data-stu-id="4b6c5-109">Feature Impact</span></span>

<span data-ttu-id="4b6c5-110">**Schweregrad –** Mittel</span><span class="sxs-lookup"><span data-stu-id="4b6c5-110">**Severity** - Medium</span></span>  
<span data-ttu-id="4b6c5-111">**Häufigkeit** : Niedrig</span><span class="sxs-lookup"><span data-stu-id="4b6c5-111">**Frequency** - Low</span></span>  

> [!Note]  
> <span data-ttu-id="4b6c5-112">In der Regel stürzt jede Anwendung, die in Internet Explorer ausgeführt wird und nicht mit DEP/NX kompatibel ist, beim Start ab und funktioniert nicht.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-112">Typically, any application that runs in Internet Explorer and is not compatible with DEP/NX will crash on startup and will not function.</span></span> <span data-ttu-id="4b6c5-113">Internet Explorer können beim Start abstürzen, wenn Add-Ons installiert sind, die nicht mit DEP/NX kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-113">Internet Explorer may crash on startup if add-ons that are not compatible with DEP/NX are installed.</span></span>

 

## <a name="description"></a><span data-ttu-id="4b6c5-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b6c5-114">Description</span></span>

<span data-ttu-id="4b6c5-115">DEP/NX ist ein Sicherheitsfeature, mit dem speicherbezogene Sicherheitsrisiken entschärft werden können.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-115">DEP/NX is a security feature that helps mitigate memory-related vulnerabilities.</span></span> <span data-ttu-id="4b6c5-116">Ab Internet Explorer 8 aktivieren alle Internet Explorer Prozesse standardmäßig das DEP/NX-Feature.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-116">As of Internet Explorer 8, all Internet Explorer processes enable the DEP/NX feature by default.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="4b6c5-117">Wirkungserz weiter</span><span class="sxs-lookup"><span data-stu-id="4b6c5-117">Manifestation of Impact</span></span>

<span data-ttu-id="4b6c5-118">Der Windows-Kernel überwacht die Ausführung eines Programms.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-118">The Windows Kernel monitors a program's execution.</span></span> <span data-ttu-id="4b6c5-119">Wenn der Kernel einen Versuch erkennt, Code von einer Speicherseite auszuführen, die nicht als ausführbare Datei gekennzeichnet ist, hält der Kernel die Ausführung des Programms an, was zu einem "Absturz" führt.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-119">If the Kernel detects an attempt to run code from a memory page that is not marked executable, the Kernel halts execution of the program, resulting in a "crash."</span></span> <span data-ttu-id="4b6c5-120">Dies ist eine Sicherheitsmaßnahme, um sicherzustellen, dass speicherbezogene Sicherheitsrisiken (z. B. Pufferüberläufe) in der Anwendung nicht ausgenutzt werden können, um beliebigen Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-120">This is a security measure to help ensure that memory-related vulnerabilities (for example, buffer overflows) in the application cannot be exploited in order to execute arbitrary code.</span></span>

## <a name="end-user-mitigation"></a><span data-ttu-id="4b6c5-121">End-User Entschärfung</span><span class="sxs-lookup"><span data-stu-id="4b6c5-121">End-User Mitigation</span></span>

-   <span data-ttu-id="4b6c5-122">Installieren Sie eine neuere Version des Add-Ons oder Frameworks, die MIT DEP/NX kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-122">Install a later version of the add-on or framework that is DEP/NX compatible.</span></span>
-   <span data-ttu-id="4b6c5-123">Führen Internet Explorer mit erhöhten Rechten als Administrator aus, und deaktivieren Sie dann DEP/NX mithilfe des **Kontrollkästchens** Speicherschutz aktivieren, um Onlineangriffe zu minimieren auf der Registerkarte **Internetoptionen**  /  **Erweitert.**</span><span class="sxs-lookup"><span data-stu-id="4b6c5-123">Run Internet Explorer elevated as Administrator, and then disable DEP/NX using the **Enable memory protection to help mitigate online attacks** check box on the **Internet Options** / **Advanced** tab.</span></span>

## <a name="developer-solution"></a><span data-ttu-id="4b6c5-124">Entwicklerlösung</span><span class="sxs-lookup"><span data-stu-id="4b6c5-124">Developer Solution</span></span>

<span data-ttu-id="4b6c5-125">Kompilieren Sie Anwendungen mithilfe der neuesten Versionen von Frameworks, die DEP-kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-125">Compile applications by using the latest versions of frameworks that are DEP compatible.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="4b6c5-126">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="4b6c5-126">Leveraging Feature Capabilities</span></span>

-   <span data-ttu-id="4b6c5-127">Verwenden Sie die /NXCOMPAT-Linkeroption, um die DEP/NX-Kompatibilität anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-127">Use the /NXCOMPAT linker option to indicate DEP/NX compatibility</span></span>
-   <span data-ttu-id="4b6c5-128">Verwenden Sie Ihren Code für andere verfügbare Verteidigungen wie Stapelschutz (/GS), sichere Ausnahmebehandlung (/SafeSEH) und ASLR (/DynamicBase).</span><span class="sxs-lookup"><span data-stu-id="4b6c5-128">Opt your code into other available defenses like stack defense (/GS), safe exception handling (/SafeSEH), and ASLR (/DynamicBase)</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="4b6c5-129">Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Nutzbarkeitstests</span><span class="sxs-lookup"><span data-stu-id="4b6c5-129">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="4b6c5-130">Testen Sie Ihren Code mit aktivierter DEP/NX-Internet Explorer version unter Windows Vista SP1 oder höher.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-130">Test your code with DEP/NX enabled by using latest released Internet Explorer version on Windows Vista SP1 or later.</span></span>
-   <span data-ttu-id="4b6c5-131">Testen Sie Internet Explorer 7 unter Windows Vista, nachdem Sie die DEP/NX-Option aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-131">Test with Internet Explorer 7 on Windows Vista after enabling the DEP/NX option.</span></span> <span data-ttu-id="4b6c5-132">Um DEP/NX für Internet Explorer 7 zu aktivieren, führen Sie Internet Explorer als Administrator aus, und aktivieren Sie dann das entsprechende Kontrollkästchen auf der Registerkarte Extras > Internetoptionen > Erweitert.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-132">To enable DEP/NX for Internet Explorer 7, run Internet Explorer as an administrator, then set the appropriate check box in the Tools > Internet Options > Advanced tab.</span></span>
-   <span data-ttu-id="4b6c5-133">Führen Sie das Internet Explorer Compatibility Test Tool (IECTT) aus, das mit dem Application Compatibility Toolkit (ACT) bereitgestellt wird, um mögliche Probleme aufgrund der DEP/NX-Änderungen zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="4b6c5-133">Run the Internet Explorer Compatibility Test Tool (IECTT), provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to the DEP/NX changes.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="4b6c5-134">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4b6c5-134">Links to Other Resources</span></span>

-   [<span data-ttu-id="4b6c5-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span><span class="sxs-lookup"><span data-stu-id="4b6c5-135">Internet Explorer 8 Security Part I: DEP/NX Memory Protection</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="4b6c5-136">Datenausführungsverhinderung</span><span class="sxs-lookup"><span data-stu-id="4b6c5-136">Data Execution Prevention</span></span>](../memory/data-execution-prevention.md)
-   [<span data-ttu-id="4b6c5-137">Neue NX-APIs zu Windows Vista SP1, Windows XP SP3 und Windows Server 2008 R2 hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="4b6c5-137">New NX APIs added to Windows Vista SP1, Windows XP SP3 and Windows Server 2008 R2</span></span>](/archive/blogs/michael_howard/)
-   [<span data-ttu-id="4b6c5-138">Download des Anwendungskompatibilitätstoolkits</span><span class="sxs-lookup"><span data-stu-id="4b6c5-138">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="4b6c5-139">[Bekannte Internet Explorer Sicherheitsfeatures](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4b6c5-139">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
