---
title: Hohe dpi-Informationen für Desktop-Apps in Windows 8.1
description: Hohe dpi-Informationen für Desktop-Apps in Windows 8.1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341732"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a><span data-ttu-id="690a8-103">Hohe dpi-Informationen für Desktop-Apps in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="690a8-103">High DPI for desktop apps in Windows 8.1</span></span>

## <a name="platforms"></a><span data-ttu-id="690a8-104">Plattformen</span><span class="sxs-lookup"><span data-stu-id="690a8-104">Platforms</span></span>

<dl> <span data-ttu-id="690a8-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="690a8-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="690a8-106">Server-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="690a8-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="690a8-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="690a8-107">Description</span></span>

<span data-ttu-id="690a8-108">In Windows 8.1 die Windows-Desktop Anwendungen zusätzlich zu den in Windows 8 unterstützten Skalierungen 200 von 100%, 125% und 150% ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="690a8-108">In Windows 8.1 desktop applications are expected to run on displays with 200% scaling in addition to the 100%, 125%, and 150% scaling that is supported in Windows 8.</span></span> <span data-ttu-id="690a8-109">Außerdem werden Desktop Anwendungen pro Monitor skaliert und nicht in einem einzelnen Skalierungsfaktor, der auf alle anzeigen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="690a8-109">In addition, desktop applications are scaled on a per-monitor basis rather than to a single scale factor applied to all displays.</span></span> <span data-ttu-id="690a8-110">Entwickler können auch neue APIs in Windows 8.1 anrufen, um Skalierungsfaktoren pro Monitor zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="690a8-110">Developers can also call new APIs in Windows 8.1 to get per-monitor scale factors.</span></span>

## <a name="manifestations"></a><span data-ttu-id="690a8-111">Kundgebungen</span><span class="sxs-lookup"><span data-stu-id="690a8-111">Manifestations</span></span>

<span data-ttu-id="690a8-112">Benutzer können neue High Density-Anzeige mit Windows 8.1 für eine fantastische visuelle Darstellung verwenden, die die höheren Pixeldaten nutzt.</span><span class="sxs-lookup"><span data-stu-id="690a8-112">Users can use new high density displays with Windows 8.1 for a terrific visual experience that takes advantage of the higher pixel data.</span></span> <span data-ttu-id="690a8-113">Wenn Anwendungen keine hohen DPI-Werte verarbeiten, werden Sie von Windows für den Benutzer skaliert.</span><span class="sxs-lookup"><span data-stu-id="690a8-113">If applications don’t handle high DPI, Windows will scale them for the user.</span></span> <span data-ttu-id="690a8-114">Außerdem können Benutzer eine Mischung aus hoher und niedriger Dichte auf demselben Computer verwenden, und Windows skaliert Inhalt für jede Anzeige entsprechend.</span><span class="sxs-lookup"><span data-stu-id="690a8-114">In addition, users can use a mix of high and low density displays on the same computer, and Windows will scale content appropriately for each display.</span></span> <span data-ttu-id="690a8-115">Dies ist eine Verbesserung gegenüber Windows 8, bei der Inhalte für einige anzeigen zu groß sein können.</span><span class="sxs-lookup"><span data-stu-id="690a8-115">This is an improvement over Windows 8, where content can be too large on some displays.</span></span>

## <a name="mitigation"></a><span data-ttu-id="690a8-116">Minderung</span><span class="sxs-lookup"><span data-stu-id="690a8-116">Mitigation</span></span>

<span data-ttu-id="690a8-117">Da Windows apps skaliert, die sich nicht selbst skalieren lassen, müssen Entwickler in der Regel keine zusätzlichen Aufgaben erledigen, aber Entwickler, die in das Schreiben von Anwendungen investieren, die High dpi unterstützen, haben einen Wettbewerbsvorteil, da diese Anwendungen auf neuen Hochleistungs-Laptops und Desktop Monitoren besser aussehen werden.</span><span class="sxs-lookup"><span data-stu-id="690a8-117">Since Windows will scale apps that don’t scale themselves, developers generally do not have to do additional work, but developers who do invest in writing applications that support high DPI will have a competitive advantage, as those applications will look better on new high DPI laptops and desktop monitors.</span></span>

## <a name="solution"></a><span data-ttu-id="690a8-118">Lösung</span><span class="sxs-lookup"><span data-stu-id="690a8-118">Solution</span></span>

<span data-ttu-id="690a8-119">Eine Anwendung, die hohe dpi-Schritte nutzen kann, ist eine komplexe Entwurfs-und Implementierungs Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="690a8-119">Making an application that can take advantage of high DPI is a complex design and implementation task.</span></span> <span data-ttu-id="690a8-120">Unter den Links unten finden Sie Lernprogramm Informationen, Inhalte der buildpräsentation und ähnliche Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="690a8-120">See the links below for tutorial information, BUILD presentation content, and similar support.</span></span>

## <a name="tests"></a><span data-ttu-id="690a8-121">Tests</span><span class="sxs-lookup"><span data-stu-id="690a8-121">Tests</span></span>

<span data-ttu-id="690a8-122">Selbst wenn Entwickler ihre Anwendungen nicht für hohe dpi-Vorgänge nutzen, sollten Sie Ihre Anwendung bei 100%, 125%, 150% und der Skalierung von 200% testen, um sicherzustellen, dass die Endbenutzer Leistung zufriedenstellend und wettbewerbsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="690a8-122">Even if developers do not choose to make their applications take advantage of high DPI, they should test their application at 100%, 125%, 150%, and 200% scaling to be sure the end-user experience is satisfactory and competitive.</span></span>

## <a name="resources"></a><span data-ttu-id="690a8-123">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="690a8-123">Resources</span></span>

-   [<span data-ttu-id="690a8-124">Whitepaper und Tutorial zu hohen dpi-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="690a8-124">White paper and tutorial on high DPI in Windows 8.1</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [<span data-ttu-id="690a8-125">Windows-Desktop-Beispiel Programme</span><span class="sxs-lookup"><span data-stu-id="690a8-125">Windows desktop sample programs</span></span>](https://www.microsoft.com/?ref=go)
-   [<span data-ttu-id="690a8-126">Build 2013-Break-out-Sitzung mit hoher dpi in Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="690a8-126">BUILD 2013 break-out session on high DPI in Windows 8.1</span></span>](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 