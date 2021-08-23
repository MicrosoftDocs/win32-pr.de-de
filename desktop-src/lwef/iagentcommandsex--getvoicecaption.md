---
title: IAgentCommandsEx GetVoiceCaption
description: IAgentCommandsEx GetVoiceCaption
ms.assetid: 0e505295-386a-421f-a43c-6da03c8a2b6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec2a6d5138b9b7074d1c9a2002f45a0076fe5d957ae5e47d865c693f73e8b37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609432"
---
# <a name="iagentcommandsexgetvoicecaption"></a>IAgentCommandsEx::GetVoiceCaption

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption
);
```

Ruft die [**VoiceCaption**](voicecaption-property.md) für ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*
</dt> <dd>

Die Adresse eines BSTR, der den Wert des [**Beschriftungstexts**](caption-property.md) empfängt, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigt wird.

</dd> </dl>

Der zurückgegebene Text ist für das [**Command-Objekt**](/windows/desktop/lwef/the-command-object) festgelegt und wird im Fenster Sprachbefehle angezeigt, wenn Ihre Clientanwendung eingabeaktiv ist.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandsEx::SetVoiceCaption**](iagentcommandsex--setvoicecaption.md)


 

 