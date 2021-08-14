---
title: IAgentCommands GetCount
description: IAgentCommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 810f9fc268bc13558e4e51a3b64dd6f5b1d54caa5a055d9c90b6a8d11c48b3c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749824"
---
# <a name="iagentcommandsgetcount"></a>IAgentCommands::GetCount

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

Ruft die Anzahl der [**Command-Objekte**](/windows/desktop/lwef/the-command-object) in einer [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Adresse einer Variablen, die die Anzahl der [**Befehle**](/windows/desktop/lwef/the-command-object) in einer [**Commands-Auflistung empfängt.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

*pdwCount* enthält nur die Anzahl von [**Befehlen,**](/windows/desktop/lwef/the-command-object) die Sie in Ihrer [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) definieren. Server- oder andere Clienteinträge sind nicht enthalten.

 

 