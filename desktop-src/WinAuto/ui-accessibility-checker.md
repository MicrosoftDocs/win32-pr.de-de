---
title: Barrierefreiheits Tools-accchecker (UI-Zugriffs Prüfung)
description: Beschreibt die Zugriffs Prüfung (UI-Zugriffs Überprüfung), ein Tool zum Testen der Benutzeroberflächenautomatisierungs-oder Active Accessibility Microsoft-Implementierung (MSAA) einer Anwendung.
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- UI Accessibility Checker
- Zugriffs Prüfung
- Implementierung der Benutzeroberflächen Automatisierung, testen
- UIA-Implementierung, testen
- Microsoft Active Accessibility-Implementierung, testen
- MSAA-Implementierung, testen
- Testen der Benutzeroberflächen Automatisierung
- Testen von UIA
- Testen von Microsoft Active Accessibility
- Testen von MSAA
- UIA-TestTools
- Benutzeroberflächenautomatisierungs-TestTools
- MSAA-TestTools
- Microsoft Active Accessibility TestTools
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "106341290"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a><span data-ttu-id="73f7a-117">Barrierefreiheits Tools-accchecker (UI-Zugriffs Prüfung)</span><span class="sxs-lookup"><span data-stu-id="73f7a-117">Accessibility tools - AccChecker (UI Accessibility Checker)</span></span>

<span data-ttu-id="73f7a-118">Die **Zugriffs** Prüfung (UI-Zugriffs Prüfung) überprüft, ob die erforderlichen Barrierefreiheits Anforderungen der Benutzeroberfläche bei der Entwicklung und Implementierung von Benutzeroberflächen Automatisierung (UIA) oder Microsoft Active Accessibility (MSAA) unabhängig vom zugrunde liegenden Benutzeroberflächen Framework erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="73f7a-118">**AccChecker** (UI Accessibility Checker) verifies that key UI accessibility requirements are met in the design and implementation of UI Automation (UIA) or Microsoft Active Accessibility (MSAA) regardless of the underlying UI framework.</span></span> <span data-ttu-id="73f7a-119">Die **Zugriffs** Prüfung umfasst auch eine Reihe von webbarrierefreiheits Überprüfungen.</span><span class="sxs-lookup"><span data-stu-id="73f7a-119">**AccChecker** also includes a set of web accessibility verifications.</span></span>

<span data-ttu-id="73f7a-120">**Accchecker** bietet die folgenden Ebenen der Funktionalität:</span><span class="sxs-lookup"><span data-stu-id="73f7a-120">**AccChecker** provides the following levels of functionality:</span></span>

- <span data-ttu-id="73f7a-121">Eine Windows-GUI-Anwendung, die manuelle Tests, Nachrichten Protokollierung und Unterdrückungs Generierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="73f7a-121">A Windows GUI application that supports manual testing, message logging, and suppression generation.</span></span>
- <span data-ttu-id="73f7a-122">Eine API zur Verwendung in automatisierten Test-Frameworks.</span><span class="sxs-lookup"><span data-stu-id="73f7a-122">An API for use in automated testing frameworks.</span></span>
- <span data-ttu-id="73f7a-123">Eine Konsolenanwendung, die nicht verwaltete Test Automatisierungen für Szenarien unterstützt, in denen die von der **accchecker** verwaltete API nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="73f7a-123">A console application that supports unmanaged test automations for scenarios where the **AccChecker** managed API can't be used.</span></span>

<span data-ttu-id="73f7a-124">Alle Ebenen der **accchecker** -Funktionalität stellen Routinen zum Überprüfen von Microsoft Active Accessibility programmgesteuerten Zugriff, programmgesteuerte Ereignis Generierung, Steuerelement Layout und Tastaturnavigation bereit.</span><span class="sxs-lookup"><span data-stu-id="73f7a-124">All levels of **AccChecker** functionality provide routines for verifying Microsoft Active Accessibility programmatic access, programmatic event generation, control layout, and keyboard navigation.</span></span> <span data-ttu-id="73f7a-125">**Accchecker** bietet auch einen grundlegenden Screenreader-Transkriptions Dienst.</span><span class="sxs-lookup"><span data-stu-id="73f7a-125">**AccChecker** also provides a basic screen reader transcription service.</span></span>

<span data-ttu-id="73f7a-126">**Accchecker** wird mit dem Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="73f7a-126">**AccChecker** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="73f7a-127">Sie befindet sich im \\ Ordner "bin \\ < *Version* > \\ < *Platform* > \\ accchecker" des SDK-Installations Pfads.</span><span class="sxs-lookup"><span data-stu-id="73f7a-127">It is located in the \\bin\\<*version*>\\<*platform*>\\AccChecker folder of the SDK installation path.</span></span>

> [!NOTE]
> <span data-ttu-id="73f7a-128">**Accchecker** ist ein Legacy Tool.</span><span class="sxs-lookup"><span data-stu-id="73f7a-128">**AccChecker** is a legacy tool.</span></span> <span data-ttu-id="73f7a-129">Stattdessen wird die [](https://accessibilityinsights.io/) Verwendung von eingabeinsights empfohlen.</span><span class="sxs-lookup"><span data-stu-id="73f7a-129">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="73f7a-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="73f7a-130">Requirements</span></span>

<span data-ttu-id="73f7a-131">Erfordert .NET Framework 2,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="73f7a-131">Requires .NET Framework 2.0 or later.</span></span>

<span data-ttu-id="73f7a-132">Die **Zugriffs** Prüfung kann verwendet werden, um Barrierefreiheits Daten auf Systemen zu untersuchen, die nicht über Microsoft-Benutzeroberflächen Automatisierung verfügen, aber nur die Eigenschaften von Microsoft Active Accessibility untersuchen</span><span class="sxs-lookup"><span data-stu-id="73f7a-132">**AccChecker** can be used to examine accessibility data on systems that don't have Microsoft UI Automation, but can only examine the Microsoft Active Accessibility properties.</span></span> <span data-ttu-id="73f7a-133">Zum Untersuchen der Benutzeroberflächen Automatisierung muss die Benutzeroberflächen Automatisierung auf dem System vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="73f7a-133">To examine UI Automation, UI Automation must be present on the system.</span></span> <span data-ttu-id="73f7a-134">Weitere Informationen finden Sie im Abschnitt "Anforderungen" unter [UI Automation](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="73f7a-134">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="73f7a-135">Die **Zugriffs** Prüfung wird als Teil der Gesamtmenge der Tools im Windows SDK installiert und nicht als separater Download der exe-Datei verteilt.</span><span class="sxs-lookup"><span data-stu-id="73f7a-135">**AccChecker** is installed as part of the overall set of tools in theWindows SDK, it is not distributed as a separate exe download.</span></span> <span data-ttu-id="73f7a-136">Die Windows SDK umfasst alle Tools für die Barrierefreiheit, die in diesem Abschnitt dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="73f7a-136">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="73f7a-137">Holen Sie sich den Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="73f7a-137">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="73f7a-138">(Es gibt auch ein SDK-Download Archiv, das von dieser Seite verknüpft ist, wenn Sie eine vorherige Version benötigen.)</span><span class="sxs-lookup"><span data-stu-id="73f7a-138">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="73f7a-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73f7a-139">Related topics</span></span>

- [<span data-ttu-id="73f7a-140">Überwachung für barrierefreie Ereignisse</span><span class="sxs-lookup"><span data-stu-id="73f7a-140">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
- [<span data-ttu-id="73f7a-141">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="73f7a-141">Inspect</span></span>](inspect-objects.md)
- [<span data-ttu-id="73f7a-142">TestTools</span><span class="sxs-lookup"><span data-stu-id="73f7a-142">Testing Tools</span></span>](testing-tools.md)
- [<span data-ttu-id="73f7a-143">Benutzeroberflächenautomatisierungs-Überprüfung</span><span class="sxs-lookup"><span data-stu-id="73f7a-143">UI Automation Verify</span></span>](ui-automation-verify.md)
