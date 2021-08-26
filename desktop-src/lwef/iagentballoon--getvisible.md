---
title: IAgentBalloon GetVisible
description: IAgentBalloon GetVisible
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 939026026e18e550ca18838977f00a8878db9039595d9eadd0b30b88235a0248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962320"
---
# <a name="iagentballoongetvisible"></a>IAgentBalloon::GetVisible

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

Bestimmt, ob das Wort balloon sichtbar oder ausgeblendet ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*
</dt> <dd>

Adresse einer Variablen, die **TRUE empfängt,** wenn das Wort Balloon sichtbar ist, und **False,** wenn ausgeblendet.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentBalloon::SetVisible**](iagentballoon--setvisible.md)


 

 




