---
title: Das Warteflag
description: Das Warteflag
ms.assetid: b971ccd4-0507-4f05-adb3-d4930496034d
keywords:
- MCI_WAIT-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 311e1a55e756cfc3c1038f6ab3ccb4b708bb066dde962afff31006dcf39b7c4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801434"
---
# <a name="the-wait-flag"></a>Das Warteflag

MCI-Befehle kehren in der Regel sofort an den Benutzer zurück, auch wenn es einige Minuten dauert, die vom Befehl initiierte Aktion auszuführen. Sie können das Warteflag (MCI WAIT) verwenden, um das Gerät anleiten, bis die angeforderte Aktion abgeschlossen ist, bevor die Steuerung an die \_ Anwendung zurückverlangt wird.

Beispielsweise gibt der folgende [**Wiedergabebefehl**](play.md) die Steuerung erst dann an die Anwendung zurück, wenn die Wiedergabe abgeschlossen ist:


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> Der Benutzer kann einen Wartevorgang abbrechen, indem er eine Haltetaste drückt. Standardmäßig ist diese Taste STRG+BREAK. Anwendungen können diesen Schlüssel mithilfe des Befehls [**break**](break.md) ([**MCI \_ BREAK**](mci-break.md)) neu definieren. (**MCI \_ BREAK** verwendet die [**MCI \_ BREAK \_ PARMS-Struktur.)**](mci-break-parms.md) Wenn ein Wartevorgang abgebrochen wird, versucht MCI, die Steuerung an die Anwendung zurück zu geben, ohne den Befehl zu unterbrechen, der dem Flag "wait" zugeordnet ist.

 

 

 




