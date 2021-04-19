---
description: .
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Windows 7-Unterstützung für Intel AVX aktivieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440c71c5fd6aa65b5e56b8dfb0b6eab134418192
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362722"
---
# <a name="enable-windows-7-support-for-intel-avx"></a><span data-ttu-id="eeb5e-103">Windows 7-Unterstützung für Intel AVX aktivieren</span><span class="sxs-lookup"><span data-stu-id="eeb5e-103">Enable Windows 7 Support for Intel AVX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="eeb5e-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="eeb5e-104">Affected Platforms</span></span>

 <span data-ttu-id="eeb5e-105">**Clients** : Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="eeb5e-105">**Clients** - Windows 7 SP1</span></span>  
<span data-ttu-id="eeb5e-106">**Server** -Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="eeb5e-106">**Servers** - Windows Server 2008 R2 SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="eeb5e-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="eeb5e-107">Feature Impact</span></span>

 <span data-ttu-id="eeb5e-108">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="eeb5e-108">**Severity** - Low</span></span>  
<span data-ttu-id="eeb5e-109">**Häufigkeit** -niedrig</span><span class="sxs-lookup"><span data-stu-id="eeb5e-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="eeb5e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eeb5e-110">Description</span></span>

<span data-ttu-id="eeb5e-111">Intel<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="eeb5e-111">Intel<sup>?</sup></span></span> <span data-ttu-id="eeb5e-112">Erweiterte Vektor Erweiterungen (AVX)<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="eeb5e-112">Advanced Vector Extensions (AVX)<sup>?</sup></span></span> <span data-ttu-id="eeb5e-113">ist eine 256-Bit-SIMD-Gleit Komma-Vektor Erweiterung der Intel-Architektur.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-113">is a 256-bit SIMD floating-point vector extension of Intel architecture.</span></span> <span data-ttu-id="eeb5e-114">Sie enthält Erweiterungen für Anweisungs-und Register Sätze.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-114">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="eeb5e-115">Microsoft hat einige API-Erweiterungen entwickelt, wie z. b. xstate-Funktionen, mit denen Anwendungen auf Informationen und den Status erweiterter Prozessor Features zugreifen und diese bearbeiten können (einschließlich AVX).</span><span class="sxs-lookup"><span data-stu-id="eeb5e-115">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including AVX.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="eeb5e-116">Verwendungsszenarien</span><span class="sxs-lookup"><span data-stu-id="eeb5e-116">Usage Scenarios</span></span>

<span data-ttu-id="eeb5e-117">Es gibt drei allgemeine Ebenen der möglichen Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-117">There are three general levels of potential impact.</span></span>

<span data-ttu-id="eeb5e-118">**Ebene 1:** Anwendungen, die Intel AVX nicht direkt verwenden, sehen keinerlei Auswirkung auf ihre Funktionalität, auch wenn Sie Bibliotheken aufzurufen oder Compiler verwenden, die indirekt Intel AVX-Erweiterungen verwenden oder generieren.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-118">**Level 1:** Applications that do not directly use Intel AVX will not see any impact to their functionality even if they call into libraries or use compilers that indirectly use or generate Intel AVX extensions.</span></span> <span data-ttu-id="eeb5e-119">Dies stellt die Mehrzahl der Anwendungen dar.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-119">This represents by far the majority of applications.</span></span>

<span data-ttu-id="eeb5e-120">**Ebene 2:** Erweiterte Anwendungen, die den Intel AVX-Anweisungs Satz explizit verwenden, sind in der Lage, auf AVX-Register Inhalte zuzugreifen und diese zu ändern, wenn eine Hardware Ausnahme ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-120">**Level 2:** Advanced applications that explicitly use the Intel AVX instruction set will be able to access and change AVX register contents when a hardware exception is raised.</span></span> <span data-ttu-id="eeb5e-121">Eine sehr geringe Anzahl von Anwendungen würde in diese Kategorie fallen, da Sie eine intime Kenntnis des Anweisungs Datenstroms impliziert, der zum Zeitpunkt der Ausnahme ausgeführt wird, z. b. Anwendungen mit Abschnitten, die in der Assemblysprache geschrieben wurden, oder solche, die zur Laufzeit Computercode generieren (z. b. Laufzeiten für verwalteten Code mit Just-in-Time-Kompilierung</span><span class="sxs-lookup"><span data-stu-id="eeb5e-121">A very small number of applications would fall into this category, as it implies an intimate knowledge of the instruction stream executing at the time of the exception, such as applications with sections written in assembly language or those that generate machine code at runtime (for example, managed code runtimes with just-in-time compilation).</span></span>

<span data-ttu-id="eeb5e-122">**Ebene 3:** Debugger-Anwendungen können in der Anwendung, die gedebuggt wird, auf den AVX-Zustand zugreifen und ihn bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-122">**Level 3:** Debugger applications will be able to access and manipulate the AVX state in the application being debugged.</span></span>

## <a name="how-to-leverage-feature-capabilities"></a><span data-ttu-id="eeb5e-123">Funktionsweise von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="eeb5e-123">How to Leverage Feature Capabilities</span></span>

<span data-ttu-id="eeb5e-124">**Ebene 1:** Es ist keine Aktion erforderlich, damit Anwendungen Intel AVX verwenden können.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-124">**Level 1:** No action is necessary for applications to use Intel AVX.</span></span>

<span data-ttu-id="eeb5e-125">**Ebene 2:** Anwendungen in dieser Kategorie haben die Möglichkeit, zum Zeitpunkt der Ausnahme innerhalb ihrer Ausnahme Filter auf den AVX-Zustand zuzugreifen und ihn zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-125">**Level 2:** Applications in this category have the option to access and manipulate AVX state at the time of the exception from within their exception filters.</span></span> <span data-ttu-id="eeb5e-126">Nachdem Sie den Basis Prozessor Kontext über GetExceptionInformation erhalten haben, sollten Filter folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="eeb5e-126">After obtaining the base processor context via GetExceptionInformation, filters should:</span></span>

 <span data-ttu-id="eeb5e-127">**1.** überprüfen Sie den Wert des **context- \_ xstate** -Flags.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-127">**1.** Check the value of the **CONTEXT\_XSTATE** flag.</span></span> <span data-ttu-id="eeb5e-128">Dieses Flag gibt an, dass mindestens eine xstate-Funktion im Kontext vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-128">This flag indicates the presence of at least one XState feature in the context.</span></span>  
<span data-ttu-id="eeb5e-129">**2.** wenn dies der Fall ist, können Sie **getxstatefeaturesmask** aufrufen und den Wert des **xstate- \_ AVX** -Flags in der zurückgegebenen Maske testen.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-129">**2.** If this is the case, call **GetXStateFeaturesMask** and test the value of the **XSTATE\_AVX** flag in the returned mask.</span></span> <span data-ttu-id="eeb5e-130">Dies gibt an, dass der AVX-Zustand im Kontext vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-130">This indicates the presence of AVX state in the context.</span></span>  
<span data-ttu-id="eeb5e-131">**3.** rufen Sie **Lo-exstatefeature** auf, um den tatsächlichen Speicherort abzurufen, an dem der AVX-Status gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-131">**3.** Call **LocateXStateFeature** to retrieve the actual location where the AVX state is stored.</span></span>  

<span data-ttu-id="eeb5e-132">**Ebene 3:** Es ist nicht erforderlich, vorhandene Debugger-Anwendungen zu aktualisieren, es sei denn, Sie möchten auf die Intel AVX-Register zugreifen:</span><span class="sxs-lookup"><span data-stu-id="eeb5e-132">**Level 3:** It is not necessary to update existing debugger applications unless they wish access the Intel AVX registers:</span></span>

<span data-ttu-id="eeb5e-133">**1.** um zu ermitteln, ob AVX aktiviert ist, sollte der Debugger Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="eeb5e-133">**1.** To determine if AVX is enabled, the debugger should use:</span></span>

-   <span data-ttu-id="eeb5e-134">Getenabledxstatefeatures, um eine Maske von aktivierten xstate-Features auf x86-oder x64-Prozessoren zu erhalten, um zu bestimmen, welche Features auf dem System vorhanden und aktiviert sind, bevor Sie eine xstate-Prozessor Funktion verwenden oder xstate-Kontexte bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-134">GetEnabledXStateFeatures to get a mask of enabled XState features on x86 or x64 processors to determine what features are present and enabled on the system before using an XState processor feature or attempting to manipulate XState contexts</span></span>

  
<span data-ttu-id="eeb5e-135">**2.** wenn AVX vorhanden ist und Sie den AVX-Zustand von der zu debuggenden Anwendung abrufen und bearbeiten möchten (z. b. GetThreadContext und SetThreadContext), sollte der Debugger Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="eeb5e-135">**2.** If AVX is present and you wish to retrieve and manipulate the AVX state from the application being debugged (for example, GetThreadContext and SetThreadContext), the debugger should use:</span></span>

-   <span data-ttu-id="eeb5e-136">Initializecontext-Funktion zum Initialisieren einer Kontext Struktur in einem Puffer mit der erforderlichen Größe und Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="eeb5e-136">InitializeContext Function to Initialize a context structure inside a buffer with the necessary size and alignment</span></span>
-   <span data-ttu-id="eeb5e-137">Copycontext-Funktion zum Kopieren einer Quell Kontext Struktur (einschließlich eines beliebigen xstate) in eine initialisierte Ziel Kontext Struktur</span><span class="sxs-lookup"><span data-stu-id="eeb5e-137">CopyContext Function to copy a source context structure (including any XState) onto an initialized destination context structure</span></span>

  
<span data-ttu-id="eeb5e-138">**3.** zum Testen, festlegen und suchen des AVX-Zustands innerhalb eines Prozessor Kontexts sollte der Debugger Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="eeb5e-138">**3.** To test, set and locate the AVX state within a processor context, the debugger should use:</span></span>

-   <span data-ttu-id="eeb5e-139">Locatcher exstatefeature zum Abrufen eines Zeigers auf den Prozessor Zustand für eine einzelne xstate-Funktion innerhalb einer Kontext Struktur</span><span class="sxs-lookup"><span data-stu-id="eeb5e-139">LocateXStateFeature to retrieve a pointer to the processor state for an individual XState feature within a context structure</span></span>
-   <span data-ttu-id="eeb5e-140">Getxstatefeaturesmask zum Zurückgeben der Maske von xstate-Funktionen, die innerhalb einer Kontext Struktur festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-140">GetXStateFeaturesMask to return the mask of XState features set within a context structure</span></span>
-   <span data-ttu-id="eeb5e-141">Setxstatefeaturesmask zum Festlegen der Maske von xstate-Funktionen, die innerhalb einer Kontext Struktur festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="eeb5e-141">SetXStateFeaturesMask to set the mask of XState features set within a context structure</span></span>

  


## <a name="links-to-other-resources"></a><span data-ttu-id="eeb5e-142">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="eeb5e-142">Links to Other Resources</span></span>

-   <span data-ttu-id="eeb5e-143">Informationen zu den xstate-Funktionen in der Windows SDK finden Sie unter [Debuggingfunktionen](../debug/debugging-functions.md).</span><span class="sxs-lookup"><span data-stu-id="eeb5e-143">For information about the XState functions in the Windows SDK, see [Debugging Functions](../debug/debugging-functions.md).</span></span>
-   <span data-ttu-id="eeb5e-144">Eine Übersicht über die Anweisungen und Funktionen von Intel AVX finden Sie unter [Intel AVX: New Frontiers in Performance Verbesserungen und Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span><span class="sxs-lookup"><span data-stu-id="eeb5e-144">For an overview of the instructions and capabilities of the Intel AVX, see [Intel AVX: New Frontiers in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span></span>

 

 
