---
title: Iagentballoon getVisible
description: Iagentballoon getVisible
ms.assetid: 328af211-4ea4-482c-8487-42c8e4cd66b0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55fd8dbf6792d34b15f82ab6c402e9a0e7eb3ad3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856875"
---
# <a name="iagentballoongetvisible"></a>Iagentballoon:: getVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for word balloon
);                   // Visible setting
```

Bestimmt, ob die Wort Sprechblase sichtbar oder ausgeblendet ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*
</dt> <dd>

Adresse einer Variablen, die **true** empfängt, wenn die Wort Sprechblase sichtbar ist, und **false** , wenn Sie ausgeblendet ist.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentballoon:: setVisible**](iagentballoon--setvisible.md)


 

 




