---
title: Iagentcommand GetEnabled
description: Iagentcommand GetEnabled
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238844a70ea7fde3ef0c07cad1a6f3abab5613d1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472932"
---
# <a name="iagentcommandgetenabled"></a>Iagentcommand:: GetEnabled

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

Ruft den Wert der [**aktivierten**](enabled-property.md) Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbenabled*
</dt> <dd>

Die Adresse einer Variablen, die **true** erhält, wenn der [**Befehl**](/windows/desktop/lwef/the-command-object) aktiviert ist, oder **false** , wenn Sie deaktiviert ist. Ein deaktivierter **Befehl** kann nicht ausgewählt werden.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: setCaption**](iagentcommand--setcaption.md), [**iagentcommand:: setVisible**](iagentcommand--setvisible.md), [**iagentcommand:: setvoice**](iagentcommand--setvoice.md), [**iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md)


 

 