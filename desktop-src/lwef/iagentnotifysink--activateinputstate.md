---
title: IAgentNotifySink ActivateInputState
description: IAgentNotifySink ActivateInputState
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a2d86ae3d79a51bc2adc3b3d32ee719502087c4c723e2c1778103596b97d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749582"
---
# <a name="iagentnotifysinkactivateinputstate"></a>IAgentNotifySink::ActivateInputState

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

Benachrichtigt eine Clientanwendung, dass sich der aktive Eingabezustand eines Zeichens geändert hat.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*
</dt> <dd>

Bezeichner des Zeichens, dessen Eingabeaktivierungsstatus geändert wurde.

</dd> <dt>

<span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bActivated*
</dt> <dd>

Eingabe des aktiven Flags. Dieser boolesche Wert ist **True,** wenn das Zeichen, auf das *von dwCharID* verwiesen wird, eingabeaktiv wird. und **False,** wenn das Zeichen seinen aktiven Eingabezustand verloren hat.

</dd> </dl>

 

 




