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
# <a name="the-wait-flag"></a>Das Wait-Flag.

MCI-Befehle kehren normalerweise sofort an den Benutzer zurück, auch wenn es einige Minuten dauert, bis die vom Befehl initiierte Aktion abgeschlossen ist. Sie können das Flag "wait" (MCI \_ Wait) verwenden, um das Gerät so zu leiten, dass es bis zum Abschluss der angeforderten Aktion gewartet wird, bevor die Steuerung an die Anwendung zurückgegeben wird.

Der folgende [**Wiedergabe**](play.md) Befehl gibt z. b. die Steuerung nicht an die Anwendung zurück, bis die Wiedergabe abgeschlossen ist:


```C++
mciSendString("play mydevice from 0 to 100 wait", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



> [!Note]  
> Der Benutzer kann einen Warte Vorgang abbrechen, indem er eine Break-Taste drückt. Standardmäßig ist dieser Schlüssel Strg + Pause. Anwendungen können diesen Schlüssel mit dem Befehl "unter [**brechen**](break.md) " ([**MCI- \_ Pause**](mci-break.md)) neu definieren. (Bei der **MCI-unter \_ Brechung** wird die MCI-Struktur zum unter [**brechen von \_ \_ Parametern**](mci-break-parms.md) Wenn ein warte Vorgang abgebrochen wird, versucht MCI, die Steuerung an die Anwendung zurückzugeben, ohne den dem "wait"-Flag zugeordneten Befehl zu unterbrechen.

 

 

 




