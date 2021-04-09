---
title: Modul 3. Windows-Grafiken
description: In Modul 1 dieser Reihe wurde gezeigt, wie ein leeres Fenster erstellt wird.
ms.assetid: 02416d36-519e-49bd-8a52-bd3afde2be34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bbe0e7afe882180a056f4c77d72de16df0ef943
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036564"
---
# <a name="module-3-windows-graphics"></a><span data-ttu-id="9288a-104">Modul 3.</span><span class="sxs-lookup"><span data-stu-id="9288a-104">Module 3.</span></span> <span data-ttu-id="9288a-105">Windows-Grafiken</span><span class="sxs-lookup"><span data-stu-id="9288a-105">Windows Graphics</span></span>

<span data-ttu-id="9288a-106">In [Modul 1](your-first-windows-program.md) dieser Reihe wurde gezeigt, wie ein leeres Fenster erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9288a-106">[Module 1](your-first-windows-program.md) of this series showed how to create a blank window.</span></span> <span data-ttu-id="9288a-107">[Modul 2](module-2--using-com-in-your-windows-program.md) hat einen geringfügigen Umweg durch den Component Object Model (com) gemacht, der die Grundlage für viele der modernen Windows-APIs ist.</span><span class="sxs-lookup"><span data-stu-id="9288a-107">[Module 2](module-2--using-com-in-your-windows-program.md) took a slight detour through the Component Object Model (COM), which is the foundation for many of the modern Windows APIs.</span></span> <span data-ttu-id="9288a-108">Nun ist es an der Zeit, dem leeren Fenster, das wir in Modul 1 erstellt haben, Grafiken hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9288a-108">Now it is time to add graphics to the blank window that we created in Module 1.</span></span>

<span data-ttu-id="9288a-109">Dieses Modul beginnt mit einem Überblick über die Windows-Grafik Architektur.</span><span class="sxs-lookup"><span data-stu-id="9288a-109">This module starts with a high-level overview of the Windows graphics architecture.</span></span> <span data-ttu-id="9288a-110">Wir betrachten dann Direct2D, eine leistungsstarke Grafik-API, die in Windows 7 eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="9288a-110">We then look at Direct2D, a powerful graphics API that was introduced in Windows 7.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9288a-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9288a-111">In this section</span></span>

-   [<span data-ttu-id="9288a-112">Übersicht über die Windows-Grafik Architektur</span><span class="sxs-lookup"><span data-stu-id="9288a-112">Overview of the Windows Graphics Architecture</span></span>](overview-of-the-windows-graphics-architecture.md)
-   [<span data-ttu-id="9288a-113">Der Desktopfenster-Manager</span><span class="sxs-lookup"><span data-stu-id="9288a-113">The Desktop Window Manager</span></span>](the-desktop-window-manager.md)
-   [<span data-ttu-id="9288a-114">Modus für beibehaltene Modus und unmittelbarer</span><span class="sxs-lookup"><span data-stu-id="9288a-114">Retained Mode Versus Immediate Mode</span></span>](retained-mode-versus-immediate-mode.md)
-   [<span data-ttu-id="9288a-115">Ihr erstes Direct2D-Programm</span><span class="sxs-lookup"><span data-stu-id="9288a-115">Your First Direct2D Program</span></span>](your-first-direct2d-program.md)
-   [<span data-ttu-id="9288a-116">Renderziele, Geräte und Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9288a-116">Render Targets, Devices, and Resources</span></span>](render-targets--devices--and-resources.md)
-   [<span data-ttu-id="9288a-117">Zeichnen mit Direct2D</span><span class="sxs-lookup"><span data-stu-id="9288a-117">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)
-   [<span data-ttu-id="9288a-118">DPI-und Device-Independent Pixel</span><span class="sxs-lookup"><span data-stu-id="9288a-118">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)
-   [<span data-ttu-id="9288a-119">Verwenden von Color in Direct2D</span><span class="sxs-lookup"><span data-stu-id="9288a-119">Using Color in Direct2D</span></span>](using-color-in-direct2d.md)
-   [<span data-ttu-id="9288a-120">Anwenden von Transformationen in Direct2D</span><span class="sxs-lookup"><span data-stu-id="9288a-120">Applying Transforms in Direct2D</span></span>](applying-transforms-in-direct2d.md)
-   [<span data-ttu-id="9288a-121">Anhang: Matrix Transformationen</span><span class="sxs-lookup"><span data-stu-id="9288a-121">Appendix: Matrix Transforms</span></span>](appendix--matrix-transforms.md)

## <a name="related-topics"></a><span data-ttu-id="9288a-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9288a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9288a-123">Erlernen Sie das Program mieren für Windows in C++</span><span class="sxs-lookup"><span data-stu-id="9288a-123">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 




