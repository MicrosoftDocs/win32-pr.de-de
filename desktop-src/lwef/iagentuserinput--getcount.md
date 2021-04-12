---
title: Iagentuserinput GetCount
description: Iagentuserinput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ac4b597f7367eff10154bde256698ef371c3619
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206186"
---
# <a name="iagentuserinputgetcount"></a>Iagentuserinput:: GetCount

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

Ruft die Anzahl der [**Befehls**](command-event.md) Alternativen ab, die an einen [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt werden.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Adresse einer Variablen, die die Anzahl der vom Server identifizierten [**Befehle**](command-event.md) empfängt.

</dd> </dl>

Wenn die Spracheingabe nicht die Quelle für den Befehl war, z. b. wenn der Benutzer den Befehl aus dem Popupmenü des Zeichens ausgewählt hat, gibt **GetCount** den Wert 1 zurück. Wenn **GetCount** NULL (0) zurückgibt, hat die Spracherkennungs-Engine gesprochene Eingaben erkannt, aber festgestellt, dass es keinen übereinstimmenden Befehl gab.

 

 




