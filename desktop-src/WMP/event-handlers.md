---
title: Ereignishandler
description: Ereignishandler
ms.assetid: abb5f123-b838-46fb-ab11-cee70cc76a38
keywords:
- Windows Media Player Skins, Ereignishandler in JScript
- Skins, Ereignishandler in JScript
- Ereignisse, JScript
- JScript-Dateien für Skins, Ereignishandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec4413ae3a2358b01685cd0edfe66de92810a64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337749"
---
# <a name="event-handlers"></a><span data-ttu-id="56f64-107">Ereignishandler</span><span class="sxs-lookup"><span data-stu-id="56f64-107">Event Handlers</span></span>

<span data-ttu-id="56f64-108">Microsoft JScript wird zum Verarbeiten von Ereignissen in der Skin-Definitionsdatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="56f64-108">Microsoft JScript is used to process events in the skin definition file.</span></span> <span data-ttu-id="56f64-109">Weitere Informationen zu Ereignis Handlern finden Sie unter [Behandeln von Ereignissen](handling-events.md) .</span><span class="sxs-lookup"><span data-stu-id="56f64-109">See [Handling Events](handling-events.md) for more information about event handlers.</span></span>

<span data-ttu-id="56f64-110">Sie können in einem Ereignishandler mehr als eine Codezeile enthalten, aber beachten Sie, dass es nicht erforderlich ist, die Zeilenlänge zu überschreiten, die JScript zulässt.</span><span class="sxs-lookup"><span data-stu-id="56f64-110">You can have more than one line of code in an event handler, but care must be taken not to exceed the line length that JScript permits.</span></span> <span data-ttu-id="56f64-111">Trennen Sie die Zeilen durch Semikolons.</span><span class="sxs-lookup"><span data-stu-id="56f64-111">Separate the lines by semicolons.</span></span>


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a><span data-ttu-id="56f64-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="56f64-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56f64-113">**Verwenden von JScript**</span><span class="sxs-lookup"><span data-stu-id="56f64-113">**Using JScript**</span></span>](using-jscript.md)
</dt> </dl>

 

 




