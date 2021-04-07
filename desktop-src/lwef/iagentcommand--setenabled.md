---
title: Iagentcommand-abgeleitete
description: Iagentcommand-abgeleitete
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038864"
---
# <a name="iagentcommandsetenabled"></a>Iagentcommand:: stenabled

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

Legt die [**aktivierte**](enabled-property.md) Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*benabled*
</dt> <dd>

Ein boolescher Wert, der den Wert der [**aktivierten**](enabled-property.md) Einstellung eines [**Befehls**](/windows/desktop/lwef/the-command-object)festlegt. **True** aktiviert den **Befehl**. **False** deaktiviert es. Ein deaktivierter **Befehl** kann nicht ausgewählt werden.

</dd> </dl>

Für einen [**Befehl**](/windows/desktop/lwef/the-command-object) muss die [**aktivierte**](enabled-property.md) Eigenschaft auf **true** festgelegt sein, damit Sie ausgewählt werden können. Außerdem muss die [**Beschriftung**](caption-property.md) -Eigenschaft festgelegt sein, und die [**Visible**](visible-property.md) -Eigenschaft muss auf **true** festgelegt sein, damit Sie im Popup Menü des Zeichens angezeigt wird. Damit der **Befehl** im **Fenster "Sprachbefehle**" angezeigt wird, müssen Sie die [**Voice**](voice-property.md)-Eigenschaft festlegen.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: getcaption**](iagentcommand--getcaption.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)


 

 