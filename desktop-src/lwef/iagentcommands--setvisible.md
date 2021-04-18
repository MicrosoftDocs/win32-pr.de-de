---
title: Iagentcommands setVisible
description: Iagentcommands setVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338252"
---
# <a name="iagentcommandssetvisible"></a>Iagentcommands:: setVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

Legt den Wert der [**Visible**](visible-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*
</dt> <dd>

Ein boolescher Wert, der die [**sichtbare**](visible-property.md) Eigenschaft einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung bestimmt. **True** legt fest, dass die [**Beschriftung**](caption-property.md) der **Befehle** Auflistung sichtbar ist, wenn das Popupmenü des Zeichens angezeigt wird. *False* zeigt ihn nicht an.

</dd> </dl>

Für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung muss die [**Caption**](caption-property.md) -Eigenschaft festgelegt sein und deren [**Visible**](visible-property.md) -Eigenschaft auf **true** festgelegt sein, damit Sie im Popupmenü des Zeichens angezeigt wird. Die **Visible** -Eigenschaft muss auch auf **true** festgelegt werden, damit Befehle in der Auflistung angezeigt werden, wenn die Client Anwendung aktiv ist.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommands:: getVisible**](iagentcommands--getvisible.md), [ **iagentcommand:: setCaption**](iagentcommand--setcaption.md)


 

 