---
title: Iagentcharakteriex-"stautopopupmenu"
description: Iagentcharakteriex-"stautopopupmenu"
ms.assetid: f2402b1f-a39b-4fd5-a046-c0a3245d2af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcfd1bd7ea0b02f226ed6f0365b466577807a193
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947774"
---
# <a name="iagentcharacterexsetautopopupmenu"></a>Iagentcharakteriex:: abtautopopupmenu

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetAutoPopupMenu(
   long bAutoPopupMenu,  // auto pop-up menu display setting
);
```

Legt fest, ob der Server das Popup Menü des Zeichens automatisch anzeigt.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bAutoPopupMenu"></span><span id="bautopopupmenu"></span><span id="BAUTOPOPUPMENU"></span>*bautopopupmenu*
</dt> <dd>

Das automatische Popup-Menü Anzeigeflag. Wenn dieser Parameter **true** ist, zeigt der Microsoft-Agent automatisch das Popup Menü des Zeichens an, wenn der Benutzer mit der rechten Maustaste auf das Symbol der Taskleiste des Zeichens oder Zeichens klickt.

</dd> </dl>

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

Wenn Sie diese Eigenschaft auf " **false**" festlegen, können Sie ein eigenes Menü Verarbeitungs Verhalten erstellen. Um das Menü nach dem Festlegen dieser Eigenschaft auf **false** anzuzeigen, verwenden Sie die [**iagentcharakteriex:: showPopupMenu**](iagentcharacterex--showpopupmenu.md) -Methode.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex:: GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md), [ **iagentcharakteriex:: showPopupMenu**](iagentcharacterex--showpopupmenu.md)


 

 




