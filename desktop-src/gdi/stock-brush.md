---
description: Von der Graphics Device Interface (GDI) werden sieben vordefinierte logische Aktien Pinsel verwaltet. Es gibt auch 21 vordefinierte logische Aktien Pinsel, die von der Fenster Verwaltungsschnittstelle (User) verwaltet werden.
ms.assetid: ddbc6d54-47f6-4810-9d3a-feede80f2bed
title: Aktien Pinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522337752c2d81a92302d4a6a8f025393db1ce15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980528"
---
# <a name="stock-brush"></a><span data-ttu-id="65448-104">Aktien Pinsel</span><span class="sxs-lookup"><span data-stu-id="65448-104">Stock Brush</span></span>

<span data-ttu-id="65448-105">Von der Graphics Device Interface (GDI) werden sieben vordefinierte logische Aktien Pinsel verwaltet.</span><span class="sxs-lookup"><span data-stu-id="65448-105">There are seven predefined logical stock brushes maintained by the graphics device interface (GDI).</span></span> <span data-ttu-id="65448-106">Es gibt auch 21 vordefinierte logische Aktien Pinsel, die von der Fenster Verwaltungsschnittstelle (User) verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="65448-106">There are also 21 predefined logical stock brushes maintained by the window management interface (USER).</span></span>

<span data-ttu-id="65448-107">Die folgende Abbildung zeigt Rechtecke, die mithilfe der sieben vordefinierten Aktien Pinsel gezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="65448-107">The following illustration shows rectangles painted by using the seven predefined stock brushes.</span></span>

![Abbildung, die sieben Felder anzeigt: ein schwarzer, drei graue Schattierungen und drei, die leer erscheinen](images/csbru-03.png)

<span data-ttu-id="65448-109">Eine Anwendung kann ein Handle abrufen, das einen der sieben Aktien Pinsel durch Aufrufen der [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) -Funktion identifiziert, wobei der pinkentyp angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="65448-109">An application can retrieve a handle identifying one of the seven stock brushes by calling the [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function, specifying the brush type.</span></span>

<span data-ttu-id="65448-110">Die 21 Stock-Pinsel, die von der Fenster Verwaltungsschnittstelle verwaltet werden, entsprechen den Farben von Fensterelementen, z. b. Menüs, Scrollleisten und Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="65448-110">The 21 stock brushes maintained by the window management interface correspond to the colors of window elements such as menus, scroll bars, and buttons.</span></span> <span data-ttu-id="65448-111">Eine Anwendung kann ein Handle abrufen, das einen dieser Pinsel identifiziert, indem Sie die [**getsyscolorbrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) -Funktion aufruft und einen System Farbwert angibt.</span><span class="sxs-lookup"><span data-stu-id="65448-111">An application can obtain a handle identifying one of these brushes by calling the [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush) function and specifying a system-color value.</span></span> <span data-ttu-id="65448-112">Eine Anwendung kann die Farbe, die einem bestimmten Fensterelement entspricht, abrufen, indem die [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) -Funktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="65448-112">An application can retrieve the color corresponding to a particular window element by calling the [**GetSysColor**](/windows/win32/api/winuser/nf-winuser-getsyscolor) function.</span></span> <span data-ttu-id="65448-113">Eine Anwendung kann die Farbe, die einem Window-Element entspricht, durch Aufrufen der [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) -Funktion festlegen.</span><span class="sxs-lookup"><span data-stu-id="65448-113">An application can set the color corresponding to a window element by calling the [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) function.</span></span>

 

 
