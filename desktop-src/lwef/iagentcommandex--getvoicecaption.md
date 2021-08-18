---
title: IAgentCommandEx GetVoiceCaption
description: IAgentCommandEx GetVoiceCaption
ms.assetid: a81accfd-c137-4347-8ead-4ed5e7148751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d093a971331c6c5cddf467e770dae69960ae0d616ddc9b37863a46d25becb7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105418"
---
# <a name="iagentcommandexgetvoicecaption"></a>IAgentCommandEx::GetVoiceCaption

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption text
);
```

Ruft die [**VoiceCaption für einen**](voicecaption-property.md) Befehl [**ab.**](/windows/desktop/lwef/the-command-object)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*
</dt> <dd>

Die Adresse eines BSTR, der [](caption-property.md) den Wert des Beschriftungstexts empfängt, der für einen Befehl [**angezeigt wird.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

[**VoiceCaption ist der**](voicecaption-property.md) Text, der für ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) im Sprachbefehlsfenster angezeigt wird, wenn Ihre Clientanwendung eingabeaktiv ist.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandEx::SetVoiceCaption**](iagentcommandex--setvoicecaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 