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
# <a name="event-handlers"></a>Ereignishandler

Microsoft JScript wird zum Verarbeiten von Ereignissen in der Skin-Definitionsdatei verwendet. Weitere Informationen zu Ereignis Handlern finden Sie unter [Behandeln von Ereignissen](handling-events.md) .

Sie können in einem Ereignishandler mehr als eine Codezeile enthalten, aber beachten Sie, dass es nicht erforderlich ist, die Zeilenlänge zu überschreiten, die JScript zulässt. Trennen Sie die Zeilen durch Semikolons.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von JScript**](using-jscript.md)
</dt> </dl>

 

 




