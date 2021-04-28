---
description: Aktivieren der Windows 7-Unterstützung für Intel AVX
ms.assetid: fe19e337-3109-42d6-a704-70662ac7c684
title: Aktivieren der Windows 7-Unterstützung für Intel AVX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1509bac62634c85aa733b2c1de0c152169ac6cda
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088458"
---
# <a name="enable-windows-7-support-for-intel-avx"></a><span data-ttu-id="e315e-103">Aktivieren der Windows 7-Unterstützung für Intel AVX</span><span class="sxs-lookup"><span data-stu-id="e315e-103">Enable Windows 7 Support for Intel AVX</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="e315e-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="e315e-104">Affected Platforms</span></span>

 <span data-ttu-id="e315e-105">**Clients** – Windows 7 SP1</span><span class="sxs-lookup"><span data-stu-id="e315e-105">**Clients** - Windows 7 SP1</span></span>  
<span data-ttu-id="e315e-106">**Server** – Windows Server 2008 R2 SP1</span><span class="sxs-lookup"><span data-stu-id="e315e-106">**Servers** - Windows Server 2008 R2 SP1</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="e315e-107">Auswirkungen auf Features</span><span class="sxs-lookup"><span data-stu-id="e315e-107">Feature Impact</span></span>

 <span data-ttu-id="e315e-108">**Schweregrad –** Niedrig</span><span class="sxs-lookup"><span data-stu-id="e315e-108">**Severity** - Low</span></span>  
<span data-ttu-id="e315e-109">**Häufigkeit** : Niedrig</span><span class="sxs-lookup"><span data-stu-id="e315e-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="e315e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e315e-110">Description</span></span>

<span data-ttu-id="e315e-111">Intel<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="e315e-111">Intel<sup>?</sup></span></span> <span data-ttu-id="e315e-112">Advanced Vector Extensions (AVX)<sup>?</sup></span><span class="sxs-lookup"><span data-stu-id="e315e-112">Advanced Vector Extensions (AVX)<sup>?</sup></span></span> <span data-ttu-id="e315e-113">ist eine 256-Bit-SIMD-Gleitkommavektorerweiterung der Intel-Architektur.</span><span class="sxs-lookup"><span data-stu-id="e315e-113">is a 256-bit SIMD floating-point vector extension of Intel architecture.</span></span> <span data-ttu-id="e315e-114">Sie enthält Erweiterungen für Anweisungs- und Registersätze.</span><span class="sxs-lookup"><span data-stu-id="e315e-114">It includes extensions to both instruction and register sets.</span></span>

<span data-ttu-id="e315e-115">Microsoft hat einige API-Erweiterungen entwickelt, z. B. XState-Funktionen, mit denen Anwendungen auf erweiterte Prozessorfeatureinformationen und -zustände zugreifen und diese bearbeiten können, einschließlich AVX.</span><span class="sxs-lookup"><span data-stu-id="e315e-115">Microsoft has developed some API enhancements, such as XState functions, that enable applications to access and manipulate extended processor feature information and state, including AVX.</span></span>

## <a name="usage-scenarios"></a><span data-ttu-id="e315e-116">Verwendungsszenarien</span><span class="sxs-lookup"><span data-stu-id="e315e-116">Usage Scenarios</span></span>

<span data-ttu-id="e315e-117">Es gibt drei allgemeine Ebenen potenzieller Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="e315e-117">There are three general levels of potential impact.</span></span>

<span data-ttu-id="e315e-118">**Ebene 1:** Anwendungen, die Intel AVX nicht direkt verwenden, haben keine Auswirkungen auf ihre Funktionalität, selbst wenn sie Bibliotheken aufrufen oder Compiler verwenden, die intel AVX-Erweiterungen indirekt verwenden oder generieren.</span><span class="sxs-lookup"><span data-stu-id="e315e-118">**Level 1:** Applications that do not directly use Intel AVX will not see any impact to their functionality even if they call into libraries or use compilers that indirectly use or generate Intel AVX extensions.</span></span> <span data-ttu-id="e315e-119">Dies stellt den weitaus größten Teil der Anwendungen dar.</span><span class="sxs-lookup"><span data-stu-id="e315e-119">This represents by far the majority of applications.</span></span>

<span data-ttu-id="e315e-120">**Ebene 2:** Erweiterte Anwendungen, die explizit den Intel AVX-Anweisungssatz verwenden, können auf AVX-Registerinhalte zugreifen und diese ändern, wenn eine Hardwareausnahme ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="e315e-120">**Level 2:** Advanced applications that explicitly use the Intel AVX instruction set will be able to access and change AVX register contents when a hardware exception is raised.</span></span> <span data-ttu-id="e315e-121">Eine sehr kleine Anzahl von Anwendungen würde in diese Kategorie fallen, da sie ein fundiertes Wissen über den Anweisungsstream impliziert, der zum Zeitpunkt der Ausnahme ausgeführt wird, z. B. Anwendungen mit Abschnitten, die in der Assemblysprache geschrieben sind, oder solche, die Computercode zur Laufzeit generieren (z. B. Laufzeiten von verwaltetem Code mit Just-in-Time-Kompilierung).</span><span class="sxs-lookup"><span data-stu-id="e315e-121">A very small number of applications would fall into this category, as it implies an intimate knowledge of the instruction stream executing at the time of the exception, such as applications with sections written in assembly language or those that generate machine code at runtime (for example, managed code runtimes with just-in-time compilation).</span></span>

<span data-ttu-id="e315e-122">**Ebene 3:** Debuggeranwendungen können auf den AVX-Status in der zu debuggenden Anwendung zugreifen und diesen bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e315e-122">**Level 3:** Debugger applications will be able to access and manipulate the AVX state in the application being debugged.</span></span>

## <a name="how-to-leverage-feature-capabilities"></a><span data-ttu-id="e315e-123">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="e315e-123">How to Leverage Feature Capabilities</span></span>

<span data-ttu-id="e315e-124">**Ebene 1:** Es ist keine Aktion erforderlich, damit Anwendungen Intel AVX verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e315e-124">**Level 1:** No action is necessary for applications to use Intel AVX.</span></span>

<span data-ttu-id="e315e-125">**Ebene 2:** Anwendungen in dieser Kategorie haben die Möglichkeit, in ihren Ausnahmefiltern auf den AVX-Zustand zum Zeitpunkt der Ausnahme zu zugreifen und ihn zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e315e-125">**Level 2:** Applications in this category have the option to access and manipulate AVX state at the time of the exception from within their exception filters.</span></span> <span data-ttu-id="e315e-126">Nach dem Abrufen des Basisprozessorkontexts über GetExceptionInformation sollten Filter:</span><span class="sxs-lookup"><span data-stu-id="e315e-126">After obtaining the base processor context via GetExceptionInformation, filters should:</span></span>

 <span data-ttu-id="e315e-127">**1. Überprüfen** Sie den Wert des **CONTEXT \_ XSTATE-Flags.**</span><span class="sxs-lookup"><span data-stu-id="e315e-127">**1.** Check the value of the **CONTEXT\_XSTATE** flag.</span></span> <span data-ttu-id="e315e-128">Dieses Flag gibt an, dass mindestens ein XState-Feature im Kontext vorlag.</span><span class="sxs-lookup"><span data-stu-id="e315e-128">This flag indicates the presence of at least one XState feature in the context.</span></span>  
<span data-ttu-id="e315e-129">**2.** Wenn dies der Fall ist, rufen Sie **GetXStateFeaturesMask** auf, und testen Sie den Wert des **XSTATE \_ AVX-Flags** in der zurückgegebenen Maske.</span><span class="sxs-lookup"><span data-stu-id="e315e-129">**2.** If this is the case, call **GetXStateFeaturesMask** and test the value of the **XSTATE\_AVX** flag in the returned mask.</span></span> <span data-ttu-id="e315e-130">Dies gibt das Vorhandensein des AVX-Zustands im Kontext an.</span><span class="sxs-lookup"><span data-stu-id="e315e-130">This indicates the presence of AVX state in the context.</span></span>  
<span data-ttu-id="e315e-131">**3. Rufen Sie** **LocateXStateFeature auf,** um den tatsächlichen Speicherort des AVX-Zustands abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e315e-131">**3.** Call **LocateXStateFeature** to retrieve the actual location where the AVX state is stored.</span></span>  

<span data-ttu-id="e315e-132">**Ebene 3:** Es ist nicht erforderlich, vorhandene Debuggeranwendungen zu aktualisieren, es sei denn, sie möchten auf die Intel AVX-Register zugreifen:</span><span class="sxs-lookup"><span data-stu-id="e315e-132">**Level 3:** It is not necessary to update existing debugger applications unless they wish access the Intel AVX registers:</span></span>

<span data-ttu-id="e315e-133">**1.** Um zu bestimmen, ob AVX aktiviert ist, sollte der Debugger Verwenden:</span><span class="sxs-lookup"><span data-stu-id="e315e-133">**1.** To determine if AVX is enabled, the debugger should use:</span></span>

-   <span data-ttu-id="e315e-134">GetEnabledXStateFeatures zum Erhalten einer Maske aktivierter XState-Features auf x86- oder x64-Prozessoren, um zu bestimmen, welche Features auf dem System vorhanden und aktiviert sind, bevor ein XState-Prozessorfeature verwendet oder versucht wird, XState-Kontexte zu bearbeiten</span><span class="sxs-lookup"><span data-stu-id="e315e-134">GetEnabledXStateFeatures to get a mask of enabled XState features on x86 or x64 processors to determine what features are present and enabled on the system before using an XState processor feature or attempting to manipulate XState contexts</span></span>

  
<span data-ttu-id="e315e-135">**2.** Wenn AVX vorhanden ist und Sie den AVX-Zustand aus der zu debuggenden Anwendung abrufen und bearbeiten möchten (z. B. GetThreadContext und SetThreadContext), sollte der Debugger Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="e315e-135">**2.** If AVX is present and you wish to retrieve and manipulate the AVX state from the application being debugged (for example, GetThreadContext and SetThreadContext), the debugger should use:</span></span>

-   <span data-ttu-id="e315e-136">InitializeContext-Funktion zum Initialisieren einer Kontextstruktur innerhalb eines Puffers mit der erforderlichen Größe und Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="e315e-136">InitializeContext Function to Initialize a context structure inside a buffer with the necessary size and alignment</span></span>
-   <span data-ttu-id="e315e-137">CopyContext-Funktion zum Kopieren einer Quellkontextstruktur (einschließlich eines beliebigen XState) in eine initialisierte Zielkontextstruktur</span><span class="sxs-lookup"><span data-stu-id="e315e-137">CopyContext Function to copy a source context structure (including any XState) onto an initialized destination context structure</span></span>

  
<span data-ttu-id="e315e-138">**3.** Zum Testen, Festlegen und Suchen des AVX-Zustands in einem Prozessorkontext sollte der Debugger Verwenden:</span><span class="sxs-lookup"><span data-stu-id="e315e-138">**3.** To test, set and locate the AVX state within a processor context, the debugger should use:</span></span>

-   <span data-ttu-id="e315e-139">LocateXStateFeature zum Abrufen eines Zeigers auf den Prozessorzustand für ein einzelnes XState-Feature innerhalb einer Kontextstruktur</span><span class="sxs-lookup"><span data-stu-id="e315e-139">LocateXStateFeature to retrieve a pointer to the processor state for an individual XState feature within a context structure</span></span>
-   <span data-ttu-id="e315e-140">GetXStateFeaturesMask zum Zurückgeben der Maske von XState-Features, die innerhalb einer Kontextstruktur festgelegt sind</span><span class="sxs-lookup"><span data-stu-id="e315e-140">GetXStateFeaturesMask to return the mask of XState features set within a context structure</span></span>
-   <span data-ttu-id="e315e-141">SetXStateFeaturesMask zum Festlegen der Maske von XState-Features, die innerhalb einer Kontextstruktur festgelegt sind</span><span class="sxs-lookup"><span data-stu-id="e315e-141">SetXStateFeaturesMask to set the mask of XState features set within a context structure</span></span>

  


## <a name="links-to-other-resources"></a><span data-ttu-id="e315e-142">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e315e-142">Links to Other Resources</span></span>

-   <span data-ttu-id="e315e-143">Informationen zu den XState-Funktionen im Windows SDK finden Sie unter [Debuggen von Funktionen.](../debug/debugging-functions.md)</span><span class="sxs-lookup"><span data-stu-id="e315e-143">For information about the XState functions in the Windows SDK, see [Debugging Functions](../debug/debugging-functions.md).</span></span>
-   <span data-ttu-id="e315e-144">Eine Übersicht über die Anweisungen und Funktionen von Intel AVX finden Sie unter [Intel AVX: New Grenzlinien in Leistungsverbesserungen und Energieeffizienz.](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/)</span><span class="sxs-lookup"><span data-stu-id="e315e-144">For an overview of the instructions and capabilities of the Intel AVX, see [Intel AVX: New Frontiers in Performance Improvements and Energy Efficiency](https://software.intel.com/articles/intel-avx-new-frontiers-in-performance-improvements-and-energy-efficiency/).</span></span>

 

 
