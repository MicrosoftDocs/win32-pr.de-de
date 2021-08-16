---
title: IAgentUserInput GetCount
description: IAgentUserInput GetCount
ms.assetid: 9c127387-b680-405a-9a62-ee08cc70813a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f52c296dd152fd1e31a87e21d80f8b25d52ae880b300487cdcba746e81dfa0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749517"
---
# <a name="iagentuserinputgetcount"></a>IAgentUserInput::GetCount

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of a variable for number of alternatives 
);
```

Ruft die Anzahl der [**Befehlsalternativen**](command-event.md) ab, die an einen [**IAgentNotifySink::Command-Rückruf**](iagentnotifysink--command.md) übergeben werden.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Adresse einer Variablen, die die Anzahl der vom Server [**identifizierten Befehlsalternativen**](command-event.md) empfängt.

</dd> </dl>

Wenn die Spracheingabe nicht die Quelle für den Befehl war, z. B. wenn der Benutzer den Befehl im Popupmenü des Zeichens ausgewählt hat, gibt **GetCount** 1 zurück. Wenn **GetCount** null (0) zurückgibt, hat die Spracherkennungs-Engine gesprochene Eingaben erkannt, aber festgestellt, dass kein übereinstimmender Befehl vorhanden war.

 

 




