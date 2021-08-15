---
title: Ereignishandler
description: Ereignishandler
ms.assetid: abb5f123-b838-46fb-ab11-cee70cc76a38
keywords:
- Windows Media Player Skins, Ereignishandler in JScript
- Skins, Ereignishandler in JScript
- events,JScript
- JScript für Skins,Ereignishandler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c936e36cd9b7404260473068ccc3d6c3f5d0ab75553ba878dff88587e535ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339271"
---
# <a name="event-handlers"></a>Ereignishandler

Microsoft JScript wird verwendet, um Ereignisse in der Skindefinitionsdatei zu verarbeiten. Weitere [Informationen zu Ereignishandlern](handling-events.md) finden Sie unter Behandeln von Ereignissen.

Sie können mehr als eine Codezeile in einem Ereignishandler verwenden, aber es muss darauf achten, die Zeilenlänge nicht zu überschreiten, die JScript erlaubt. Trennen Sie die Zeilen durch Semikolons.


```C++
onclick = "JScript: player.URL = 'https://proseware.com/cool.wma' ; myText.value = 'Playing'; "

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden JScript**](using-jscript.md)
</dt> </dl>

 

 




