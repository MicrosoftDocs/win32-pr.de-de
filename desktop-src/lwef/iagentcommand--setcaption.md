---
title: Iagentcommand setCaption
description: Iagentcommand setCaption
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88453f54ffa59b413f30d27c58aa6cd2dcc6e12e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038911"
---
# <a name="iagentcommandsetcaption"></a>Iagentcommand:: setCaption

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

Legt den [**Beschriftungs**](caption-property.md) Text fest, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszcaption*
</dt> <dd>

Ein BSTR, der den Text für die [**Caption**](caption-property.md) -Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object)angibt.

</dd> </dl>

Wenn Sie die [**Caption**](caption-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object) festlegen, wird definiert, wie diese im Popupmenü des Zeichens angezeigt wird, wenn die [**sichtbare**](visible-property.md) Eigenschaft auf **true** festgelegt ist und die Anwendung nicht der Eingabe aktive Client ist. Um einen Zugriffsschlüssel (unline-mnetmonic) für Ihre **Beschriftung** anzugeben, fügen Sie vor diesem Zeichen ein kaufmännisches und-Zeichen (&) ein. Um ihn auswählbar zu machen, muss seine [**aktivierte**](enabled-property.md) Eigenschaft auf **true** festgelegt werden.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: getcaption**](iagentcommand--getcaption.md), [**iagentcommand:: SetEnabled**](iagentcommand--setenabled.md), [**iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)


 

 