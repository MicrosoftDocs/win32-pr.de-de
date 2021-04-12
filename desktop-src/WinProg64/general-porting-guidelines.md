---
title: Allgemeine Richtlinien für die Portierung
description: Das Portieren von 32-Bit-Anwendungen auf 64-Bit-Microsoft Windows ist einfacher als das Portieren von 16-Bit-Anwendungen auf 32-Bit-Windows. Die Verschiebung wird jedoch mit einer sorgfältigen Planung reibungslos verlaufen. Im folgenden finden Sie einige allgemeine Richtlinien.
ms.assetid: 28c1656e-93a2-441b-8946-18017e0b2b29
keywords:
- Portieren von 32-Bit-Anwendungen auf eine 64-Bit-Windows 64-Bit-Windows-Programmierung
- 64-Bit-Windows-Programmier Handbuch 64-Bit Windows-Programmierung, Portieren von Richtlinien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31734edd8b85bd61b8b84cb2c66d835f0085ac1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "104218926"
---
# <a name="general-porting-guidelines"></a><span data-ttu-id="fd3fd-107">Allgemeine Richtlinien für die Portierung</span><span class="sxs-lookup"><span data-stu-id="fd3fd-107">General Porting Guidelines</span></span>

<span data-ttu-id="fd3fd-108">Das Portieren von 32-Bit-Anwendungen auf 64-Bit-Microsoft Windows ist einfacher als das Portieren von 16-Bit-Anwendungen auf 32-Bit-Windows.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-108">Porting 32-bit applications to 64-bit Microsoft Windows will be easier than it was porting 16-bit applications to 32-bit Windows.</span></span> <span data-ttu-id="fd3fd-109">Die Verschiebung wird jedoch mit einer sorgfältigen Planung reibungslos verlaufen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-109">However, the move will go more smoothly with some careful planning.</span></span> <span data-ttu-id="fd3fd-110">Im folgenden finden Sie einige allgemeine Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-110">The following are some general guidelines.</span></span>

## <a name="planning"></a><span data-ttu-id="fd3fd-111">Planung</span><span class="sxs-lookup"><span data-stu-id="fd3fd-111">Planning</span></span>

-   <span data-ttu-id="fd3fd-112">Legen Sie die Größe des erforderlichen Aufwands für den Port fest.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-112">Determine the magnitude of the effort required for the port.</span></span> <span data-ttu-id="fd3fd-113">Messen Sie, wie viel Arbeit beteiligt ist, indem Sie die folgenden Elemente identifizieren:</span><span class="sxs-lookup"><span data-stu-id="fd3fd-113">Gauge how much work is involved by identifying the following items:</span></span>
    -   <span data-ttu-id="fd3fd-114">Problem 32-Bit-Code.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-114">Problem 32-bit code.</span></span> <span data-ttu-id="fd3fd-115">Kompilieren Sie Ihren 32-Bit-Code mit dem 64-Bit-Compiler, und untersuchen Sie das Ausmaß der Fehler und Warnungen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-115">Compile your 32-bit code with the 64-bit compiler and examine the extent of the errors and warnings.</span></span>
    -   <span data-ttu-id="fd3fd-116">Freigegebene Komponenten oder Abhängigkeiten.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-116">Shared components or dependencies.</span></span> <span data-ttu-id="fd3fd-117">Bestimmen Sie, welche Komponenten in der Anwendung von anderen Teams stammen und ob diese Teams beabsichtigen, 64-Bit-Versionen Ihres Codes zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-117">Determine which components in your application originate from other teams and whether those teams plan to develop 64-bit versions of their code.</span></span>
    -   <span data-ttu-id="fd3fd-118">Legacy-oder Assemblycode.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-118">Legacy or assembly code.</span></span> <span data-ttu-id="fd3fd-119">Windows-basierte 16-Bit-Anwendungen können nicht auf 64-Bit-Fenstern ausgeführt werden und müssen umgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-119">16-bit Windows-based applications do not run on 64-bit Windows and must be rewritten.</span></span> <span data-ttu-id="fd3fd-120">Während der x86-Assemblycode in WOW64 ausgeführt wird, können Sie diesen Code umschreiben, um die Geschwindigkeit der Intel Itanium-Architektur zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-120">While x86 assembly code runs in WOW64, you may want to rewrite this code to take advantage of the speed of the Intel Itanium architecture.</span></span>
-   <span data-ttu-id="fd3fd-121">Portieren Sie die gesamte Anwendung, nicht nur Teile davon.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-121">Port the entire application, not just portions of it.</span></span>

    <span data-ttu-id="fd3fd-122">Obwohl es möglich ist, Teile einer Anwendung zu portieren oder Code auf 2G mit/LARGEADDRESSAWARE: No einzuschränken, stellt diese Strategie kurzfristigen Aufwand für langfristige Probleme dar.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-122">Although it is possible to port pieces of an application or to limit code to 2G with /LARGEADDRESSAWARE:NO, this strategy trades short-term gain for long-term pain.</span></span>

    > [!Note]  
    > <span data-ttu-id="fd3fd-123">/LARGEADDRESSAWARE: No wird für eine ARM64-Binärdatei ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-123">/LARGEADDRESSAWARE:NO is ignored for an ARM64 binary.</span></span>

     

-   <span data-ttu-id="fd3fd-124">Suchen Sie Ersatz für Technologien, die nicht portiert werden.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-124">Find substitutes for technologies that will not be ported.</span></span>

    <span data-ttu-id="fd3fd-125">Einige Technologien, einschließlich DAO (Datenzugriffs Objekt) und der Jet Red Database Engine, werden nicht in 64-Bit-Windows portiert.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-125">Some technologies, including DAO (Data Access Object) and the Jet Red database engine, will not be ported to 64-bit Windows.</span></span>

-   <span data-ttu-id="fd3fd-126">Behandeln Sie Ihre 64-Bit-Version als separate Produktversion.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-126">Treat your 64-bit version as a separate product release.</span></span>

    <span data-ttu-id="fd3fd-127">Auch wenn Ihr 64-Bit-Produkt die gleiche Codebasis wie Ihr 32-Bit gemeinsam nutzen kann, sind zusätzliche Tests erforderlich, und es können weitere Überlegungen zur Version vorliegen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-127">Even though your 64-bit product may share the same code base as your 32-bit, it needs additional testing and may have other release considerations.</span></span>

## <a name="development"></a><span data-ttu-id="fd3fd-128">Entwicklung</span><span class="sxs-lookup"><span data-stu-id="fd3fd-128">Development</span></span>

-   <span data-ttu-id="fd3fd-129">Beginnen Sie jetzt mit der Entwicklung von kompatibler Code</span><span class="sxs-lookup"><span data-stu-id="fd3fd-129">Start developing compliant code now.</span></span>

    <span data-ttu-id="fd3fd-130">Entwickler können mit dem Schreiben von kompatibler Code beginnen, indem Sie die neuesten Windows-Header Dateien und die neuen Datentypen ohne negative Auswirkungen auf die 32-Bit-Produktentwicklung verwenden.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-130">Developers can start writing compliant code by using the latest Windows header files and the new data types with no adverse effects on 32-bit product development.</span></span> <span data-ttu-id="fd3fd-131">Weitere Informationen finden Sie unter Vorbereiten [für 64-Bit-Windows](getting-ready-for-64-bit-windows.md).</span><span class="sxs-lookup"><span data-stu-id="fd3fd-131">For more information, see [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md).</span></span>

-   <span data-ttu-id="fd3fd-132">Stellen Sie sicher, dass Ihr Code für 32-und 64-Bit-Fenster kompiliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-132">Ensure that your code can be compiled for both 32- and 64-bit Windows.</span></span>

    <span data-ttu-id="fd3fd-133">Das neue Datenmodell war so konzipiert, dass 32-und 64-Bit-Anwendungen aus einer einzelnen Codebasis mit wenigen Änderungen erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-133">The new data model was designed to allow 32- and 64-bit applications to be built from a single code base with few modifications.</span></span> <span data-ttu-id="fd3fd-134">Das SQL Server-und das Windows-Entwicklungsteam entwickeln 32-und 64-Bit-Versionen ihrer Produkte aus der gleichen Codebasis.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-134">The SQL Server and Windows development teams are developing 32- and 64-bit versions of their products from the same code base.</span></span>

-   <span data-ttu-id="fd3fd-135">Verwenden Sie die neuen Optimierungs Features des Compilers, um optimale Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-135">Use the compiler's new optimization features for best performance.</span></span>

    <span data-ttu-id="fd3fd-136">Die Code Optimierung für Intel Itanium-Prozessoren ist wichtiger als bei x86.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-136">Code optimization for Intel Itanium processors is more important than it was for the x86.</span></span> <span data-ttu-id="fd3fd-137">Der Compiler geht von vielen der Optimierungs Funktionen aus, die zuvor vom Mikroprozessor verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-137">The compiler assumes many of the optimization functions previously handled by the microprocessor.</span></span> <span data-ttu-id="fd3fd-138">Sie können die Leistung einer 64-Bit-Anwendung maximieren, indem Sie zwei neue Optimierungs Features des Compilers verwenden: *Profil gesteuerte Optimierung* und *Optimierung des gesamten Programms*.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-138">You can maximize the performance of a 64-bit application by using two new optimization features of the compiler: *Profile Guided Optimization* and *Whole Program Optimization*.</span></span> <span data-ttu-id="fd3fd-139">Beide Features führen zu längeren Buildzeiten und erfordern die frühe Entwicklung von guten Testszenarien.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-139">Both features result in longer build times and require the early development of good test scenarios.</span></span>

    <span data-ttu-id="fd3fd-140">Die *Profil gesteuerte Optimierung* umfasst einen zweistufigen Kompilierungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-140">*Profile Guided Optimization* involves a two-step compile process.</span></span> <span data-ttu-id="fd3fd-141">Während der ersten Kompilierung wird der Code instrumentiert, um das Ausführungs Verhalten aufzuzeichnen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-141">During the first compile, the code is instrumented to capture the execution behavior.</span></span> <span data-ttu-id="fd3fd-142">Diese Informationen werden während der zweiten Kompilierung verwendet, um alle Optimierungs Features zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-142">This information is used during the second compile to guide all optimization features.</span></span>

    <span data-ttu-id="fd3fd-143">Die *Optimierung des gesamten Programms* analysiert den Code in allen Anwendungs Dateien, nicht nur eine einzige.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-143">*Whole Program Optimization* analyzes the code in all application files, not just a single one.</span></span> <span data-ttu-id="fd3fd-144">Diese Vorgehensweise erhöht die Leistung auf verschiedene Weise, z. a. eine bessere Inlining sowie verbesserte Nebeneffekte und benutzerdefinierte Aufruf Konventionen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-144">This approach increases performance in several ways, including better inlining, as well as improved side-effect analysis and custom calling conventions.</span></span>

## <a name="testing"></a><span data-ttu-id="fd3fd-145">Test</span><span class="sxs-lookup"><span data-stu-id="fd3fd-145">Testing</span></span>

-   <span data-ttu-id="fd3fd-146">Bestimmen Sie, ob Sie 64-oder 32-Bit-Code testen, der in WOW64 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-146">Determine whether you'll test 64- or 32-bit code running in WOW64.</span></span>

    <span data-ttu-id="fd3fd-147">Einige Anwendungen enthalten sowohl systemeigenen 64-Bit-Code als auch 32-Bit-Code, der in WOW64 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-147">Some applications include both native 64-bit code and 32-bit code running in WOW64.</span></span> <span data-ttu-id="fd3fd-148">Untersuchen Sie dies sehr gut, während Sie einen Testplan entwickeln, und entscheiden Sie, ob Ihre TestTools 64-Bit, 32-Bit oder eine Kombination sein sollten.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-148">Investigate this closely while developing a test plan, and decide whether your test tools should be 64-bit, 32-bit, or a combination.</span></span> <span data-ttu-id="fd3fd-149">Sie müssen häufig sowohl die 64-als auch die 32-Bit-Version der Anwendung auf 64-Bit-Windows testen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-149">You will often need to test both the 64- and 32-bit versions of your application on 64-bit Windows.</span></span>

-   <span data-ttu-id="fd3fd-150">Testen Sie häufig verwendete 32-Bit-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-150">Test frequently used 32-bit components.</span></span>

    <span data-ttu-id="fd3fd-151">Kompilieren Sie zunächst den Code in 64-Bit neu, und testen Sie.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-151">First, recompile your code to 64-bit and test.</span></span> <span data-ttu-id="fd3fd-152">Zum anderen beheben Sie Probleme, kompilieren Sie in 32 Bits neu, und testen Sie dann.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-152">Second, fix problems, recompile in 32-bits, and then test.</span></span> <span data-ttu-id="fd3fd-153">Als dritte Neukompilierung in 64-Bit und testen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-153">Third, recompile to 64-bit and test.</span></span>

-   <span data-ttu-id="fd3fd-154">Testen Sie die com-und RPC-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-154">Test COM and RPC components.</span></span>

    <span data-ttu-id="fd3fd-155">Stellen Sie sicher, dass die com-und RPC-Komponenten 32-und 64-Bit ordnungsgemäß kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-155">Make sure that both 32- and 64-bit COM and RPC components communicate correctly.</span></span> <span data-ttu-id="fd3fd-156">Sie müssen möglicherweise auch die Kommunikation mit 16-Bit-Komponenten über ein Netzwerk testen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-156">You may also have to test communications with 16-bit components over a network.</span></span>

-   <span data-ttu-id="fd3fd-157">Testen Sie Ihre 32-Bit-Version auf 64-Bit-Fenstern.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-157">Test your 32-bit version on 64-bit Windows.</span></span>

    <span data-ttu-id="fd3fd-158">Kunden können weiterhin 32-Bit-Anwendungen auf 64-Bit-Windows verwenden, bei denen Leistungs-und Arbeitsspeicher Probleme keine wichtigen Aspekte sind.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-158">Customers can continue to use 32-bit applications on 64-bit Windows where performance and memory issues are not major considerations.</span></span>

-   <span data-ttu-id="fd3fd-159">Testen Sie verschiedene Speicherkonfigurationen.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-159">Test different memory configurations.</span></span>

    <span data-ttu-id="fd3fd-160">Wenn Sie große Mengen an Arbeitsspeicher auf dem Server hinzufügen, werden in der Anwendung oder im Betriebssystem manchmal nicht aufmerkte Probleme angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fd3fd-160">Adding large amounts of memory on the server sometimes exposes previously unnoticed problems in either the application or the operating system.</span></span>

 

 




