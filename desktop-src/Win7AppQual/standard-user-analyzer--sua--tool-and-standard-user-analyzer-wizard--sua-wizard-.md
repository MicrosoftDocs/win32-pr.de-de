---
description: Erfahren Sie, wie Sie mit dem Tool "Standard User Analyzer" (SUA) und dem SUA-Assistenten Ihre Anwendungen testen und potenzielle Kompatibilitätsprobleme erkennen.
ms.assetid: 229ee531-32b9-4e11-b64c-3ce5b5ab6530
title: Standardbenutzeranalyse-Tool (Standard User Analyzer, SUA) und SUA-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99a897c603f185db775c059e4b3dd4a040cba9ad
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314583"
---
# <a name="standard-user-analyzer-sua-tool-and-standard-user-analyzer-wizard-sua-wizard"></a><span data-ttu-id="0c822-103">Standardbenutzeranalyse-Tool (Standard User Analyzer, SUA) und SUA-Assistent</span><span class="sxs-lookup"><span data-stu-id="0c822-103">Standard User Analyzer (SUA) Tool and Standard User Analyzer Wizard (SUA Wizard)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="0c822-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="0c822-104">Affected Platforms</span></span>

<span data-ttu-id="0c822-105">**Clients:** Windows XP, Windows Vista, Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c822-105">**Clients:** Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="0c822-106">**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="0c822-106">**Servers:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  

## <a name="description"></a><span data-ttu-id="0c822-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c822-107">Description</span></span>

<span data-ttu-id="0c822-108">Das Anwendungskompatibilitäts-Toolkit umfasst das Tool "Standard User Analyzer" (SUA) und den standardmäßigen benutzeranalyseassistenten (SUA Wizard).</span><span class="sxs-lookup"><span data-stu-id="0c822-108">The Application Compatibility Toolkit includes the Standard User Analyzer (SUA) tool and the Standard User Analyzer Wizard (SUA Wizard).</span></span> <span data-ttu-id="0c822-109">Mit diesen Tools können Sie Ihre Anwendungen testen und API-Aufrufe überwachen, um potenzielle Kompatibilitätsprobleme aufgrund der Benutzerkontensteuerung (User Account Control, UAC) im Windows 7-Betriebssystem zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="0c822-109">These tools enable you to test your applications and to monitor API calls in order to detect potential compatibility issues due to the User Account Control (UAC) feature in the Windows 7 operating system.</span></span>

<span data-ttu-id="0c822-110">UAC, früher als "eingeschränktes Benutzerkonto (LUA)" bezeichnet, erfordert, dass alle Benutzer (einschließlich der Mitglieder der Administrator Gruppe) als Standard Benutzer ausgeführt werden, indem Sie das Dialogfeld "Sicherheits Aufforderung" verwenden, bis die Anwendung absichtlich erhöht wird.</span><span class="sxs-lookup"><span data-stu-id="0c822-110">UAC, formerly known as Limited User Account (LUA), requires that all users (including members of the Administrator group) run as Standard Users by using the security prompt dialog box until the application is deliberately elevated.</span></span> <span data-ttu-id="0c822-111">Anwendungen, die Zugriff und Berechtigungen für Speicherorte benötigen, die für einen Standardbenutzer nicht verfügbar sind, können jedoch nicht ordnungsgemäß mit der Standard Benutzerrolle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0c822-111">However, applications that require access and privileges for locations that are unavailable to a Standard User cannot run properly with the Standard User role.</span></span>

## <a name="usage"></a><span data-ttu-id="0c822-112">Verwendung</span><span class="sxs-lookup"><span data-stu-id="0c822-112">Usage</span></span>

<span data-ttu-id="0c822-113">Die folgenden Abschnitte enthalten ausführliche Informationen zur Verwendung der Tools des SUA-und SUA-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="0c822-113">The following sections provide detailed information about how to use the SUA and SUA Wizard tools.</span></span>

<span data-ttu-id="0c822-114">**SUA-Tool**</span><span class="sxs-lookup"><span data-stu-id="0c822-114">**SUA Tool**</span></span>

<span data-ttu-id="0c822-115">Mit dem SUA-Tool können Sie eine Anwendung analysieren, einen ausführlichen Bericht zu den UAC-bezogenen Problemen überprüfen und dann die vorgeschlagenen und ausgewählten Anwendungs entschärfungen anwenden, wie im folgenden Flussdiagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0c822-115">The SUA tool enables you to analyze an application, review a detailed report about the UAC-related issues, and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span>

![Diagramm, das den Flow des S U A-Tools anzeigt.](images/act-suaflowchart-appcookbook.gif)

<span data-ttu-id="0c822-117">*SUA-Tool und Virtualisierung*</span><span class="sxs-lookup"><span data-stu-id="0c822-117">*SUA Tool and Virtualization*</span></span>

<span data-ttu-id="0c822-118">Nur das SUA-Tool ermöglicht es Ihnen, das Virtualisierungsfeature zu aktivieren und zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="0c822-118">Only the SUA tool enables you to turn on and off the virtualization feature.</span></span> <span data-ttu-id="0c822-119">Wenn Sie das Virtualisierungsfeature ausschalten, verhält sich die getestete Anwendung mehr, als Sie im Windows XP-Betriebssystem funktioniert.</span><span class="sxs-lookup"><span data-stu-id="0c822-119">By turning off the virtualization feature, the tested application will behave more like when it is functioning on the Windows XP operating system.</span></span>

<span data-ttu-id="0c822-120">*SUA-Tool und erweiterte Berechtigungen*</span><span class="sxs-lookup"><span data-stu-id="0c822-120">*SUA Tool and Elevated Privileges*</span></span>

<span data-ttu-id="0c822-121">Nur das SUA-Tool ermöglicht Ihnen das Aktivieren und Deaktivieren der Funktion zum **starten mit erhöhten** rechten.</span><span class="sxs-lookup"><span data-stu-id="0c822-121">Only the SUA tool enables you to turn on and off the **Launch Elevated** feature.</span></span> <span data-ttu-id="0c822-122">Mit dem Feature "mit erhöhten Rechten starten" kann die ausgewählte Anwendung als Administrator oder als Standard Benutzer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0c822-122">The Launch Elevated feature enables the selected application to run as an Administrator or as a Standard User.</span></span> <span data-ttu-id="0c822-123">Abhängig von Ihrer Auswahl finden Sie verschiedene Typen von UAC-bezogenen Problemen.</span><span class="sxs-lookup"><span data-stu-id="0c822-123">Depending on your selection, you will locate different types of UAC-related issues.</span></span> <span data-ttu-id="0c822-124">Wenn Sie das Kontrollkästchen mit **erhöhten Rechten starten** deaktivieren, wird Ihre Anwendung mit vollen Administrator Rechten ausgeführt, wodurch SUA die Probleme vorhersagen kann, die für einen Standard Benutzer auftreten können.</span><span class="sxs-lookup"><span data-stu-id="0c822-124">If you clear the **Launch Elevated** check box, your application will run with full Administrator privileges, which enables SUA to predict the issues that might occur for a Standard User.</span></span> <span data-ttu-id="0c822-125">Wenn Sie das Kontrollkästchen mit erhöhten Rechten starten aktivieren, werden Fehler angezeigt, die sich aus der eigentlichen Anwendung ergeben und Fehler erzeugen.</span><span class="sxs-lookup"><span data-stu-id="0c822-125">If you select the Launch Elevated check box, you will see errors that result from the application actually running and generating errors.</span></span>

<span data-ttu-id="0c822-126">**SUA-Assistent**</span><span class="sxs-lookup"><span data-stu-id="0c822-126">**SUA Wizard**</span></span>

<span data-ttu-id="0c822-127">Der SUA-Assistent ermöglicht es Ihnen, einen schrittweisen Prozess zu befolgen, mit dem Sie eine Anwendung analysieren und dann die vorgeschlagenen und ausgewählten Anwendungs entschärfungen anwenden können, wie im folgenden Flussdiagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="0c822-127">The SUA Wizard enables you to follow a guided, step-by-step process by which you can analyze an application and then apply the suggested and selected application mitigations, as shown in the following flowchart.</span></span> <span data-ttu-id="0c822-128">Im Gegensatz zum SUA-Tool ermöglicht der Assistent keine Überprüfung der detaillierten UAC-bezogenen Probleme.</span><span class="sxs-lookup"><span data-stu-id="0c822-128">Unlike the SUA tool, the wizard does not enable a review of the detailed UAC-related issues.</span></span>

![Diagramm, das den Flow des S U A-Assistenten anzeigt.](images/act-suaflowchart-appcookbook.gif)

## <a name="links-to-other-resources"></a><span data-ttu-id="0c822-130">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0c822-130">Links to Other Resources</span></span>

-   [<span data-ttu-id="0c822-131">Anwendungskompatibilitäts-Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="0c822-131">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="0c822-132">[Grundlegendes zu den Standard Tools für die Benutzer Analyse](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="0c822-132">[Understanding the Standard User Analyzer Tools](/previous-versions/windows/it-pro/windows-7/cc838047(v=ws.10))</span></span>
-   <span data-ttu-id="0c822-133">[Technische Referenz für Standard Benutzer Analyse](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="0c822-133">[Standard User Analyzer Technical Reference](/previous-versions/windows/it-pro/windows-7/cc765948(v=ws.10))</span></span>
-   <span data-ttu-id="0c822-134">[Testen und Beheben von Problemen mithilfe der Entwicklungs Tools](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="0c822-134">[Testing and Mitigating Issues by Using the Development Tools](/previous-versions/orphan-topics/ws.10/cc766461(v=ws.10))</span></span>
-   [<span data-ttu-id="0c822-135">Anwendungs Kompatibilität und Benutzerkontensteuerung</span><span class="sxs-lookup"><span data-stu-id="0c822-135">Application Compatibility and User Account Control</span></span>](/previous-versions/windows/)

> [!Note]  
> <span data-ttu-id="0c822-136">Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0c822-136">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
