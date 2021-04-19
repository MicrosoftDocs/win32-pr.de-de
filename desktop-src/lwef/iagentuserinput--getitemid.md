---
title: Iagentuserinput getItemID
description: Iagentuserinput getItemID
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716ae1386d87fa6051111801c5603837519eeb4c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342234"
---
# <a name="iagentuserinputgetitemid"></a>Iagentuserinput:: getItemID

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

Ruft den Bezeichner einer [**Befehls**](command-event.md) Alternative ab, die an einen [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wurde.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwitemindex*
</dt> <dd>

Der Index der [**Befehls**](command-event.md) Alternative, die an den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf übermittelt wird.

</dd> <dt>

<span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwcommandid*
</dt> <dd>

Adresse einer Variablen, die die ID eines [**Befehls**](command-event.md)empfängt.

</dd> </dl>

Wenn die Spracheingabe den [**iagentnotifysink:: Command**](iagentnotifysink--command.md) -Rückruf auslöst, gibt der Server die IDs für alle übereinstimmenden [**Befehle**](command-event.md) zurück, die von der Anwendung definiert werden.

## <a name="see-also"></a>Weitere Informationen

[**Iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md), [**iagentuserinput:: GetItemText**](iagentuserinput--getitemtext.md), [**iagentuserinput:: getallitemdata**](iagentuserinput--getallitemdata.md)


 

 




