---
title: Iagentcharakteriex showPopupMenu
description: Iagentcharakteriex showPopupMenu
ms.assetid: f93c4c9e-5ef8-42d1-8f22-d6625af7978f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535a86496f3553e0927ebe67d2c9823b738fb901
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856479"
---
# <a name="iagentcharacterexshowpopupmenu"></a><span data-ttu-id="379f0-103">Iagentcharakteriex:: showPopupMenu</span><span class="sxs-lookup"><span data-stu-id="379f0-103">IAgentCharacterEx::ShowPopupMenu</span></span>

<span data-ttu-id="379f0-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="379f0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT ShowPopupMenu(
   short x,  // x-coordinate of pop-up menu
   short y   // y-coordinate of pop-up menu
);
```

<span data-ttu-id="379f0-105">Zeigt das Popup Menü für das Zeichen an.</span><span class="sxs-lookup"><span data-stu-id="379f0-105">Displays the pop-up menu for the character.</span></span>

-   <span data-ttu-id="379f0-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="379f0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="379f0-107"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="379f0-107"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="379f0-108">Die x-Koordinate des Popup Menüs des Zeichens in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="379f0-108">The x-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> <dt>

<span data-ttu-id="379f0-109"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="379f0-109"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="379f0-110">Die y-Koordinate des Popup Menüs des Zeichens in Pixel relativ zum Bildschirm Ursprung (oben links).</span><span class="sxs-lookup"><span data-stu-id="379f0-110">The y-coordinate of the character's pop-up menu in pixels, relative to the screen origin (upper left).</span></span>

</dd> </dl>

<span data-ttu-id="379f0-111">Wenn Sie [**iagentcharakteriex:: setautopopupmenu**](iagentcharacterex--setautopopupmenu.md) auf **false** festlegen, wird das Menü vom Server nicht mehr automatisch angezeigt, wenn mit der rechten Maustaste auf das Zeichen oder das zugehörige Symbol der Taskleiste geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="379f0-111">When you set [**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md) to **False**, the server no longer automatically displays the menu when the character or its taskbar icon is right-clicked.</span></span> <span data-ttu-id="379f0-112">Mit dieser Methode können Sie das Menü anzeigen.</span><span class="sxs-lookup"><span data-stu-id="379f0-112">You can use this method to display the menu.</span></span>

<span data-ttu-id="379f0-113">Das Menü wird angezeigt, bis der Benutzer einen Befehl auswählt oder ein anderes Menü anzeigt.</span><span class="sxs-lookup"><span data-stu-id="379f0-113">The menu displays until the user selects a command or displays another menu.</span></span> <span data-ttu-id="379f0-114">Es kann jeweils nur ein Popup Menü angezeigt werden. Daher wird durch Aufrufe dieser Methode das erste Menü abgebrochen (entfernt).</span><span class="sxs-lookup"><span data-stu-id="379f0-114">Only one pop-up menu can be displayed at a time; therefore, calls to this method will cancel (remove) the former menu.</span></span>

<span data-ttu-id="379f0-115">Diese Methode sollte nur aufgerufen werden, wenn die Client Anwendung der aktive Client des Zeichens ist. Andernfalls tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="379f0-115">This method should only be called when your client application is the active client of the character; otherwise it fails.</span></span>

[<span data-ttu-id="379f0-116">**Iagentcharakteriex:: abtautopopupmenu**</span><span class="sxs-lookup"><span data-stu-id="379f0-116">**IAgentCharacterEx::SetAutoPopupMenu**</span></span>](iagentcharacterex--setautopopupmenu.md)

 

 




