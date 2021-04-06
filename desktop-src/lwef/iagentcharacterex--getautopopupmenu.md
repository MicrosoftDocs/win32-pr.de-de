---
title: Iagentcharakteriex GetAutoPopupMenu
description: Iagentcharakteriex GetAutoPopupMenu
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7a3b8d1075c596f27af17df34c7cb94d8a1ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947918"
---
# <a name="iagentcharacterexgetautopopupmenu"></a><span data-ttu-id="b9cba-103">Iagentcharakteriex:: GetAutoPopupMenu</span><span class="sxs-lookup"><span data-stu-id="b9cba-103">IAgentCharacterEx::GetAutoPopupMenu</span></span>

<span data-ttu-id="b9cba-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="b9cba-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAutoPopupMenu(
   long * pbAutoPopupMenu  // address of auto pop-up menu display setting
);
```

<span data-ttu-id="b9cba-105">Ruft ab, ob der Server das Popup Menü des Zeichens automatisch anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b9cba-105">Retrieves whether the server automatically displays the character's pop-up menu.</span></span>

-   <span data-ttu-id="b9cba-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="b9cba-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b9cba-107"><span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbautopopupmenu*</span><span class="sxs-lookup"><span data-stu-id="b9cba-107"><span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbAutoPopupMenu*</span></span>
</dt> <dd>

<span data-ttu-id="b9cba-108">Adresse einer Variablen, die **true** empfängt, wenn der Microsoft-Agent-Server die Anzeige des Popup Menüs des Zeichens automatisch behandelt, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b9cba-108">Address of a variable that receives **True** if the Microsoft Agent server automatically handles displaying the character's pop-up menu and **False** if not.</span></span>

</dd> </dl>

<span data-ttu-id="b9cba-109">Wenn diese Eigenschaft auf **false** festgelegt ist, muss die Anwendung das Popup Menü mithilfe der [**iagentcharakteriex:: showPopupMenu**](iagentcharacterex--showpopupmenu.md) -Methode anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b9cba-109">When this property is set to **False**, your application must display the pop-up menu using [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md) method.</span></span>

<span data-ttu-id="b9cba-110">Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.</span><span class="sxs-lookup"><span data-stu-id="b9cba-110">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9cba-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b9cba-111">See Also</span></span>

<span data-ttu-id="b9cba-112">[**Iagentcharakteriex:: abtautopopupmenu**](iagentcharacterex--setautopopupmenu.md), [ **iagentcharakteriex:: showPopupMenu**](iagentcharacterex--showpopupmenu.md)</span><span class="sxs-lookup"><span data-stu-id="b9cba-112">[**IAgentCharacterEx::SetAutoPopupMenu**](iagentcharacterex--setautopopupmenu.md), [**IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)</span></span>


 

 




