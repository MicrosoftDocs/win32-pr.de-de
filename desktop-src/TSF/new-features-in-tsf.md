---
title: Neue Features in TSF
description: Mit der Veröffentlichung von Microsoft WindowsXP Service Pack 1 bietet das Text Services-Framework (TSF) mehrere neue Features.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Text Services Framework (TSF), neue Features
- TSF (Text Dienst Framework), neue Features
- Text Dienste, neue Features
- TSF-aktivierte Anwendungen, neue Features
- Text Services Framework (TSF), erweiterter Support
- TSF (Text Dienst Framework), erweiterter Support
- Text Dienste, erweiterter Support
- TSF-fähige Anwendungen, erweiterter Support
- Text Services-Framework (TSF), umfangreiche Bearbeitung
- TSF (Text Dienst Framework), umfangreiche Bearbeitung
- Text Dienste, umfangreiche Bearbeitung
- TSF-fähige Anwendungen, umfangreiche Bearbeitung
- Umfassende Bearbeitung
- Text Dienst Framework (TSF), Sicherheit
- TSF (Text Dienst Framework), Sicherheit
- Text Dienste, Sicherheit
- TSF-aktivierte Anwendungen, Sicherheit
- Sicherheit für TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a345087304be638be93fa352845cdd468bf15
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390409"
---
# <a name="new-features-in-tsf"></a><span data-ttu-id="47467-121">Neue Features in TSF</span><span class="sxs-lookup"><span data-stu-id="47467-121">New Features in TSF</span></span>

<span data-ttu-id="47467-122">Mit der Veröffentlichung von Microsoft WindowsXP Service Pack 1 bietet das Text Services-Framework (TSF) mehrere neue Features.</span><span class="sxs-lookup"><span data-stu-id="47467-122">With the release of Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) has several new features.</span></span>

## <a name="extended-support-of-advanced-text-services"></a><span data-ttu-id="47467-123">Erweiterter Support für erweiterte Text Dienste</span><span class="sxs-lookup"><span data-stu-id="47467-123">Extended Support of Advanced Text Services</span></span>

<span data-ttu-id="47467-124">Es wurde Unterstützung für TSF und Windows hinzugefügt, um eine konsistente Benutzeroberfläche für alle Anwendungen auf dem Desktop bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="47467-124">Support has been added to TSF and Windows to provide a consistent user interface for all applications across the desktop.</span></span> <span data-ttu-id="47467-125">Mit dieser neuen Unterstützung können ältere Anwendungen oder Steuerelemente, die TSF nicht kennen, einige erweiterte Text Dienste kostenlos nutzen.</span><span class="sxs-lookup"><span data-stu-id="47467-125">This new support enables legacy applications or controls that are not aware of TSF to take advantage of some advanced text services for free.</span></span> <span data-ttu-id="47467-126">Beispielsweise können die sprach Diktat-und Handschrift nun verwendet werden, um Text in ein Dokument in einer beliebigen Anwendung einzugeben.</span><span class="sxs-lookup"><span data-stu-id="47467-126">For example, speech dictation and handwriting can now be used to enter text into a document in any application.</span></span>

<span data-ttu-id="47467-127">Dieses neue Feature ist nur für den Windows XP-Dienst Pack 1 oder höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="47467-127">This new feature is available only for WindowsXP Service Pack1 or later.</span></span> <span data-ttu-id="47467-128">Sie ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47467-128">It is turned off by default.</span></span> <span data-ttu-id="47467-129">Um es zu aktivieren, aktivieren Sie das Kontrollkästchen auf der neuen Registerkarte " **erweitert** " im Bereich **Text Dienste und Eingabe Sprachen** der Systemsteuerung Regions **-und Sprachoptionen** .</span><span class="sxs-lookup"><span data-stu-id="47467-129">To enable it, click the check box in the new **Advanced** tab in the **Text Services and Input Languages** portion of the **Regional and Language Options** control panel.</span></span>

![nicht unterstützte Anwendungsunterstützung in der TSF-Systemsteuerung](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a><span data-ttu-id="47467-131">Umfangreiche Bearbeitungs Unterstützung</span><span class="sxs-lookup"><span data-stu-id="47467-131">Rich Edit Support</span></span>

<span data-ttu-id="47467-132">[Microsoft® reichhaltige Bearbeitung](../controls/rich-edit-controls.md) Version 4,1, die von Anwendungen verwendet wird, um Text mit Sonderzeichen-und Absatz Formatierung anzuzeigen und zu bearbeiten, stellt nun die TSF-Funktionalität zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="47467-132">[Microsoft® Rich Edit](../controls/rich-edit-controls.md) Version 4.1, used by applications to view and edit text with special character and paragraph formatting, now exposes TSF functionality.</span></span> <span data-ttu-id="47467-133">Diese Unterstützung ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="47467-133">By default this support is turned off.</span></span> <span data-ttu-id="47467-134">Zum Aktivieren von TSF in Rich Edit sendet eine Hostinganwendung eine spezielle Fenster Meldung an das Rich Edit-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="47467-134">To enable TSF in Rich Edit, a hosting application sends a special window message to the Rich Edit control.</span></span>

## <a name="security-improvements"></a><span data-ttu-id="47467-135">Sicherheitsverbesserungen</span><span class="sxs-lookup"><span data-stu-id="47467-135">Security Improvements</span></span>

<span data-ttu-id="47467-136">Die Sicherheit und Stabilität von TSF wurden erheblich verbessert, um die Wahrscheinlichkeit zu verringern, dass ein schädliches Programm auf den Stapel, Heap oder andere sichere Speicherorte zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="47467-136">The security and robustness of TSF have been substantially improved, to reduce the likelihood of a hostile program being able to access the stack, heap, or other secure memory locations.</span></span> <span data-ttu-id="47467-137">Die Security of Software Development Kit (SDK)-Beispielanwendungen und Text Dienste wurden ebenfalls verbessert.</span><span class="sxs-lookup"><span data-stu-id="47467-137">The security of software development kit (SDK) sample applications and text services has also been improved.</span></span>

 

 