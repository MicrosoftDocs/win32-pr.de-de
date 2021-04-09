---
title: Iagentcommands GetCommand
description: Iagentcommands GetCommand
ms.assetid: 0f4a9152-d5dc-4045-b469-8a03f0369e34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e81043bb8dbe8a6d050f226d09f03b396d0f8f9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038981"
---
# <a name="iagentcommandsgetcommand"></a>Iagentcommands:: GetCommand

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetCommand(
   long dwCommandID,         // Command ID
   IUnknown ** ppunkCommand  // address of IUnknown interface
);                    
```

Ruft ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt aus der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwcommandid*
</dt> <dd>

Die ID eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung.

</dd> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Die Adresse der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommand**](iagentcommand.md)


 

 