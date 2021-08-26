---
title: IAgentNotifySinkEx AgentPropertyChange
description: IAgentNotifySinkEx AgentPropertyChange
ms.assetid: 8293cd77-320a-4b57-b3d8-52bc450d6aa0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d7a0737428d20b297d83ac92c3ce6957dac0390c719c17b96a00983a0a57af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961490"
---
# <a name="iagentnotifysinkexagentpropertychange"></a>IAgentNotifySinkEx::AgentPropertyChange

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT AgentPropertyChange(
);
```

Benachrichtigt eine Clientanwendung, wenn der Benutzer eine Microsoft Agent-Eigenschafteneinstellung ändert.

-   Kein Rückgabewert.

Wenn der Benutzer eine Microsoft Agent-Eigenschafteneinstellung im Microsoft Agent-Eigenschaftenblatt ändert, sendet der Server dieses Ereignis an alle Clients, es sei denn, der Server ist derzeit angehalten.

## <a name="see-also"></a>Weitere Informationen

[**IAgentNotifySinkEx::D efaultCharacterChange**](iagentnotifysinkex--defaultcharacterchange.md)


 

 




