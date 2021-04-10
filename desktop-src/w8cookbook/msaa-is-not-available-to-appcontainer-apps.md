---
title: MSAA ist für Windows Store-Apps nicht verfügbar.
description: MSAA ist für Windows Store-Apps nicht verfügbar.
ms.assetid: C3C12BC7-7A0B-4859-93D0-AA78BC06E90B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e9c1221850b1fa97a3a0d5fcef119c21277486
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104039743"
---
# <a name="msaa-is-not-available-to-windows-store-apps"></a><span data-ttu-id="281f4-103">MSAA ist für Windows Store-Apps nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="281f4-103">MSAA is not available to Windows Store apps</span></span>

## <a name="platform"></a><span data-ttu-id="281f4-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="281f4-104">Platform</span></span>

<span data-ttu-id="281f4-105">**Clients** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="281f4-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="281f4-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="281f4-106">Description</span></span>

<span data-ttu-id="281f4-107">Windows 8 bietet keine Unterstützung für MSAA (Microsoft Active Accessibility) zum Lesen oder Automatisieren von verfügbaren Daten aus Windows Store-Apps.</span><span class="sxs-lookup"><span data-stu-id="281f4-107">Windows 8 does not support MSAA (Microsoft Active Accessibility) for reading or automating accessible data from Windows Store apps.</span></span> <span data-ttu-id="281f4-108">Die UIA-API (UI Automation), die seit Windows 7 verfügbar ist, sollte stattdessen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="281f4-108">The UI Automation (UIA) API, available since Windows 7, should be used instead.</span></span> <span data-ttu-id="281f4-109">Da keine Windows Store-App-Features vorhanden sind, sind keine Implementierungen vorhanden, die von dieser Änderung betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="281f4-109">Since there are no existing Windows Store app features, there are no existing implementations that are affected by this change.</span></span> <span data-ttu-id="281f4-110">Dies wirkt sich nur auf neue apps und Features aus, die für Windows 8 geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="281f4-110">This affects only new apps and features written for Windows 8.</span></span> <span data-ttu-id="281f4-111">Entwickler können weiterhin MSAA verwenden, um Ihre Barrierefreiheits Daten verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="281f4-111">Developers can still use MSAA to expose their accessibility data.</span></span> <span data-ttu-id="281f4-112">Wenn MSAA-Daten vom Windows Store-App-Anbieter bereitgestellt werden, sind UIA-Clients weiterhin in der Lage, die Daten zu lesen und zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="281f4-112">If MSAA data is provided by Windows Store app provider, UIA clients will still be able to read and automate the data.</span></span>

<span data-ttu-id="281f4-113">Um die API für Windows 8-Windows Store-Apps zu vereinfachen, haben wir entschieden, nur die Automatisierung der Benutzeroberfläche als Client für diese apps zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="281f4-113">To simplify the API for Windows 8Windows Store apps, we decided to support only UI Automation as a client for these apps.</span></span> <span data-ttu-id="281f4-114">UIA-Clients können UIA-Anbieter ohne Übersetzung nativ lesen.</span><span class="sxs-lookup"><span data-stu-id="281f4-114">UIA clients can read UIA providers natively, with no translation.</span></span> <span data-ttu-id="281f4-115">UIA-Clients können MSAA-Anbieter so lesen, dass Sie über den UIA-zu-MSAA-Proxy übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="281f4-115">UIA clients can read MSAA providers as translated through the UIA-to-MSAA Proxy.</span></span> <span data-ttu-id="281f4-116">Dadurch wird die Test Last für Windows Store-App-Entwickler reduziert.</span><span class="sxs-lookup"><span data-stu-id="281f4-116">This will reduce the testing burden for Windows Store app developers.</span></span>

<span data-ttu-id="281f4-117">Wenn Sie die Unterstützung für MSAA-Anbieter eliminieren, wird die Test Matrix weiter reduziert, aber es gibt wichtige apps, die weiterhin auf einem MSAA basieren und nicht auf Sie zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="281f4-117">Eliminating support for MSAA providers would further reduce the testing matrix, but there are major apps that are still MSAA-based and we do not want to render them inaccessible.</span></span>

## <a name="manifestation"></a><span data-ttu-id="281f4-118">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="281f4-118">Manifestation</span></span>

<span data-ttu-id="281f4-119">Entwickler von Windows Store-Apps sind nicht in der Lage, auf die Details von MSAA innerhalb des App-Modells zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="281f4-119">Windows Store app developers will not be able to access the details of MSAA within the app model.</span></span>

## <a name="solution"></a><span data-ttu-id="281f4-120">Lösung</span><span class="sxs-lookup"><span data-stu-id="281f4-120">Solution</span></span>

<span data-ttu-id="281f4-121">In MSAA sollten für Features von Windows Store-Apps keine neuen automatisierten Fälle erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="281f4-121">No new automated cases should be authored in MSAA for features of Windows Store apps.</span></span>

<span data-ttu-id="281f4-122">Wechseln Sie alle vorhandenen in-Box-Tools, die MSAA verwenden, zu UIA, wenn Sie mit Windows Store-Apps interagieren müssen.</span><span class="sxs-lookup"><span data-stu-id="281f4-122">Switch any existing in-box tools that use MSAA to UIA if they need to interact with Windows Store apps.</span></span> <span data-ttu-id="281f4-123">Entwickler von Windows Store-Apps sollten die Benutzeroberflächenautomatisierungs-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="281f4-123">Windows Store app developers should use the UI Automation API.</span></span>

## <a name="resources"></a><span data-ttu-id="281f4-124">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="281f4-124">Resources</span></span>

-   [<span data-ttu-id="281f4-125">Grundlagen der Benutzeroberflächenautomatisierung</span><span class="sxs-lookup"><span data-stu-id="281f4-125">UI Automation Fundamentals</span></span>](../winauto/entry-uiauto-win32.md)

 

 