---
title: Iagentcommands GetCount
description: Iagentcommands GetCount
ms.assetid: 17140eda-17b0-49c2-8d50-5a38a553191a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ece3e007b644b370ee721cef2d273fa50d43ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390140"
---
# <a name="iagentcommandsgetcount"></a>Iagentcommands:: GetCount

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetCount(
   long * pdwCount  // address of count of commands
);                    
```

Ruft die Anzahl der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte [**in einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung ab.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pdwCount"></span><span id="pdwcount"></span><span id="PDWCOUNT"></span>*pdwCount*
</dt> <dd>

Adresse einer Variablen, die die Anzahl der [**Befehle**](/windows/desktop/lwef/the-command-object) in einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung empfängt.

</dd> </dl>

*pdwCount* umfasst nur die Anzahl der [**Befehle**](/windows/desktop/lwef/the-command-object) , die Sie in der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definieren. Server-oder andere Client Einträge sind nicht eingeschlossen.

 

 