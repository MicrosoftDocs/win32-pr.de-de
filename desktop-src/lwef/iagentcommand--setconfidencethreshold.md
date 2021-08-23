---
title: IAgentCommand SetConfidenceThreshold
description: IAgentCommand SetConfidenceThreshold
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 244f181fb4d9e706271440797e1261fd381897e00a5a216d681e0f3984d24a6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976300"
---
# <a name="iagentcommandsetconfidencethreshold"></a>IAgentCommand::SetConfidenceThreshold

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

Legt den Wert der [**Confidence-Eigenschaft**](confidence-property.md) für einen [**Befehl fest.**](/windows/desktop/lwef/the-command-object)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*
</dt> <dd>

Der Wert für die [**Confidence-Eigenschaft**](confidence-property.md) eines [**Befehls**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Wenn der von der besten Übereinstimmung zurückgegebene Konfidenzwert, der im [**Command-Ereignis**](/windows/desktop/lwef/the-command-object) zurückgegeben wird, den für die [**ConfidenceThreshold-Eigenschaft**](/windows/desktop/lwef/confidence-property) festgelegten Wert nicht überschreitet, wird der in [**SetConfidenceText**](iagentcommand--setconfidencetext.md) angegebene Text im Lauschenden Tipp angezeigt.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 