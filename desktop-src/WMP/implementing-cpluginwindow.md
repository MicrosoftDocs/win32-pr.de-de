---
title: Implementieren von cpluginwindow
description: Implementieren von cpluginwindow
ms.assetid: b22723ce-f373-43b1-a098-86a8dbcf485e
keywords:
- Windows Media Player-Plug-ins, cpluginwindow-Klasse
- Plug-ins, cpluginwindow-Klasse
- Benutzeroberflächen-Plug-ins, cpluginwindow-Klasse
- UI-Plug-ins, cpluginwindow-Klasse
- Cpluginwindow-Klasse
- Programmier Handbuch, Benutzerschnittstellen-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe282b0c6cefbcac8fbce76ca53f8e0efaf64874
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709072"
---
# <a name="implementing-cpluginwindow"></a><span data-ttu-id="d98ff-109">Implementieren von cpluginwindow</span><span class="sxs-lookup"><span data-stu-id="d98ff-109">Implementing CPluginWindow</span></span>

<span data-ttu-id="d98ff-110">Die cpluginwindow-Klasse stellt die Benutzeroberfläche für das Plug-in bereit.</span><span class="sxs-lookup"><span data-stu-id="d98ff-110">The CPluginWindow class provides the UI to the plug-in.</span></span> <span data-ttu-id="d98ff-111">Im Fall des Such Benutzeroberflächen-Plug-Ins enthält diese Klasse den Code für die **Such** Schaltfläche und den Code, mit dem die Suchseite gestartet wird, wenn auf die Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="d98ff-111">In the case of the Search UI plug-in, this class contains the code for the **Search** button and the code that launches the search page when the button is clicked.</span></span>

<span data-ttu-id="d98ff-112">Der Assistent stellt eine grundlegende Implementierung von cpluginwindow in der Header Datei "cpluginwindow. h" bereit.</span><span class="sxs-lookup"><span data-stu-id="d98ff-112">The wizard provides a basic implementation of CPluginWindow in the CPluginWindow.h header file.</span></span> <span data-ttu-id="d98ff-113">Um dies zu gewährleisten, ändert das Such Benutzeroberflächen-Plug-in diese Datei direkt, obwohl umfassende Ergänzungen normalerweise in einer separaten cpluginwindow. cpp-Datei platziert werden.</span><span class="sxs-lookup"><span data-stu-id="d98ff-113">To keep things simple, the Search UI plug-in will modify this file directly, although extensive additions would normally be placed in a separate CPluginWindow.cpp file.</span></span>

<span data-ttu-id="d98ff-114">In den folgenden Abschnitten wird beschrieben, was Sie tun müssen, um cpluginwindow zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="d98ff-114">The following sections describe what you need to do to implement CPluginWindow:</span></span>

-   [<span data-ttu-id="d98ff-115">Die Meldungs Zuordnung</span><span class="sxs-lookup"><span data-stu-id="d98ff-115">The Message Map</span></span>](the-message-map.md)
-   [<span data-ttu-id="d98ff-116">Der Konstruktor</span><span class="sxs-lookup"><span data-stu-id="d98ff-116">The Constructor</span></span>](the-constructor.md)
-   [<span data-ttu-id="d98ff-117">Die OnPaint-Methode</span><span class="sxs-lookup"><span data-stu-id="d98ff-117">The OnPaint Method</span></span>](the-onpaint-method.md)
-   [<span data-ttu-id="d98ff-118">Die OnCreate-Methode</span><span class="sxs-lookup"><span data-stu-id="d98ff-118">The OnCreate Method</span></span>](the-oncreate-method.md)
-   [<span data-ttu-id="d98ff-119">Die onSearch-Methode</span><span class="sxs-lookup"><span data-stu-id="d98ff-119">The OnSearch Method</span></span>](the-onsearch-method.md)
-   [<span data-ttu-id="d98ff-120">Die LaunchPage-Methode</span><span class="sxs-lookup"><span data-stu-id="d98ff-120">The LaunchPage Method</span></span>](the-launchpage-method.md)

## <a name="related-topics"></a><span data-ttu-id="d98ff-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d98ff-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d98ff-122">**Programmier Handbuch für Benutzeroberflächen-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="d98ff-122">**User Interface Plug-ins Programming Guide**</span></span>](user-interface-plug-ins-programming-guide.md)
</dt> </dl>

 

 




