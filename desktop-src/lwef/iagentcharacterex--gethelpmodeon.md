---
title: Iagentcharakteriex gethelpmudeon
description: Iagentcharakteriex gethelpmudeon
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072f657ba5ac93d057474f062f73101f2559aed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207269"
---
# <a name="iagentcharacterexgethelpmodeon"></a>Iagentcharakteriex:: gethelpmudeon

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

Ruft ab, ob der kontextabhängige Hilfe Modus für das Zeichen on ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbhelpmudeon*
</dt> <dd>

Adresse einer Variablen, die **true** empfängt, wenn der Hilfe Modus für das Zeichen on ist, andernfalls **false** .

</dd> </dl>

Wenn diese Eigenschaft auf **true** festgelegt ist, ändert sich der Mauszeiger in das kontextabhängige Hilfe Bild, wenn er über das Zeichen oder über das Popupmenü für das Zeichen verschoben wird. Wenn der Benutzer auf das Zeichen klickt oder zieht oder auf ein Element im Popup Menü des Zeichens klickt, löst der Server das [**iagentnotifysinkex:: helpcomplete**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) -Ereignis aus und beendet den Hilfe Modus.

Im Hilfe Modus sendet der Server die Ereignisse " [**iagentnotifysink:: Click**](iagentnotifysink--click.md)", " [**iagentnotifysink::D ragstart**](iagentnotifysink--dragstart.md)", " [**iagentnotifysink::D ragcomplete**](iagentnotifysink--dragcomplete.md)" und " [**iagentnotifysink:: Command**](iagentnotifysink--command.md) " nicht, es sei denn, die [**GetAutoPopupMenu**](https://www.bing.com/search?q=**GetAutoPopupMenu**) -Eigenschaft gibt " **true**" zurück. In diesem Fall sendet der Server das **iagentnotifysink:: Click** -Ereignis (der Hilfe Modus wird nicht beendet), sondern nur für die Rechte Maustaste, damit Sie das Popup Menü anzeigen können.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex:: Setup**](iagentcharacterex--sethelpmodeon.md)


 

 




