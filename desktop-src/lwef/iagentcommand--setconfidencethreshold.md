---
title: Iagentcommand setconficethreshold
description: Iagentcommand setconficethreshold
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a6ba352f9385c57d0f3d1f01070f4b46e147d3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101615"
---
# <a name="iagentcommandsetconfidencethreshold"></a>Iagentcommand:: setconficethreshold

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

Legt den Wert der Eigenschaft " [**Vertrauen**](confidence-property.md) " für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lconfidence*
</dt> <dd>

Der Wert für die Eigenschaft " [**Confidence**](confidence-property.md) " eines [**Befehls**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Wenn der von der am besten zurückgegebene Wert zurückgegebene Vertrauens Wert den Wert, der [**für die Eigenschaft**](/windows/desktop/lwef/the-command-object) [**conficethreshold**](/windows/desktop/lwef/confidence-property) zurückgegeben wurde, nicht überschreitet, wird der in [**setconficetext**](iagentcommand--setconfidencetext.md) angegebene Text in der lausch Info angezeigt.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand:: getconficethreshold**](iagentcommand--getconfidencethreshold.md), [**iagentcommand:: setvertrauenstext**](iagentcommand--setconfidencetext.md), [**iagentuserinput:: getitemconfidence**](iagentuserinput--getitemconfidence.md)


 

 