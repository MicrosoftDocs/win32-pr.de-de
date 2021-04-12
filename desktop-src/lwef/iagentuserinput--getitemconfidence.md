---
title: Iagentuserinput getitemconfidence
description: Iagentuserinput getitemconfidence
ms.assetid: 7d1ca2f0-416c-43c3-99a8-9f287cb88de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846e1fca9ea1245a62fc68330d68263b63fb7cfd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309140"
---
# <a name="iagentuserinputgetitemconfidence"></a>Iagentuserinput:: getitemconfidence

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetItemConfidence(
   long dwItemIndex,    // index of Command alternative
   long * plConfidence  // address of confidence value for Command 
);
```

Ruft den Vertrauens Wert für einen [**Befehl**](command-event.md) ab, der an einen [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwitemindex*
</dt> <dd>

Der Index einer [**Befehls**](command-event.md) Alternative, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.

</dd> <dt>

<span id="plConfidence"></span><span id="plconfidence"></span><span id="PLCONFIDENCE"></span>*plconfidence*
</dt> <dd>

Adresse einer Variablen, die das Vertrauens Ergebnis für eine [**Befehls**](command-event.md) Alternative empfängt, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.

</dd> </dl>

Wenn die Spracheingabe nicht die Quelle für den Befehl war, z. b. wenn der Benutzer den Befehl aus dem Popupmenü des Zeichens ausgewählt hat, gibt der Microsoft-Agent-Server den Vertrauens Wert der besten Entsprechung als 100 und die Vertrauens Werte für alle anderen Alternativen als NULL (0) zurück.

## <a name="see-also"></a>Weitere Informationen

[**Iagentuserinput:: getItemID**](iagentuserinput--getitemid.md), [**iagentuserinput:: getallitemdata**](iagentuserinput--getallitemdata.md), [**iagentuserinput:: GetItemText**](iagentuserinput--getitemtext.md)


 

 




