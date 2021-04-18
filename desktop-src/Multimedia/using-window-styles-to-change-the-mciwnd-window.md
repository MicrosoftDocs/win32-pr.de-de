---
title: Ändern des mciwnd-Fensters mithilfe von Fenster Stilen
description: Ändern des mciwnd-Fensters mithilfe von Fenster Stilen
ms.assetid: 85851c37-e3d3-45f8-9c0a-0e1392c414af
keywords:
- Mciwndcreate-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bef1471c4da280540b5b08ed43704b73a6b16f6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337840"
---
# <a name="using-window-styles-to-change-the-mciwnd-window"></a><span data-ttu-id="721f5-104">Ändern des mciwnd-Fensters mithilfe von Fenster Stilen</span><span class="sxs-lookup"><span data-stu-id="721f5-104">Using Window Styles to Change the MCIWnd Window</span></span>

<span data-ttu-id="721f5-105">Wie bei jedem beliebigen Fenster können Sie die Darstellung und das Verhalten eines mciwnd-Fensters ändern, indem Sie aus den Standardfenster Stilen auswählen, die mit der Funktion "up [Window](/windows/win32/api/winuser/nf-winuser-createwindowa) " angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="721f5-105">As with any window, you can change the appearance and behavior of an MCIWnd window by choosing from the standard window styles specified with the [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) function.</span></span> <span data-ttu-id="721f5-106">Darüber hinaus können Sie aus verschiedenen anderen Fenster Stilen auswählen, die für mciwnd-Fenster spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="721f5-106">In addition, you can choose from several other window styles that are specific to MCIWnd windows.</span></span> <span data-ttu-id="721f5-107">Diese Formate können von Ihrer Anwendung auf folgende Weise geändert werden:</span><span class="sxs-lookup"><span data-stu-id="721f5-107">With these styles, your application can change these MCIWnd windows in the following ways:</span></span>

-   <span data-ttu-id="721f5-108">Ändern Sie die Fenstergröße.</span><span class="sxs-lookup"><span data-stu-id="721f5-108">Change window size.</span></span>
-   <span data-ttu-id="721f5-109">Ausblenden oder Anzeigen von Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="721f5-109">Hide or display controls.</span></span>
-   <span data-ttu-id="721f5-110">Ausgeben von Benachrichtigungs Meldungen.</span><span class="sxs-lookup"><span data-stu-id="721f5-110">Issue notification messages.</span></span>
-   <span data-ttu-id="721f5-111">Anzeigen von Informationen in der Titelleiste.</span><span class="sxs-lookup"><span data-stu-id="721f5-111">Display information in the title bar.</span></span>

<span data-ttu-id="721f5-112">Sie können Fenster Stile festlegen, indem Sie Sie in der [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) -Funktion angeben, oder Sie können das [**mciwndchangestyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) -Makro verwenden, um den Stil eines vorhandenen mciwnd-Fensters zu ändern.</span><span class="sxs-lookup"><span data-stu-id="721f5-112">You can set window styles by specifying them in the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function, or you can use the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro to change the style of an existing MCIWnd window.</span></span> <span data-ttu-id="721f5-113">Sie können auch ein mciwnd-Fenster für seine aktuellen Stile Abfragen, indem Sie das [**mciwndgetstyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="721f5-113">You can also query an MCIWnd window for its current styles by using the [**MCIWndGetStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstyles) macro.</span></span>

<span data-ttu-id="721f5-114">Eine Liste der mciwnd-spezifischen Fenster Stile finden Sie unter [**mciwndcreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span><span class="sxs-lookup"><span data-stu-id="721f5-114">For a list of the MCIWnd-specific window styles, see [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea).</span></span>

 

 