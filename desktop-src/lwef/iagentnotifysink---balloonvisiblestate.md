---
title: Iagentnotifysink balloonvisiblestate
description: Iagentnotifysink balloonvisiblestate
ms.assetid: 240e049c-7167-41b7-b092-95ed2a83aad3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2dd63d8eef3a7f1a70af81e13506a7e92ad84f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340221"
---
# <a name="iagentnotifysinkballoonvisiblestate"></a><span data-ttu-id="7994f-103">Iagentnotifysink:: balloonvisiblestate</span><span class="sxs-lookup"><span data-stu-id="7994f-103">IAgentNotifySink::BalloonVisibleState</span></span>

<span data-ttu-id="7994f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="7994f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT BalloonVisibleState(
   long dwCharID,  // character ID
   long bVisible   // visibility flag
);                          
```

<span data-ttu-id="7994f-105">Benachrichtigt eine Client Anwendung, wenn sich der Sichtbarkeits Zustand der Wort Sprechblase des Zeichens ändert.</span><span class="sxs-lookup"><span data-stu-id="7994f-105">Notifies a client application when the visibility state of the character's word balloon changes.</span></span>

-   <span data-ttu-id="7994f-106">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="7994f-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="7994f-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="7994f-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="7994f-108">Der Bezeichner des Zeichens, dessen Sichtbarkeits Zustand der Word-Sprechblase geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="7994f-108">Identifier of the character whose word balloon's visibility state has changed.</span></span>

</dd> <dt>

<span data-ttu-id="7994f-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*</span><span class="sxs-lookup"><span data-stu-id="7994f-109"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="7994f-110">Sichtbarkeits Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="7994f-110">Visibility flag.</span></span> <span data-ttu-id="7994f-111">Dieser boolesche Wert ist **true** , wenn die Wort Sprechblase des Zeichens sichtbar wird. und **false** , wenn es ausgeblendet wird.</span><span class="sxs-lookup"><span data-stu-id="7994f-111">This Boolean value is **True** when character's word balloon becomes visible; and **False** when it becomes hidden.</span></span>

</dd> </dl>

<span data-ttu-id="7994f-112">Dieses Ereignis wird an alle Clients des Zeichens gesendet.</span><span class="sxs-lookup"><span data-stu-id="7994f-112">This event is sent to all clients of the character.</span></span>

 

 




