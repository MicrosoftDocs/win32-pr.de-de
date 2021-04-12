---
title: UI-Automatisierungs Überprüfung (UIA-Überprüfung)
description: UI Automation Verify (UIA Verify) ist ein Test Framework für manuelles und automatisiertes Testen der Implementierung von Microsoft UI Automation eines Steuer Elements oder einer Anwendung.
ms.assetid: C66AF411-2746-4695-A893-1552B3ED1066
keywords:
- Benutzeroberflächenautomatisierungs-Überprüfung
- UIA-Überprüfung
- Implementierung der Benutzeroberflächen Automatisierung, testen
- Testen der Benutzeroberflächen Automatisierung
- UIA-TestTools
- Benutzeroberflächenautomatisierungs-TestTools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b794e5d191c07a9c0db602ebac0f908bbdf960bf
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389956"
---
# <a name="accessibility-tools---ui-automation-verify-uia-verify"></a><span data-ttu-id="4fabd-109">Barrierefreiheits Tools-UI Automation Verify (UIA Verify)</span><span class="sxs-lookup"><span data-stu-id="4fabd-109">Accessibility tools - UI Automation Verify (UIA Verify)</span></span>

<span data-ttu-id="4fabd-110">**UI Automation Verify (UIA Verify)** ist ein Test Framework für manuelles und automatisiertes Testen der Implementierung von Microsoft UI Automation eines Steuer Elements oder einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="4fabd-110">**UI Automation Verify (UIA Verify)** is a testing framework for manual and automated testing of a control's or application's implementation of Microsoft UI Automation.</span></span> <span data-ttu-id="4fabd-111">Die meisten Funktionen des Test Frameworks stammen aus einer DLL mit dem Namen WUIATestLibrary.dll.</span><span class="sxs-lookup"><span data-stu-id="4fabd-111">Most of the testing framework's functionality comes from a DLL called WUIATestLibrary.dll.</span></span> <span data-ttu-id="4fabd-112">Diese DLL enthält den Code zum Testen spezifischer Benutzeroberflächenautomatisierungs-Funktionen und unterstützt auch die Protokollierung der Testergebnisse.</span><span class="sxs-lookup"><span data-stu-id="4fabd-112">This DLL contains the code for testing specific UI Automation functionality, and it also supports logging of the test results.</span></span> <span data-ttu-id="4fabd-113">Sie können Ihre Anwendung in den Testcode integrieren und regelmäßige, automatisierte Tests oder Überprüfungen der Benutzeroberflächenautomatisierungs-Szenarios durchführen.</span><span class="sxs-lookup"><span data-stu-id="4fabd-113">You can integrate your application into the test code and conduct regular, automated testing or spot checks of your UI Automation scenarios.</span></span>

<span data-ttu-id="4fabd-114">Die **UIA-Überprüfung** wird mit dem Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="4fabd-114">**UIA Verify** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4fabd-115">Sie befindet sich im \\ Ordner "bin \\ < *Version* > \\ < *Platform* > \\ uiaverify" des SDK-Installations Pfads (VisualUIAVerifyNative.exe).</span><span class="sxs-lookup"><span data-stu-id="4fabd-115">It is located in the \\bin\\<*version*>\\<*platform*>\\UIAVerify folder of the SDK installation path (VisualUIAVerifyNative.exe).</span></span>

<span data-ttu-id="4fabd-116">Die **UIA-Überprüfung** besteht aus einer API namens Benutzeroberflächenautomatisierungs-Test Bibliothek und einer GUI-Schnittstelle namens Visual **UI Automation Verify**.</span><span class="sxs-lookup"><span data-stu-id="4fabd-116">**UIA Verify** consists of an API called the UI Automation Test Library, and a GUI interface called Visual **UI Automation Verify**.</span></span> <span data-ttu-id="4fabd-117">Diese werden in den folgenden Themen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4fabd-117">These are described in the following topics.</span></span>

> [!NOTE]
> <span data-ttu-id="4fabd-118">**Benutzeroberflächenautomatisierungs-Überprüfung** ist ein Legacy Tool.</span><span class="sxs-lookup"><span data-stu-id="4fabd-118">**UI Automation Verify** is a legacy tool.</span></span> <span data-ttu-id="4fabd-119">Stattdessen wird die [](https://accessibilityinsights.io/) Verwendung von eingabeinsights empfohlen.</span><span class="sxs-lookup"><span data-stu-id="4fabd-119">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fabd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fabd-120">Requirements</span></span>

<span data-ttu-id="4fabd-121">Die Benutzeroberflächen Automatisierung muss auf dem System vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4fabd-121">UI Automation must be present on the system.</span></span> <span data-ttu-id="4fabd-122">Weitere Informationen finden Sie im Abschnitt "Anforderungen" unter [UI Automation](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="4fabd-122">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="4fabd-123">**UIA Verify** wird als Teil der Gesamtmenge der Tools im Windows SDK installiert, nicht als separater Download.</span><span class="sxs-lookup"><span data-stu-id="4fabd-123">**UIA Verify** is installed as part of the overall set of tools in the Windows SDK, it is not distributed as a separate download.</span></span> <span data-ttu-id="4fabd-124">Die Windows SDK umfasst alle Tools für die Barrierefreiheit, die in diesem Abschnitt dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="4fabd-124">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="4fabd-125">Holen Sie sich den Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4fabd-125">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="4fabd-126">(Es gibt auch ein SDK-Download Archiv, das von dieser Seite verknüpft ist, wenn Sie eine vorherige Version benötigen.)</span><span class="sxs-lookup"><span data-stu-id="4fabd-126">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

<span data-ttu-id="4fabd-127">Um die **UIA-Überprüfung** als visuelles Tool auszuführen, suchen Sie VisualUIAVerifyNative.exe im \\ Ordner "bin \\ < *Platform* > \\ uiaverify", und führen Sie Sie aus (Sie müssen in der Regel nicht als Administrator ausgeführt werden).</span><span class="sxs-lookup"><span data-stu-id="4fabd-127">To run **UIA Verify** as a visual tool, find VisualUIAVerifyNative.exe in the \\bin\\<*platform*>\\UIAVerify folder and run it (you don't typically have to run as administrator).</span></span> <span data-ttu-id="4fabd-128">Weitere Informationen finden Sie unter [Überprüfen der Visual UI-Automatisierung](visual-ui-automation-verify.md).</span><span class="sxs-lookup"><span data-stu-id="4fabd-128">For more information, see [Visual UI Automation Verify](visual-ui-automation-verify.md).</span></span> <span data-ttu-id="4fabd-129">Informationen zur Verwendung der Bibliotheken finden Sie unter [UI Automation Test Library](ui-automation-test-library.md).</span><span class="sxs-lookup"><span data-stu-id="4fabd-129">To use the libraries, see [UI Automation Test Library](ui-automation-test-library.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4fabd-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4fabd-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fabd-131">Überwachung für barrierefreie Ereignisse</span><span class="sxs-lookup"><span data-stu-id="4fabd-131">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
</dt> <dt>

[<span data-ttu-id="4fabd-132">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="4fabd-132">Inspect</span></span>](inspect-objects.md)
</dt> <dt>

[<span data-ttu-id="4fabd-133">TestTools</span><span class="sxs-lookup"><span data-stu-id="4fabd-133">Testing Tools</span></span>](testing-tools.md)
</dt> <dt>

[<span data-ttu-id="4fabd-134">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="4fabd-134">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




