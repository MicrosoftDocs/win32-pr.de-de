---
description: 'Benutzeroberfläche : Updates des Dialogfelds "Benutzerkontensteuerung"'
ms.assetid: f2d4b82d-a84a-4fc1-b7ad-cdc92a24f889
title: Benutzeroberfläche – Dialogfeld "Benutzerkontensteuerung" aktualisiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5cd6cc6709283c7bd9cba3e26bd2df29bb02ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094418"
---
# <a name="user-interface---user-account-control-dialog-updates"></a><span data-ttu-id="a62f0-103">Benutzeroberfläche : Updates des Dialogfelds "Benutzerkontensteuerung"</span><span class="sxs-lookup"><span data-stu-id="a62f0-103">User Interface - User Account Control Dialog Updates</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="a62f0-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="a62f0-104">Affected Platforms</span></span>

<span data-ttu-id="a62f0-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="a62f0-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="a62f0-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a62f0-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="a62f0-107">Auswirkungen auf Das Feature</span><span class="sxs-lookup"><span data-stu-id="a62f0-107">Feature Impact</span></span>

<span data-ttu-id="a62f0-108">**Schweregrad –** Niedrig</span><span class="sxs-lookup"><span data-stu-id="a62f0-108">**Severity** - Low</span></span>  
<span data-ttu-id="a62f0-109">**Frequency** - Medium</span><span class="sxs-lookup"><span data-stu-id="a62f0-109">**Frequency** - Medium</span></span>  











## <a name="description"></a><span data-ttu-id="a62f0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a62f0-110">Description</span></span>

<span data-ttu-id="a62f0-111">In Windows 7 haben wir die Optionen des UAC-Dialogfelds standardisiert.</span><span class="sxs-lookup"><span data-stu-id="a62f0-111">In Windows 7, we have standardized the UAC dialog box choices.</span></span> <span data-ttu-id="a62f0-112">Bisher mussten Benutzer aus mehreren Optionen auswählen, z. B. "Weiter", "Abbrechen" usw.</span><span class="sxs-lookup"><span data-stu-id="a62f0-112">Previously, users had to select from multiple options, for example, "Continue," "Cancel," and so on.</span></span> <span data-ttu-id="a62f0-113">Jetzt erhalten Benutzer in allen Dialogfeldern ein einfaches "Ja" oder "Nein".</span><span class="sxs-lookup"><span data-stu-id="a62f0-113">Now all dialog boxes give users a simple "Yes" or "No."</span></span> <span data-ttu-id="a62f0-114">Das Dialogfeldlayout zeigt nun auch den Programmnamen, Herausgeber und Ursprung deutlich an.</span><span class="sxs-lookup"><span data-stu-id="a62f0-114">The dialog layout now also clearly shows the program name, publisher, and origin.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="a62f0-115">Nutzen von Featurefunktionen</span><span class="sxs-lookup"><span data-stu-id="a62f0-115">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="a62f0-116">Die Anforderungen an die Anwendungsentwicklung in Windows 7 für UAC-Kompatibilität sind mit denen in Windows Vista identisch.</span><span class="sxs-lookup"><span data-stu-id="a62f0-116">The application development requirements in Windows 7 for UAC compatibility are the same as in Windows Vista.</span></span> <span data-ttu-id="a62f0-117">Windows Vista-kompatible Anwendungen interagieren ohne Änderungen mit der UAC in Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a62f0-117">Windows Vista-compatible applications will interact with UAC in Windows 7 without any modifications.</span></span> <span data-ttu-id="a62f0-118">Informationen dazu, wie Windows XP-Anwendungen unter Windows 7 ordnungsgemäß funktionieren, finden Sie in den Themen zur Benutzerkontensteuerung im Cookbook zur *Windows Vista-Anwendungskompatibilität.*</span><span class="sxs-lookup"><span data-stu-id="a62f0-118">See the User Account Control topics in the *Windows Vista Application Compatibility Cookbook* for information about how to make Windows XP applications work correctly on Windows 7.</span></span> <span data-ttu-id="a62f0-119">Die UAC-Verbesserungen für Windows 7 wirken sich zwar auf die Benutzerfreundlichkeit aus, wirken sich jedoch nicht auf die Anwendungsschnittstelle aus.</span><span class="sxs-lookup"><span data-stu-id="a62f0-119">While the UAC improvements for Windows 7 will impact the user's experience, they will not impact the application interface.</span></span> <span data-ttu-id="a62f0-120">Wenn jedoch Hilfeinhalte mit den UAC-Dialogen verknüpft sind, müssen Sie die Screenshots möglicherweise aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="a62f0-120">However, if there is any help content linked to the UAC dialogs, you may need to update the screenshots.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="a62f0-121">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a62f0-121">Links to Other Resources</span></span>

-   <span data-ttu-id="a62f0-122">[Cookbook zur Windows Vista-Anwendungskompatibilität](/previous-versions/bb757005(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a62f0-122">[Windows Vista Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10))</span></span>
-   [<span data-ttu-id="a62f0-123">Download des Anwendungskompatibilitätstoolkits</span><span class="sxs-lookup"><span data-stu-id="a62f0-123">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="a62f0-124">[Standardbenutzeranalyse](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="a62f0-124">[Standard User Analyzer](/previous-versions/windows/it-pro/windows-7/cc766021(v=ws.10))</span></span>

> [!Note]  
> <span data-ttu-id="a62f0-125">Diese Ressourcen sind in einigen Sprachen und Ländern/Regionen möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a62f0-125">These resources may not be available in some languages and countries/regions.</span></span>

 

 

 
