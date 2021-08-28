---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85de69b4b594f93adfb0ff554819243c94986420a79c35e8d7a64a3c2eaccb6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716140"
---
# <a name="iagentcommandsexsetvoicecaption"></a>IAgentCommandsEx::SetVoiceCaption

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

Legt den [**VoiceCaption-Text fest,**](voicecaption-property.md) der für das [**Command-Objekt**](/windows/desktop/lwef/the-command-object) angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*
</dt> <dd>

Ein BSTR, der den Text für die [**VoiceCaption-Eigenschaft**](voicecaption-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt.

</dd> </dl>

Wenn Sie ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) in einer [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) definieren und dessen [**Voice-Eigenschaft**](voice-property.md) festlegen, legen Sie in der Regel auch die [**VoiceCaption-Eigenschaft**](voicecaption-property.md) fest. Dieser Text wird im Sprachbefehlsfenster angezeigt, wenn Ihre Clientanwendung eingabeaktiv ist und das Zeichen sichtbar ist. Wenn diese Eigenschaft nicht festgelegt ist, bestimmt die Einstellung für die [**Caption-Eigenschaft**](caption-property.md) den angezeigten Text. Wenn weder die **VoiceCaption-** noch die **Caption-Eigenschaft** festgelegt ist, wird der Befehl nicht im Fenster "Sprachbefehle" angezeigt.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandsEx::GetVoiceCaption**](iagentcommandsex--getvoicecaption.md)


 

 