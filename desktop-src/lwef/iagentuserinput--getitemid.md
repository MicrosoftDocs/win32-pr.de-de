---
title: IAgentUserInput GetItemID
description: IAgentUserInput GetItemID
ms.assetid: 3afd4d9d-51bb-4086-bf7b-7c9a2ddcd807
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fde65fc10a4cb467bd69f200e3244f1a2a73c0424d64f6a4babbd2cefd18e0be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609260"
---
# <a name="iagentuserinputgetitemid"></a>IAgentUserInput::GetItemID

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetItemID(
   long dwItemIndex,    // index of Command alternative
   long * pdwCommandID  // address of a variable for number of alternatives 
);
```

Ruft den Bezeichner einer [**Command-Alternative**](command-event.md) ab, die an einen [**IAgentNotifySink::Command-Rückruf**](iagentnotifysink--command.md) übergeben wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Der Index der [**Command-Alternative,**](command-event.md) die an den [**IAgentNotifySink::Command-Rückruf**](iagentnotifysink--command.md) übergeben wird.

</dd> <dt>

<span id="pdwCommandID"></span><span id="pdwcommandid"></span><span id="PDWCOMMANDID"></span>*pdwCommandID*
</dt> <dd>

Adresse einer Variablen, die die ID eines Befehls [**empfängt.**](command-event.md)

</dd> </dl>

Wenn die Spracheingabe den [**IAgentNotifySink::Command-Rückruf**](iagentnotifysink--command.md) auslöst, gibt der Server die IDs für alle übereinstimmenden [**Befehle**](command-event.md) zurück, die von Ihrer Anwendung definiert werden.

## <a name="see-also"></a>Weitere Informationen

[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




