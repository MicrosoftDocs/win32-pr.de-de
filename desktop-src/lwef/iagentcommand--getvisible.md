---
title: Iagentcommand getVisible
description: Iagentcommand getVisible
ms.assetid: cac07737-6a0b-4587-ae16-2137ce0d412c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1058c3855214dada0f1567f9fef81a3efc7e20a2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390295"
---
# <a name="iagentcommandgetvisible"></a>Iagentcommand:: getVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Command
);
```

Ruft den Wert der [**Visible**](visible-property.md) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*
</dt> <dd>

Die Adresse einer Variablen, die die [**sichtbare**](visible-property.md) Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)


 

 