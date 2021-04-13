---
title: Iagentcommands setCaption
description: Iagentcommands setCaption
ms.assetid: 042f7366-0071-40a5-a47c-81c02cdbe3a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8c472bfbfd82235e21c28e24e7e0ce03223ff8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390177"
---
# <a name="iagentcommandssetcaption"></a>Iagentcommands:: setCaption

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Commands collection
);
```

Legt den [**Beschriftungs**](caption-property.md) Text fest, der für eine [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszcaption*
</dt> <dd>

Ein BSTR, der den Wert für die [**Caption**](caption-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung angibt.

</dd> </dl>

Wenn Sie die [**Caption**](caption-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung festlegen, wird definiert, wie diese im Popup Menü des Zeichens angezeigt wird, wenn die [**sichtbare**](visible-property.md) Eigenschaft auf **true** festgelegt ist und die Anwendung nicht der Input-Active-Client ist. Um einen Zugriffsschlüssel (unline-mnetmonic) für Ihre **Beschriftung** anzugeben, fügen Sie vor diesem Zeichen ein kaufmännisches und-Zeichen (&) ein.

Wenn Sie Befehle für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definieren, deren [**Beschriftung**](caption-property.md) festgelegt ist, definieren Sie in der Regel auch eine **Beschriftung** für die zugehörige **Commands** -Auflistung.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommands:: getcaption**](iagentcommands--getcaption.md), [**iagentcommands:: setVisible**](iagentcommands--setvisible.md), [**iagentcommands:: setvoice**](iagentcommands--setvoice.md)


 

 