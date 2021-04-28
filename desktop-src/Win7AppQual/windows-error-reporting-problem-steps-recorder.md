---
description: Windows-Fehlerberichterstattung Problemaufzeichnung
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Windows-Fehlerberichterstattung Problemaufzeichnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46abb8adf545152e34c2b2100022068291e3571f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084158"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a><span data-ttu-id="a9b28-103">Windows-Fehlerberichterstattung Problemaufzeichnung</span><span class="sxs-lookup"><span data-stu-id="a9b28-103">Windows Error Reporting Problem Steps Recorder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="a9b28-104">Betroffene Plattformen</span><span class="sxs-lookup"><span data-stu-id="a9b28-104">Affected Platforms</span></span>

<span data-ttu-id="a9b28-105">**Clients** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9b28-105">**Clients** – Windows 7</span></span>  
<span data-ttu-id="a9b28-106">**Server** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a9b28-106">**Servers** – Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="a9b28-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a9b28-107">Description</span></span>

<span data-ttu-id="a9b28-108">Vor Windows 7 hat Windows-Fehlerberichterstattung (WER) Fehlerberichte gesammelt, die auf Reparaturprobleme hindeuteten.</span><span class="sxs-lookup"><span data-stu-id="a9b28-108">Prior to Windows 7, Windows Error Reporting (WER) collected error reports that indicated problems in need of repair.</span></span> <span data-ttu-id="a9b28-109">Diese Fehlerberichte enthalten hilfreiche Informationen, die die allgemeine Natur eines Problems beschreiben, aber nicht genügend Informationen, um die Grundursache zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a9b28-109">These error reports contain helpful information that describes the general nature of a problem, but not enough information to determine its root cause.</span></span> <span data-ttu-id="a9b28-110">Dafür benötigen Entwickler ein Tool, um das Absturz-/Hängen-Szenario für das Debuggen zu reproduzieren.</span><span class="sxs-lookup"><span data-stu-id="a9b28-110">For that, developers need a tool to reproduce the crash/hang scenario for debugging.</span></span>

<span data-ttu-id="a9b28-111">Eine neue Anwendung, Problemaufzeichnung (PSR.exe), wird für alle Builds von Windows 7 veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="a9b28-111">A new application, Problem Steps Recorder (PSR.exe), is shipping on all builds of Windows 7.</span></span> <span data-ttu-id="a9b28-112">Dieses Feature ermöglicht das Sammeln der Aktionen, die von einem Benutzer bei einem Absturz ausgeführt werden, damit Tester und Entwickler die Situation für Analyse und Debuggen reproduzieren können.</span><span class="sxs-lookup"><span data-stu-id="a9b28-112">This feature enables the collection of the actions performed by a user while encountering a crash so that testers and developers can reproduce the situation for analysis and debugging.</span></span>

## <a name="usage"></a><span data-ttu-id="a9b28-113">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="a9b28-113">Usage</span></span>

<span data-ttu-id="a9b28-114">Derzeit muss ein Windows-Fehlerberichterstattung-Dienstentwickler die PSR-Aktivierung für eine Anwendung anfordern. Microsoft-Supportorganisationen verwenden dieses Tool auch bei der Problembehandlung mit Endbenutzern.</span><span class="sxs-lookup"><span data-stu-id="a9b28-114">Currently, a Windows Error Reporting service developer must request PSR enablement for an application; Microsoft support organizations also use this tool while troubleshooting with end users.</span></span> <span data-ttu-id="a9b28-115">Es sind Pläne vorhanden, um PSR nach der Veröffentlichung von Windows 7 unter Windows Quality Online Services (Winqual) verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="a9b28-115">Plans are in place to make PSR available at Windows Quality Online Services (Winqual) after the release of Windows 7.</span></span>

<span data-ttu-id="a9b28-116">**Hinweis:** Wenn PSR für eine Anwendung aktiviert ist, kann es für die Anwendung zu Leistungseinbußen führen.</span><span class="sxs-lookup"><span data-stu-id="a9b28-116">**Note:** With PSR enabled for an application, the application may see some performance degradation.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="a9b28-117">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a9b28-117">Links to Other Resources</span></span>

-   [<span data-ttu-id="a9b28-118">Windows-Fehlerberichterstattung Blogeintrag</span><span class="sxs-lookup"><span data-stu-id="a9b28-118">Windows Error Reporting blog entry</span></span>](/archive/blogs/wer/)
-   [<span data-ttu-id="a9b28-119">Windows Quality Online Services (Winqual)</span><span class="sxs-lookup"><span data-stu-id="a9b28-119">Windows Quality Online Services (Winqual)</span></span>](https://winqual.microsoft.com)

 

 
