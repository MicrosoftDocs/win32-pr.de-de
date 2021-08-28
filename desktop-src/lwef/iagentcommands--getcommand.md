---
title: IAgentCommands GetCommand
description: IAgentCommands GetCommand
ms.assetid: 0f4a9152-d5dc-4045-b469-8a03f0369e34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ae5e8a92ce8d4a8e04ff049569195e5a2baa21ec3bc398f5fa6ba6ef3c1e3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609690"
---
# <a name="iagentcommandsgetcommand"></a>IAgentCommands::GetCommand

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetCommand(
   long dwCommandID,         // Command ID
   IUnknown ** ppunkCommand  // address of IUnknown interface
);                    
```

Ruft ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) aus der [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Die ID eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) in der [**Commands-Auflistung.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*Iunknown*
</dt> <dd>

Die Adresse der [**IUnknown-Schnittstelle**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) für das [**Command-Objekt.**](/windows/desktop/lwef/the-command-object)

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommand**](iagentcommand.md)


 

 