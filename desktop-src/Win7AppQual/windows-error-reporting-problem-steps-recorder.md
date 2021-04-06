---
description: .
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Windows-Fehlerberichterstattung Problem Aufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25fb70acef867b878063bd6011fde6867f7f0e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759786"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a><span data-ttu-id="bb80f-103">Windows-Fehlerberichterstattung Problem Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="bb80f-103">Windows Error Reporting Problem Steps Recorder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="bb80f-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="bb80f-104">Affected Platforms</span></span>

<span data-ttu-id="bb80f-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb80f-105">**Clients** – Windows 7</span></span>  
<span data-ttu-id="bb80f-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb80f-106">**Servers** – Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="bb80f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bb80f-107">Description</span></span>

<span data-ttu-id="bb80f-108">Vor Windows 7 wurden von Windows-Fehlerberichterstattung (wer) Fehlerberichte erfasst, die auf Probleme bei der Reparatur hinweisen.</span><span class="sxs-lookup"><span data-stu-id="bb80f-108">Prior to Windows 7, Windows Error Reporting (WER) collected error reports that indicated problems in need of repair.</span></span> <span data-ttu-id="bb80f-109">Diese Fehlerberichte enthalten hilfreiche Informationen, die die allgemeine Art eines Problems beschreiben, jedoch nicht genügend Informationen, um die Grundursache zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="bb80f-109">These error reports contain helpful information that describes the general nature of a problem, but not enough information to determine its root cause.</span></span> <span data-ttu-id="bb80f-110">Dafür benötigen Entwickler ein Tool, um das Absturz-/stillstandzenario für das Debuggen zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="bb80f-110">For that, developers need a tool to reproduce the crash/hang scenario for debugging.</span></span>

<span data-ttu-id="bb80f-111">Eine neue Anwendung, Problem Schritte Recorder (PSR.exe), wird auf allen Builds von Windows 7 ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="bb80f-111">A new application, Problem Steps Recorder (PSR.exe), is shipping on all builds of Windows 7.</span></span> <span data-ttu-id="bb80f-112">Diese Funktion ermöglicht das Sammeln von Aktionen, die von einem Benutzer ausgeführt werden, während ein Absturz auftritt, sodass Tester und Entwickler die Situation für Analyse und Debuggen reproduzieren können.</span><span class="sxs-lookup"><span data-stu-id="bb80f-112">This feature enables the collection of the actions performed by a user while encountering a crash so that testers and developers can reproduce the situation for analysis and debugging.</span></span>

## <a name="usage"></a><span data-ttu-id="bb80f-113">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="bb80f-113">Usage</span></span>

<span data-ttu-id="bb80f-114">Derzeit muss ein Windows-Fehlerberichterstattung Service-Entwickler PSR-Aktivierung für eine Anwendung anfordern. Microsoft-Support Organisationen verwenden dieses Tool auch bei der Problembehandlung mit Endbenutzern.</span><span class="sxs-lookup"><span data-stu-id="bb80f-114">Currently, a Windows Error Reporting service developer must request PSR enablement for an application; Microsoft support organizations also use this tool while troubleshooting with end users.</span></span> <span data-ttu-id="bb80f-115">Pläne sind vorhanden, um PSR nach der Veröffentlichung von Windows 7 unter Windows Quality Online Services (Winqual) verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="bb80f-115">Plans are in place to make PSR available at Windows Quality Online Services (Winqual) after the release of Windows 7.</span></span>

<span data-ttu-id="bb80f-116">**Hinweis:** Wenn PSR für eine Anwendung aktiviert ist, kann es bei der Anwendung zu Leistungseinbußen kommen.</span><span class="sxs-lookup"><span data-stu-id="bb80f-116">**Note:** With PSR enabled for an application, the application may see some performance degradation.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="bb80f-117">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="bb80f-117">Links to Other Resources</span></span>

-   [<span data-ttu-id="bb80f-118">Blogeintrag Windows-Fehlerberichterstattung</span><span class="sxs-lookup"><span data-stu-id="bb80f-118">Windows Error Reporting blog entry</span></span>](/archive/blogs/wer/)
-   [<span data-ttu-id="bb80f-119">Windows Quality Online Services (Winqual)</span><span class="sxs-lookup"><span data-stu-id="bb80f-119">Windows Quality Online Services (Winqual)</span></span>](https://winqual.microsoft.com)

 

 
