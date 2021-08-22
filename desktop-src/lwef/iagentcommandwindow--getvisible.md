---
title: IAgentCommandWindow GetVisible
description: IAgentCommandWindow GetVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 949591bc22c93711af19ce18cb024ede9714335f249839eb4819a73e231e0d83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976240"
---
# <a name="iagentcommandwindowgetvisible"></a>IAgentCommandWindow::GetVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

Bestimmt, ob das Fenster "Sprachbefehle" sichtbar oder ausgeblendet ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Adresse einer Variablen, die **True** empfängt, wenn das Fenster "Sprachbefehle" sichtbar ist, oder **FALSE,** wenn es ausgeblendet ist.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCommandWindow::SetVisible**](iagentcommandwindow--setvisible.md)


 

 




