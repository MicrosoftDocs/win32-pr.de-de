---
title: Iagentcommand setVisible
description: Iagentcommand setVisible
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106340265"
---
# <a name="iagentcommandsetvisible"></a>Iagentcommand:: setVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

Legt den Wert der [**Visible**](visible-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bvisible*
</dt> <dd>

Ein boolescher Wert, der die [**sichtbare**](visible-property.md) Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object)bestimmt. **True** zeigt den **Befehl** an. **False** blendet es aus.

</dd> </dl>

Für einen [**Befehl**](/windows/desktop/lwef/the-command-object) muss die [**Visible**](visible-property.md) -Eigenschaft auf **true** festgelegt sein, und die [**Beschriftung**](caption-property.md) -Eigenschaft muss im Popup Menü des Zeichens angezeigt werden.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: getVisible**](iagentcommand--getvisible.md), [**iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)


 

 