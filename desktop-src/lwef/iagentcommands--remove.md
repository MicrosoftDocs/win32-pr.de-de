---
title: IAgentCommands Remove
description: IAgentCommands Remove
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5875d1377aecc7e28554bac6aae1ccb2b4f515f730a6ab1b0b3a83cec7573418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477193"
---
# <a name="iagentcommandsremove"></a>IAgentCommands::Remove

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

Entfernt den angegebenen [**Befehl**](/windows/desktop/lwef/the-command-object) aus einer [**Commands-Auflistung.**](/windows/desktop/lwef/the-commands-collection-object)

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

Die ID eines [**Befehls,**](/windows/desktop/lwef/the-command-object) der aus der [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) entfernt werden soll.

</dd> </dl>

Wenn Sie einen [**Befehl**](/windows/desktop/lwef/the-command-object) aus einer [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) entfernen, wird er auch aus dem Popupmenü und dem **Fenster "Sprachbefehle"** entfernt, wenn Ihre Anwendung eingabeaktiv ist.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)


 

 