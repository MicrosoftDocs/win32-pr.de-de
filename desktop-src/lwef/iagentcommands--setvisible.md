---
title: IAgentCommands SetVisible
description: IAgentCommands SetVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7979651635c27f5633d5ebeada8e5f2866d383ece0b19a38dd32082596e4712b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692779"
---
# <a name="iagentcommandssetvisible"></a>IAgentCommands::SetVisible

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

Legt den Wert der [**Visible-Eigenschaft**](visible-property.md) für eine [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*
</dt> <dd>

Ein boolescher Wert, der die [**Visible-Eigenschaft**](visible-property.md) einer [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) bestimmt. **True** legt **fest, dass** die [**Beschriftung**](caption-property.md) der Commands-Sammlung sichtbar ist, wenn das Popupmenü des Zeichens angezeigt wird. *False* zeigt es nicht an.

</dd> </dl>

Für [**eine Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) muss [**die Caption-Eigenschaft**](caption-property.md) und die [**Visible-Eigenschaft**](visible-property.md) auf **True** festgelegt sein, damit sie im Popupmenü des Zeichens angezeigt wird. Die **Visible-Eigenschaft** muss auch auf **True** festgelegt werden, damit Befehle in der Auflistung angezeigt werden, wenn Ihre Clientanwendung eingabeaktiv ist.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [ **IAgentCommand::SetCaption**](iagentcommand--setcaption.md)


 

 