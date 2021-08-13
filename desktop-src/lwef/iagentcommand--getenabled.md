---
title: IAgentCommand GetEnabled
description: IAgentCommand GetEnabled
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7118fa06fc895729755a36872a6d092d962d2416f81ac50e5c528cf9d69f5312
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477655"
---
# <a name="iagentcommandgetenabled"></a>IAgentCommand::GetEnabled

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

Ruft den Wert der [**Enabled-Eigenschaft**](enabled-property.md) für einen [**Befehl ab.**](/windows/desktop/lwef/the-command-object)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Die Adresse einer Variablen, die **TRUE empfängt,** wenn [**der Befehl**](/windows/desktop/lwef/the-command-object) aktiviert ist, oder **False,** wenn sie deaktiviert ist. Ein **deaktivierter Befehl** kann nicht ausgewählt werden.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 