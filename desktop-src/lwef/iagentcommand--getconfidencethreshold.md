---
title: IAgentCommand GetConfidenceThreshold
description: IAgentCommand GetConfidenceThreshold
ms.assetid: dfbaba7c-ed45-464e-82ab-39e33c023e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e4297012db2118da2fe5db79dbe8e969d9b4006b4078198a0d384898fc9fa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976380"
---
# <a name="iagentcommandgetconfidencethreshold"></a>IAgentCommand::GetConfidenceThreshold

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetConfidenceThreshold(
long * plConfidenceThreshold  // address of ConfidenceThreshold 
);                            // setting for Command
```

Ruft den Wert der [**ConfidenceThreshold-Eigenschaft**](/windows/desktop/lwef/confidence-property) für einen [**Befehl ab.**](/windows/desktop/lwef/the-command-object)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plConfidenceThreshold*
</dt> <dd>

Die Adresse einer Variablen, die den Wert der [**ConfidenceThreshold-Eigenschaft**](/windows/desktop/lwef/confidence-property) für einen Befehl empfängt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 