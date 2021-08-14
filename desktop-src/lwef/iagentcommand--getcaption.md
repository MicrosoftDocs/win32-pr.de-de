---
title: IAgentCommand GetCaption
description: IAgentCommand GetCaption
ms.assetid: e333faca-e2c2-478a-a803-cbc401793e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9deae89890d11e9f14472227eb60590b05f4676151403ded29a78e26fed94f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692842"
---
# <a name="iagentcommandgetcaption"></a>IAgentCommand::GetCaption

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption for Command
);
```

Ruft die [**Beschriftung**](caption-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object)ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*
</dt> <dd>

Die Adresse eines BSTR, der den Wert des [**Beschriftungstexts**](caption-property.md) empfängt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigt wird.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice,**](iagentcommand--setvoice.md) [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 