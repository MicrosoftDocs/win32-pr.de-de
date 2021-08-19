---
title: IAgentCommand SetEnabled
description: IAgentCommand SetEnabled
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da164b6603d93496e3381ccc6938a3b6d8f520bcea887cfd11f031cec7d845a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976310"
---
# <a name="iagentcommandsetenabled"></a>IAgentCommand::SetEnabled

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

Legt die [**Enabled-Eigenschaft**](enabled-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object)fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Ein boolescher Wert, der den Wert der [**Einstellung Aktiviert**](enabled-property.md) eines [**Befehls**](/windows/desktop/lwef/the-command-object)festlegt. **True** aktiviert den **Befehl**; **False** deaktiviert sie. Ein **deaktivierter Befehl** kann nicht ausgewählt werden.

</dd> </dl>

Für einen [**Befehl**](/windows/desktop/lwef/the-command-object) muss die [**Enabled-Eigenschaft**](enabled-property.md) auf **True** festgelegt sein, damit er auswählbar ist. Außerdem muss die [**Caption-Eigenschaft**](caption-property.md) und die [**Visible-Eigenschaft**](visible-property.md) auf **True** festgelegt sein, damit sie im Popupmenü des Zeichens angezeigt wird. Damit der **Befehl** im **Fenster "Sprachbefehle"** angezeigt wird, müssen Sie dessen [**Voice-Eigenschaft**](voice-property.md)festlegen.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetVoice,**](iagentcommand--setvoice.md) [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 