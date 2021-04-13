---
title: Verwenden von Geräte Kontexten
description: Verwenden von Geräte Kontexten
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- Visualisierungen, Gerätekontext
- benutzerdefinierte Visualisierungen, Gerätekontext
- Visualisierungen, Rendering-Funktion
- benutzerdefinierte Visualisierungen, Rendering-Funktion
- Funktion "Rendering", Gerätekontext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c315d5004565644750f4adcd099fc165e81575
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310308"
---
# <a name="using-device-contexts"></a><span data-ttu-id="91d89-108">Verwenden von Geräte Kontexten</span><span class="sxs-lookup"><span data-stu-id="91d89-108">Using Device Contexts</span></span>

<span data-ttu-id="91d89-109">Der Gerätekontext ist ein Standard Handle für einen Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="91d89-109">The device context is a standard handle to a device context.</span></span> <span data-ttu-id="91d89-110">Sie benötigen dies für viele Zeichnungsfunktionen, damit Microsoft Windows weiß, welches Fenster gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="91d89-110">You need this for many drawing functions so that Microsoft Windows knows which window to draw in.</span></span> <span data-ttu-id="91d89-111">Um z. b. ein Rechteck zu zeichnen, müssen Sie den Gerätekontext angeben.</span><span class="sxs-lookup"><span data-stu-id="91d89-111">For example, to draw a rectangle, you need to specify the device context.</span></span>


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



<span data-ttu-id="91d89-112">Der Gerätekontext wird durch die Funktion " **Rendering** " von Windows Media Player angegeben.</span><span class="sxs-lookup"><span data-stu-id="91d89-112">The device context is specified by Windows Media Player through the **Render** function.</span></span> <span data-ttu-id="91d89-113">Wenn das Plug-in mithilfe eines Fensters gerendert wird, müssen Sie den Gerätekontext dieses Fensters verwenden.</span><span class="sxs-lookup"><span data-stu-id="91d89-113">If your plug-in renders using a window, you'll need to use the device context of that window.</span></span> <span data-ttu-id="91d89-114">Verwenden Sie diesen Gerätekontext für ein beliebiges Zeichnungs Tool, das einen Gerätekontext erfordert.</span><span class="sxs-lookup"><span data-stu-id="91d89-114">Use this device context for any drawing tool that requires a device context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91d89-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="91d89-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91d89-116">**Implementieren von Rendering**</span><span class="sxs-lookup"><span data-stu-id="91d89-116">**Implementing Render**</span></span>](implementing-render.md)
</dt> </dl>

 

 




