---
title: Iagentcommandwindow getVisible
description: Iagentcommandwindow getVisible
ms.assetid: a69a2aaa-5a3a-46b8-b505-49609a2aa5ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c66c6d7bf2ee59512f478fd8daa7cee882515690
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341648"
---
# <a name="iagentcommandwindowgetvisible"></a>Iagentcommandwindow:: getVisible

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for Visible setting for 
);                   // Voice Commands Window
```

Bestimmt, ob das Sprachbefehle Fenster sichtbar oder ausgeblendet ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbvisible*
</dt> <dd>

Adresse einer Variablen, die **true** erhält, wenn das Sprachbefehle Fenster sichtbar ist, oder **false** , wenn Sie ausgeblendet ist.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommandwindow:: setVisible**](iagentcommandwindow--setvisible.md)


 

 




