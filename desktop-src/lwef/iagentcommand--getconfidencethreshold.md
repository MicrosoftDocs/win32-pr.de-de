---
title: Iagentcommand getconficethreshold
description: Iagentcommand getconficethreshold
ms.assetid: dfbaba7c-ed45-464e-82ab-39e33c023e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6557ad4e6831734106ee2c2e8021f923ef8806
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725945"
---
# <a name="iagentcommandgetconfidencethreshold"></a>Iagentcommand:: getconficethreshold

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetConfidenceThreshold(
long * plConfidenceThreshold  // address of ConfidenceThreshold 
);                            // setting for Command
```

Ruft den Wert der [**conficethreshold**](/windows/desktop/lwef/confidence-property) -Eigenschaft für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plconficethreshold*
</dt> <dd>

Die Adresse einer Variablen, die den Wert der [**conficethreshold**](/windows/desktop/lwef/confidence-property) -Eigenschaft für einen Befehl empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: setconficethreshold**](iagentcommand--setconfidencethreshold.md), [**iagentcommand:: setvertrauenstext**](iagentcommand--setconfidencetext.md), [**iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md)


 

 