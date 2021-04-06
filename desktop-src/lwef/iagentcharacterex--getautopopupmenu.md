---
title: Iagentcharakteriex GetAutoPopupMenu
description: Iagentcharakteriex GetAutoPopupMenu
ms.assetid: c29bfd6e-c7eb-426e-be38-2fa0bdb13211
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c7a3b8d1075c596f27af17df34c7cb94d8a1ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947918"
---
# <a name="iagentcharacterexgetautopopupmenu"></a>Iagentcharakteriex:: GetAutoPopupMenu

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetAutoPopupMenu(
   long * pbAutoPopupMenu  // address of auto pop-up menu display setting
);
```

Ruft ab, ob der Server das Popup Menü des Zeichens automatisch anzeigt.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbAutoPopupMenu"></span><span id="pbautopopupmenu"></span><span id="PBAUTOPOPUPMENU"></span>*pbautopopupmenu*
</dt> <dd>

Adresse einer Variablen, die **true** empfängt, wenn der Microsoft-Agent-Server die Anzeige des Popup Menüs des Zeichens automatisch behandelt, andernfalls **false** .

</dd> </dl>

Wenn diese Eigenschaft auf **false** festgelegt ist, muss die Anwendung das Popup Menü mithilfe der [**iagentcharakteriex:: showPopupMenu**](iagentcharacterex--showpopupmenu.md) -Methode anzeigen.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex:: abtautopopupmenu**](iagentcharacterex--setautopopupmenu.md), [ **iagentcharakteriex:: showPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 




