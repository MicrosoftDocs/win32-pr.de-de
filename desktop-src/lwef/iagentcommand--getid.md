---
title: Iagentcommand-GetId
description: Iagentcommand-GetId
ms.assetid: 4d8d8be7-7003-4ef3-abba-b5232267c993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d1f5887123df19496c0610c53fe59a3f64961cd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390157"
---
# <a name="iagentcommandgetid"></a>Iagentcommand:: GetId

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetID(
   long * pdwID  // address of ID for Command
);
```

Ruft die ID für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwid*
</dt> <dd>

Die Adresse einer Variablen, die die ID eines [**Befehls**](/windows/desktop/lwef/the-command-object)empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md), [**iagentcommands:: Remove**](iagentcommands--remove.md)


 

 