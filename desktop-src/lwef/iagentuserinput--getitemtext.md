---
title: IAgentUserInput GetItemText
description: IAgentUserInput GetItemText
ms.assetid: 69653806-c001-4015-bd05-3c261a312ede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd9c1392bd56e3bb59212edeb79d862260786edb87583c0e8fdf049e8345b40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119359040"
---
# <a name="iagentuserinputgetitemtext"></a>IAgentUserInput::GetItemText

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetItemText(
   Long dwItemIndex,  // index of Command alternative
   BSTR * pbszText    // address of voice text for Command 
);
```

Ruft den Sprachtext für eine [**Befehlsalternative**](command-event.md) ab, die an den [**IAgentNotifySink::Command-Rückruf**](iagentnotifysink--command.md) übergeben wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwItemIndex"></span><span id="dwitemindex"></span><span id="DWITEMINDEX"></span>*dwItemIndex*
</dt> <dd>

Der Index [](command-event.md) einer Befehlsalternative, die an den [**IAgentNotifySink::Command-Rückruf**](iagentnotifysink--command.md) übergeben wird.

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Adresse eines BSTR, der den Wert des Sprachtexts für den [**Befehl**](command-event.md)empfängt.

</dd> </dl>

Wenn die Spracheingabe nicht die Quelle für den Befehl war, z. B. wenn der Benutzer den Befehl im Popupmenü des Zeichens ausgewählt hat, gibt der Server **NULL** für den Sprachtext des [**Befehls**](command-event.md)zurück.

## <a name="see-also"></a>Weitere Informationen

[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md), [**IAgentUserInput::GetAllItemData**](iagentuserinput--getallitemdata.md)


 

 




