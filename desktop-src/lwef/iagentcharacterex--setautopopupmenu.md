---
title: Iagentcharakteriex-"stautopopupmenu"
description: Iagentcharakteriex-"stautopopupmenu"
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcfd1bd7ea0b02f226ed6f0365b466577807a193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947774"
---
# <a name="iagentcharacterexsetautopopupmenu"></a><span data-ttu-id="b6382-103">Iagentcharakteriex:: abtautopopupmenu</span><span class="sxs-lookup"><span data-stu-id="b6382-103">IAgentCharacterEx::SetAutoPopupMenu</span></span>

<span data-ttu-id="b6382-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b6382-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

<span data-ttu-id="b6382-105">Legt fest, ob der Server das Popup Menü des Zeichens automatisch anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b6382-105">Sets whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="b6382-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b6382-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b6382-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bautopopupmenu*</span><span class="sxs-lookup"><span data-stu-id="b6382-107"><span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="b6382-108">Das automatische Popup-Menü Anzeigeflag.</span><span class="sxs-lookup"><span data-stu-id="b6382-108">The automatic pop-up menu display flag.</span></span> <span data-ttu-id="b6382-109">Wenn dieser Parameter **true** ist, zeigt der Microsoft-Agent automatisch das Popup Menü des Zeichens an, wenn der Benutzer mit der rechten Maustaste auf das Symbol der Taskleiste des Zeichens oder Zeichens klickt.</span><span class="sxs-lookup"><span data-stu-id="b6382-109">If this parameter is **True**, Microsoft Agent automatically displays the character's pop-up menu when the user right-clicks the character or character's taskbar icon.</span></span>

</dd> </dl>

<span data-ttu-id="b6382-110">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="b6382-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="b6382-111">Wenn Sie diese Eigenschaft auf " **false**" festlegen, können Sie ein eigenes Menü Verarbeitungs Verhalten erstellen.</span><span class="sxs-lookup"><span data-stu-id="b6382-111">By setting this property to **False**, you can create your own menu-handling behavior.</span></span> <span data-ttu-id="b6382-112">Um das Menü nach dem Festlegen dieser Eigenschaft auf **false** anzuzeigen, verwenden Sie die [**iagentcharakteriex:: showPopupMenu**](iagentcharacterex--showpopupmenu.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b6382-112">To display the menu after setting this property to **False**, use the [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="b6382-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b6382-113">See Also</span></span>

<span data-ttu-id="b6382-114">[**Iagentcharakteriex:: GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [ **iagentcharakteriex:: showPopupMenu**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="b6382-114">[**IAgentCharacterEx::GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 




