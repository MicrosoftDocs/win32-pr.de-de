---
title: Iagentuserinput GetItemText
description: Iagentuserinput GetItemText
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7010172147f86282903641c46aa5137ce69c80be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036224"
---
# <a name="iagentuserinputgetitemtext"></a>Iagentuserinput:: GetItemText

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

Ruft den sprach Text für eine [**Befehls**](command-event.md) Alternative ab, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwitemindex*
</dt> <dd>

Der Index einer [**Befehls**](command-event.md) Alternative, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbsztext*
</dt> <dd>

Die Adresse eines BSTR-Werts, der den Wert des sprach Texts für den [**Befehl**](command-event.md)empfängt.

</dd> </dl>

Wenn die Spracheingabe nicht die Quelle für den Befehl war, z. b. wenn der Benutzer den Befehl aus dem Popupmenü des Zeichens ausgewählt hat, gibt der Server für den sprach Text des [**Befehls**](command-event.md) **null** zurück.

## <a name="see-also"></a>Weitere Informationen

[**Iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md), [**iagentuserinput:: getItemID**](iagentuserinput--getitemid.md), [**iagentuserinput:: getallitemdata**](iagentuserinput--getallitemdata.md)


 

 




