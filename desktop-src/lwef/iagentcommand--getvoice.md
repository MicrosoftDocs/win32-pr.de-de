---
title: Iagentcommand getvoice
description: Iagentcommand getvoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341710"
---
# <a name="iagentcommandgetvoice"></a>Iagentcommand:: getvoice

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

Ruft den Wert der [**Voice**](voice-property.md) -Text-Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszvoice*
</dt> <dd>

Die Adresse eines BSTR, der die [**Voice**](voice-property.md) -Text-Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.

</dd> </dl>

Ein [**Befehl**](/windows/desktop/lwef/the-command-object) , bei dem der [**Voice**](voice-property.md) -Eigenschaften Satz und seine [**aktivierte**](enabled-property.md) Eigenschaft auf **true** festgelegt sind, sind sprach zugänglich. Wenn die [**Beschriftungs**](caption-property.md) Eigenschaft ebenfalls festgelegt ist, wird Sie im Fenster "Sprachbefehle" angezeigt. Wenn die [**sichtbare**](visible-property.md) Eigenschaft auf **true** festgelegt ist, wird Sie im Popupmenü des Zeichens angezeigt.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)


 

 