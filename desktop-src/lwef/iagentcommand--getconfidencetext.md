---
title: Iagentcommand getconficetext
description: Iagentcommand getconficetext
ms.assetid: d98339eb-0986-497c-b43c-4e4a952328e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987dca39016a20d185fbd4b8fd2b554c8bec02f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314660"
---
# <a name="iagentcommandgetconfidencetext"></a>Iagentcommand:: getconficetext

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetConfidenceText(
   BSTR * pbszTipText  // address of ConfidenceText setting for Command 
);
```

Ruft den zuvor für einen [**Befehl**](/windows/desktop/lwef/the-command-object)festgelegten lausch Tipp Text ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbsztiptext*
</dt> <dd>

Die Adresse eines BSTR-Werts, der den Wert des lauschenden Trink Texts für einen [**Befehl**](/windows/desktop/lwef/the-command-object)empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: setconficethreshold**](iagentcommand--setconfidencethreshold.md), [**iagentcommand:: getconficethreshold**](iagentcommand--getconfidencethreshold.md), [**iagentcommand:: setconficetext**](iagentcommand--setconfidencetext.md), [**iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md)


 

 