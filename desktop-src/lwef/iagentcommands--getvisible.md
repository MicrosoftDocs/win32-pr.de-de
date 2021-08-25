---
title: IAgentCommands GetVisible
description: IAgentCommands GetVisible
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d63ef62a0e57539d633d595901c6cfde1a252ac9ef369f9f56bc3ddaaeea0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961910"
---
# <a name="iagentcommandsgetvisible"></a>IAgentCommands::GetVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

Ruft den Wert der [**Visible-Eigenschaft**](visible-property.md) für eine [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Die Adresse einer Variablen, die den Wert der [**Visible-Eigenschaft**](visible-property.md) für eine [**Commands-Auflistung empfängt.**](/windows/desktop/lwef/the-commands-collection-object)

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [ **IAgentCommands::SetCaption**](iagentcommands--setcaption.md)


 

 