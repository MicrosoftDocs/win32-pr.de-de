---
description: .
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Benutzeroberfläche-Dialog Informationen zur Benutzerkontensteuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5711f8bbed029102bea81e0f4cfcbd4649b5a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354024"
---
# <a name="user-interface---user-account-control-dialog-updates"></a><span data-ttu-id="86b08-103">Benutzeroberfläche-Dialog Informationen zur Benutzerkontensteuerung</span><span class="sxs-lookup"><span data-stu-id="86b08-103">User Interface - User Account Control Dialog Updates</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="86b08-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="86b08-104">Affected Platforms</span></span>

<span data-ttu-id="86b08-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="86b08-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="86b08-106">**Server** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="86b08-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="86b08-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="86b08-107">Feature Impact</span></span>

<span data-ttu-id="86b08-108">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="86b08-108">**Severity** - Low</span></span>  
<span data-ttu-id="86b08-109">**Frequency** -Medium</span><span class="sxs-lookup"><span data-stu-id="86b08-109">**Frequency** - Medium</span></span>  











## <a name="description"></a><span data-ttu-id="86b08-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="86b08-110">Description</span></span>

<span data-ttu-id="86b08-111">In Windows 7 haben wir die Optionen für das UAC-Dialogfeld standardisiert.</span><span class="sxs-lookup"><span data-stu-id="86b08-111">In Windows 7, we have standardized the UAC dialog box choices.</span></span> <span data-ttu-id="86b08-112">Zuvor mussten die Benutzer mehrere Optionen auswählen, z. b. "Fortfahren", "Abbrechen" usw.</span><span class="sxs-lookup"><span data-stu-id="86b08-112">Previously, users had to select from multiple options, for example, "Continue," "Cancel," and so on.</span></span> <span data-ttu-id="86b08-113">Alle Dialogfelder lassen Benutzern nun ein einfaches "yes" oder "No" (Nein).</span><span class="sxs-lookup"><span data-stu-id="86b08-113">Now all dialog boxes give users a simple "Yes" or "No."</span></span> <span data-ttu-id="86b08-114">Im Dialogfeld Layout werden nun auch der Programmname, der Herausgeber und der Ursprung deutlich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="86b08-114">The dialog layout now also clearly shows the program name, publisher, and origin.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="86b08-115">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="86b08-115">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="86b08-116">Die Anwendungs Entwicklungsanforderungen in Windows 7 für die UAC-Kompatibilität sind identisch mit denen in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="86b08-116">The application development requirements in Windows 7 for UAC compatibility are the same as in Windows Vista.</span></span> <span data-ttu-id="86b08-117">Windows Vista-kompatible Anwendungen interagieren ohne Änderungen mit UAC in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="86b08-117">Windows Vista-compatible applications will interact with UAC in Windows 7 without any modifications.</span></span> <span data-ttu-id="86b08-118">Informationen dazu, wie Windows XP-Anwendungen unter Windows 7 ordnungsgemäß funktionieren, finden Sie in den Themen zur Benutzerkontensteuerung im *Cookbook zur Windows Vista-Anwendungs Kompatibilität* .</span><span class="sxs-lookup"><span data-stu-id="86b08-118">See the User Account Control topics in the *Windows Vista Application Compatibility Cookbook* for information about how to make Windows XP applications work correctly on Windows 7.</span></span> <span data-ttu-id="86b08-119">Die UAC-Verbesserungen für Windows 7 wirken sich zwar auf die Benutzeroberfläche aus, Sie wirken sich jedoch nicht auf die Anwendungs Schnittstelle aus.</span><span class="sxs-lookup"><span data-stu-id="86b08-119">While the UAC improvements for Windows 7 will impact the user's experience, they will not impact the application interface.</span></span> <span data-ttu-id="86b08-120">Wenn jedoch Hilfe Inhalt mit den UAC-Dialogfeldern verknüpft ist, müssen Sie möglicherweise die Screenshots aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="86b08-120">However, if there is any help content linked to the UAC dialogs, you may need to update the screenshots.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="86b08-121">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="86b08-121">Links to Other Resources</span></span>

-   <span data-ttu-id="86b08-122">[Cookbook zur Windows Vista-Anwendungs Kompatibilität](/previous-versions/bb757005(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="86b08-122">[Windows Vista Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10))</span></span>
-   [<span data-ttu-id="86b08-123">Anwendungskompatibilitäts-Toolkit Download</span><span class="sxs-lookup"><span data-stu-id="86b08-123">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="86b08-124">[Standardbenutzeranalyse](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="86b08-124">[Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span></span>

> [!Note]  
> <span data-ttu-id="86b08-125">Diese Ressourcen sind in einigen Sprachen und Ländern bzw. Regionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="86b08-125">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
