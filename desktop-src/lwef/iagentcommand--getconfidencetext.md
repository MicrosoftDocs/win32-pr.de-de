---
title: IAgentCommand GetConfidenceText
description: IAgentCommand GetConfidenceText
ms.assetid: d98339eb-0986-497c-b43c-4e4a952328e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d1d5894a04eeb09289e98db42362acbc43d587e5ac680b98276260ba9c323b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961930"
---
# <a name="iagentcommandgetconfidencetext"></a>IAgentCommand::GetConfidenceText

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetConfidenceText(
   BSTR * pbszTipText  // address of ConfidenceText setting for Command 
);
```

Ruft den Text des Lauschen-Tipps ab, der zuvor für einen Befehl [**festgelegt wurde.**](/windows/desktop/lwef/the-command-object)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*
</dt> <dd>

Die Adresse eines BSTR, der den Wert des Texts lauschende Trinkgeld für einen [**Befehl empfängt.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 