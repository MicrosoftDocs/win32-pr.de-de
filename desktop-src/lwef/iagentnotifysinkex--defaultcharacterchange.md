---
title: Iagentnotifysinkex defaultcharacters-Änderung
description: Iagentnotifysinkex defaultcharacters-Änderung
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339001"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a><span data-ttu-id="06ee5-103">Iagentnotifysinkex::D efaultcharacters-Änderung</span><span class="sxs-lookup"><span data-stu-id="06ee5-103">IAgentNotifySinkEx::DefaultCharacterChange</span></span>

<span data-ttu-id="06ee5-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="06ee5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

<span data-ttu-id="06ee5-105">Benachrichtigt eine Client Anwendung, wenn sich das Standard Zeichen ändert.</span><span class="sxs-lookup"><span data-stu-id="06ee5-105">Notifies a client application when the default character changes.</span></span>

-   <span data-ttu-id="06ee5-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="06ee5-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="06ee5-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszguid*</span><span class="sxs-lookup"><span data-stu-id="06ee5-107"><span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszGUID*</span></span>
</dt> <dd>

<span data-ttu-id="06ee5-108">Der eindeutige Bezeichner für das Zeichen.</span><span class="sxs-lookup"><span data-stu-id="06ee5-108">The unique identifier for the character.</span></span>

</dd> </dl>

<span data-ttu-id="06ee5-109">Wenn der Benutzer das als Standard Zeichen des Benutzers zugewiesene Zeichen ändert, sendet der Server dieses Ereignis an Clients, die das Standard Zeichen geladen haben.</span><span class="sxs-lookup"><span data-stu-id="06ee5-109">When the user changes the character assigned as the user's default character, the server sends this event to clients that have loaded the default character.</span></span> <span data-ttu-id="06ee5-110">Das Ereignis gibt den eindeutigen Bezeichner (GUID) des Zeichens zurück, der mit geschweiften Klammern und Bindestrichen formatiert ist, die definiert wird, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor erstellt wird</span><span class="sxs-lookup"><span data-stu-id="06ee5-110">The event returns the character's unique identifier (GUID) formatted with braces and dashes, which is defined when the character is built with the Microsoft Agent Character Editor.</span></span>

<span data-ttu-id="06ee5-111">Wenn das neue Zeichen angezeigt wird, wird die gleiche Größe wie jede bereits geladene Instanz des Zeichens oder das vorherige Standard Zeichen (in dieser Reihenfolge) angenommen.</span><span class="sxs-lookup"><span data-stu-id="06ee5-111">When the new character appears, it assumes the same size as any already loaded instance of the character or the previous default character (in that order).</span></span>

## <a name="see-also"></a><span data-ttu-id="06ee5-112">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="06ee5-112">See Also</span></span>

[<span data-ttu-id="06ee5-113">**Iagent:: Load**</span><span class="sxs-lookup"><span data-stu-id="06ee5-113">**IAgent::Load**</span></span>](iagent--load.md)


 

 




