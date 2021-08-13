---
title: IAgentCommand GetVoice
description: IAgentCommand GetVoice
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120e27996f06a0446f7aaab944df8638134990fffe951400d94c690f52f78cac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750427"
---
# <a name="iagentcommandgetvoice"></a>IAgentCommand::GetVoice

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

Ruft den Wert der [**Voicetext-Eigenschaft**](voice-property.md) für einen [**Befehl ab.**](/windows/desktop/lwef/the-command-object)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*
</dt> <dd>

Die Adresse eines BSTR, der die [**Voicetext-Eigenschaft**](voice-property.md) für einen [**Befehl empfängt.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

Auf [**einen Befehl,**](/windows/desktop/lwef/the-command-object) dessen [**Voice-Eigenschaft**](voice-property.md) und [**die Enabled-Eigenschaft**](enabled-property.md) auf **True** festgelegt ist, kann auf die Stimme zugegriffen werden. Wenn die [**Caption-Eigenschaft**](caption-property.md) ebenfalls festgelegt ist, wird sie im Fenster Sprachbefehle angezeigt. Wenn die [**Visible-Eigenschaft**](visible-property.md) auf **True festgelegt** ist, wird sie im Popupmenü des Zeichens angezeigt.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 