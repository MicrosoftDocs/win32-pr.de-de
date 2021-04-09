---
title: Das Wait-Flag.
description: Das Wait-Flag.
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- MCI_WAIT-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e552650aca9cf104d2c87d7faddd0b6c85b5a6b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037620"
---
# <a name="the-wait-flag"></a><span data-ttu-id="773be-104">Das Wait-Flag.</span><span class="sxs-lookup"><span data-stu-id="773be-104">The Wait Flag</span></span>

<span data-ttu-id="773be-105">MCI-Befehle kehren normalerweise sofort an den Benutzer zurück, auch wenn es einige Minuten dauert, bis die vom Befehl initiierte Aktion abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="773be-105">MCI commands usually return to the user immediately, even if it takes several minutes to complete the action initiated by the command.</span></span> <span data-ttu-id="773be-106">Sie können das Flag "wait" (MCI \_ Wait) verwenden, um das Gerät so zu leiten, dass es bis zum Abschluss der angeforderten Aktion gewartet wird, bevor die Steuerung an die Anwendung zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="773be-106">You can use the "wait" (MCI\_WAIT) flag to direct the device to wait until the requested action is completed before returning control to the application.</span></span>

<span data-ttu-id="773be-107">Der folgende [**Wiedergabe**](play.md) Befehl gibt z. b. die Steuerung nicht an die Anwendung zurück, bis die Wiedergabe abgeschlossen ist:</span><span class="sxs-lookup"><span data-stu-id="773be-107">For example, the following [**play**](play.md) command will not return control to the application until the playback completes:</span></span>


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> <span data-ttu-id="773be-108">Der Benutzer kann einen Warte Vorgang abbrechen, indem er eine Break-Taste drückt.</span><span class="sxs-lookup"><span data-stu-id="773be-108">The user can cancel a wait operation by pressing a break key.</span></span> <span data-ttu-id="773be-109">Standardmäßig ist dieser Schlüssel Strg + Pause.</span><span class="sxs-lookup"><span data-stu-id="773be-109">By default, this key is CTRL+BREAK.</span></span> <span data-ttu-id="773be-110">Anwendungen können diesen Schlüssel mit dem Befehl "unter [**brechen**](break.md) " ([**MCI- \_ Pause**](mci-break.md)) neu definieren.</span><span class="sxs-lookup"><span data-stu-id="773be-110">Applications can redefine this key by using the [**break**](break.md) ([**MCI\_BREAK**](mci-break.md)) command.</span></span> <span data-ttu-id="773be-111">(Bei der **MCI-unter \_ Brechung** wird die MCI-Struktur zum unter [**brechen von \_ \_ Parametern**](mci-break-parms.md) Wenn ein warte Vorgang abgebrochen wird, versucht MCI, die Steuerung an die Anwendung zurückzugeben, ohne den dem "wait"-Flag zugeordneten Befehl zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="773be-111">(**MCI\_BREAK** uses the [**MCI\_BREAK\_PARMS**](mci-break-parms.md) structure.) When a wait operation is canceled, MCI attempts to return control to the application without interrupting the command associated with the "wait" flag.</span></span>

 

 

 




