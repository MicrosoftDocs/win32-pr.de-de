---
title: IAgentCommand SetCaption
description: IAgentCommand SetCaption
ms.assetid: f4fdd37a-28b4-4e00-885c-58addedec659
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ffccf42a972ec9635c929fb954d58bfaff967af364d24ae505e1dbb2bd8772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976360"
---
# <a name="iagentcommandsetcaption"></a>IAgentCommand::SetCaption

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetCaption(
   BSTR bszCaption  // Caption setting for Command
);
```

Legt den [**Beschriftungstext**](caption-property.md) fest, der für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angezeigt wird.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*
</dt> <dd>

Ein BSTR, der den Text für die [**Caption-Eigenschaft**](caption-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object)angibt.

</dd> </dl>

Durch Festlegen der [**Caption-Eigenschaft**](caption-property.md) für einen [**Befehl**](/windows/desktop/lwef/the-command-object) wird definiert, wie sie im Popupmenü des Zeichens angezeigt wird, wenn die [**Visible-Eigenschaft**](visible-property.md) auf **True** festgelegt ist und Ihre Anwendung nicht der eingabeaktive Client ist. Um einen Zugriffsschlüssel (unlineiertes mnemonic) für Ihre **Beschriftung** anzugeben, schließen Sie ein ampersand (&)-Zeichen vor dieses Zeichen ein. Damit sie auswählbar ist, muss die [**Enabled-Eigenschaft**](enabled-property.md) auf **True** festgelegt werden.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)


 

 