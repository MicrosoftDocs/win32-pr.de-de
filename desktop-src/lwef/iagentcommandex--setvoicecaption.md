---
title: IAgentCommandEx SetVoiceCaption
description: IAgentCommandEx SetVoiceCaption
ms.assetid: 672fdc13-25d3-4ced-b295-2b687767c17f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe76edb17c2b099db5e16e2b6160703c6b11e8a9f52bcbc24a9ca4bfcb7077c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477213"
---
# <a name="iagentcommandexsetvoicecaption"></a>IAgentCommandEx::SetVoiceCaption

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Legt den [**VoiceCaption-Text**](voicecaption-property.md) fest, der für einen Befehl [**angezeigt wird.**](/windows/desktop/lwef/the-command-object)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

Ein BSTR, der den Text für die [**VoiceCaption-Eigenschaft**](voicecaption-property.md) für einen [**Befehl angibt.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Wenn Sie ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) in einer [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) definieren und dessen [**Voice-Eigenschaft**](voice-property.md) festlegen, legen Sie in der Regel auch die [**VoiceCaption-Eigenschaft**](voicecaption-property.md) fest. Dieser Text wird im Fenster Sprachbefehle angezeigt, wenn Ihre Clientanwendung aktiv ist. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die Einstellung für die [**Caption-Eigenschaft**](caption-property.md) den angezeigten Text. Wenn weder **voiceCaption noch** die -Eigenschaft festgelegt ist, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt.

[**Caption**](caption-property.md)

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 