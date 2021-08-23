---
title: IAgentCommands SetCaption
description: IAgentCommands SetCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b38138d218804461afc782efc14ff3685f55d2f737db6fdb21c39021efbcb36e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665470"
---
# <a name="iagentcommandssetcaption"></a>IAgentCommands::SetCaption

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

Legt den [**Beschriftungstext**](caption-property.md) fest, der für eine [**Commands-Auflistung angezeigt**](/windows/desktop/lwef/the-commands-collection-object) wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Ein BSTR, der den Wert für die [**Caption-Eigenschaft**](caption-property.md) für eine [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) angibt.

</dd> </dl>

Das Festlegen der [**Caption-Eigenschaft**](caption-property.md) für eine [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) definiert, wie sie im Popupmenü des Zeichens angezeigt wird, wenn die [**Visible-Eigenschaft**](visible-property.md) auf **True** festgelegt ist und Ihre Anwendung nicht der eingabeaktive Client ist. Um einen Zugriffsschlüssel (unlined mnemonisch) für Die Beschriftung **anzugeben,** schließen Sie vor diesem Zeichen ein ampersand-Zeichen (&) ein.

Wenn Sie Befehle für eine [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) definieren, deren Beschriftung festgelegt ist, definieren Sie in der Regel auch eine **Beschriftung** für ihre **Commands-Sammlung.** [](caption-property.md)

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommands::GetCaption**](iagentcommands--getcaption.md), [**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetVoice**](iagentcommands--setvoice.md)


 

 