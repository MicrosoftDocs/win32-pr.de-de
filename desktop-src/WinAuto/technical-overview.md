---
title: Technischer Überblick
description: Microsoft Active Accessibility verbessert die Art und Weise, wie Barrierefreiheits Hilfen (spezialisierte Programme, die Menschen mit Behinderungen helfen, die Computer effektiver verwenden) mit Anwendungen arbeiten, die unter Microsoft Windows ausgeführt werden.
ms.assetid: d71ef40e-4c58-4ee6-8909-04ff4f8d20d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69f3931c6a69e9b8caed849942424039178a7884
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712947"
---
# <a name="technical-overview"></a><span data-ttu-id="250fb-103">Technischer Überblick</span><span class="sxs-lookup"><span data-stu-id="250fb-103">Technical Overview</span></span>

<span data-ttu-id="250fb-104">Microsoft Active Accessibility verbessert die Art und Weise, wie Barrierefreiheits Hilfen (spezialisierte Programme, die Menschen mit Behinderungen helfen, die Computer effektiver verwenden) mit Anwendungen arbeiten, die unter Microsoft Windows ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="250fb-104">Microsoft Active Accessibility improves the way accessibility aids (specialized programs that help people with disabilities use computers more effectively) work with applications running on Microsoft Windows.</span></span>

<span data-ttu-id="250fb-105">Microsoft Active Accessibility basiert auf der von Microsoft entwickelten Component Object Model (com) und ist ein Industriestandard, der eine gängige Methode für die Kommunikation von Anwendungen und Betriebssystemen definiert.</span><span class="sxs-lookup"><span data-stu-id="250fb-105">Microsoft Active Accessibility is based on the Component Object Model (COM), which was developed by Microsoft and is an industry standard that defines a common way for applications and operating systems to communicate.</span></span> <span data-ttu-id="250fb-106">Microsoft Active Accessibility besteht aus den folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="250fb-106">Microsoft Active Accessibility consists of the following components:</span></span>

-   <span data-ttu-id="250fb-107">Die COM-Schnittstelle [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), die Informationen über Benutzeroberflächen Elemente verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="250fb-107">The COM interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), which exposes information about UI elements.</span></span> <span data-ttu-id="250fb-108">**IAccessible** verfügt auch über Eigenschaften und Methoden zum Abrufen von Informationen über und zum Bearbeiten dieses Benutzeroberflächen Elements.</span><span class="sxs-lookup"><span data-stu-id="250fb-108">**IAccessible** also has properties and methods for obtaining information about and manipulating that UI element.</span></span>
-   <span data-ttu-id="250fb-109">WinEvents, ein Ereignis System, mit dem Server Clients benachrichtigen können, wenn ein Barrierefreies Objekt geändert wird.</span><span class="sxs-lookup"><span data-stu-id="250fb-109">WinEvents, an event system that allows servers to notify clients when an accessible object changes.</span></span>
-   <span data-ttu-id="250fb-110">Oleacc.dll, eine Support-oder Lauf Zeit-dll.</span><span class="sxs-lookup"><span data-stu-id="250fb-110">Oleacc.dll, a support or run-time DLL.</span></span>

<span data-ttu-id="250fb-111">Die Microsoft Active Accessibility-dll, Oleacc.dll, besteht aus den folgenden Komponenten:</span><span class="sxs-lookup"><span data-stu-id="250fb-111">The Microsoft Active Accessibility DLL, Oleacc.dll, consists of the following components:</span></span>

-   <span data-ttu-id="250fb-112">Funktionen, die es Clients ermöglichen, einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger anzufordern (z. b. [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span><span class="sxs-lookup"><span data-stu-id="250fb-112">Functions that allow clients to request an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer (for example, [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)).</span></span>
-   <span data-ttu-id="250fb-113">Funktionen, mit denen Server einen [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger an einen Client (z. [**b. lresultfromuject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)) zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="250fb-113">Functions that allow servers to return an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer to a client (for example, [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)).</span></span>
-   <span data-ttu-id="250fb-114">Funktionen zum erhalten von lokalisiertem Text für die Rollen-und Statuscodes (z. b. [**getroletext**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) und [**getstatetext**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span><span class="sxs-lookup"><span data-stu-id="250fb-114">Functions for getting localized text for the role and state codes (for example, [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) and [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)).</span></span>
-   <span data-ttu-id="250fb-115">Einige Hilfsfunktionen ([**accessiblechildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span><span class="sxs-lookup"><span data-stu-id="250fb-115">Some helper functions ([**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)).</span></span>
-   <span data-ttu-id="250fb-116">Code, der die Standard Implementierung von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für Standardbenutzer-und COMCTL-Steuerelemente bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="250fb-116">Code that provides the default implementation of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) for standard USER and COMCTL controls.</span></span> <span data-ttu-id="250fb-117">Da diese im Namen der System Steuerelemente **IAccessible** implementieren, werden *Sie als* Proxys bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="250fb-117">Because these implement **IAccessible** on behalf of the system controls, they are known as *proxies*.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="250fb-118">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="250fb-118">In this section</span></span>

-   [<span data-ttu-id="250fb-119">Funktionsweise von Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="250fb-119">How Active Accessibility Works</span></span>](how-active-accessibility-works.md)
-   [<span data-ttu-id="250fb-120">Grundlagen zu Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="250fb-120">Active Accessibility Basics</span></span>](active-accessibility-basics.md)
-   [<span data-ttu-id="250fb-121">Server Richtlinien</span><span class="sxs-lookup"><span data-stu-id="250fb-121">Server Guidelines</span></span>](server-guidelines.md)
-   [<span data-ttu-id="250fb-122">Client Richtlinien</span><span class="sxs-lookup"><span data-stu-id="250fb-122">Client Guidelines</span></span>](client-guidelines.md)
-   [<span data-ttu-id="250fb-123">COM-und Unicode-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="250fb-123">COM and Unicode Guidelines</span></span>](com-and-unicode-guidelines.md)

 

 




