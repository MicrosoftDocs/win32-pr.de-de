---
title: IAgentCharacterEx SetAutoPopupMenu
description: IAgentCharacterEx SetAutoPopupMenu
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a616bd95836d8f8131aaccabe0bb6db4f35a5caf22c480c17908935d80f2b12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118477958"
---
# <a name="iagentcharacterexsetautopopupmenu"></a>IAgentCharacterEx::SetAutoPopupMenu

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

Legt fest, ob der Server automatisch das Popupmenü des Zeichens anzeigt.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bAutoPopupMenu*
</dt> <dd>

Das Anzeigeflag des automatischen Popupmenüs. Wenn dieser Parameter **True** ist, zeigt der Microsoft-Agent automatisch das Popupmenü des Zeichens an, wenn der Benutzer mit der rechten Maustaste auf das Zeichen oder das Taskleistensymbol des Zeichens klickt.

</dd> </dl>

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

Wenn Sie diese Eigenschaft auf **False** festlegen, können Sie Ein eigenes Menübehandlungsverhalten erstellen. Um das Menü nach dem Festlegen dieser Eigenschaft auf **False** anzuzeigen, verwenden Sie die [**IAgentCharacterEx::ShowPopupMenu-Methode.**](iagentcharacterex--showpopupmenu.md)

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx::GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [ **IAgentCharacterEx::ShowPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 




