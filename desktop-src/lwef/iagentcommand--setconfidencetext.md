---
title: IAgentCommand SetConfidenceText
description: IAgentCommand SetConfidenceText
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8889c8c8c52f392a368c38a91510e112adbeeca42c611cdc0adcadad94f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976340"
---
# <a name="iagentcommandsetconfidencetext"></a>IAgentCommand::SetConfidenceText

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

Legt den Wert des Texts Lauschende Trinkgeld für einen [**Befehl fest.**](/windows/desktop/lwef/the-command-object)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*
</dt> <dd>

Ein BSTR, der den Text für die [**ConfidenceText-Eigenschaft**](confidencetext-property.md) eines Befehls [**angibt.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Wenn der von der besten Übereinstimmung zurückgegebene Konfidenzwert, der im [**Command-Ereignis**](/windows/desktop/lwef/the-command-object) zurückgegeben wird, den für die [**ConfidenceThreshold-Eigenschaft**](/windows/desktop/lwef/confidence-property) festgelegten Wert nicht überschreitet, wird der in *bszTipText* angegebene Text im Lauschenden Tipp angezeigt.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 