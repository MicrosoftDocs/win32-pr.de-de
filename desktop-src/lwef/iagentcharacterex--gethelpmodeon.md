---
title: IAgentCharacterEx GetHelpModeOn
description: IAgentCharacterEx GetHelpModeOn
ms.assetid: 848c9e75-6e4c-487c-b01c-36ec6314d0c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb78cf535fbfd7e28ab797c887c8e1548d3fd18dce03fb6b64d888c7e304c0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118750785"
---
# <a name="iagentcharacterexgethelpmodeon"></a>IAgentCharacterEx::GetHelpModeOn

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT GetHelpModeOn(
   long * pbHelpModeOn  // address of help mode setting
);
```

Ruft ab, ob der kontextsensitive Hilfemodus für das Zeichen aktiviert ist.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="pbHelpModeOn"></span><span id="pbhelpmodeon"></span><span id="PBHELPMODEON"></span>*pbHelpModeOn*
</dt> <dd>

Die Adresse einer Variablen, die **TRUE empfängt,** wenn der Hilfemodus für das Zeichen aktiviert ist, und **False,** wenn dies nicht der Fall ist.

</dd> </dl>

Wenn diese Eigenschaft auf **True** festgelegt ist, ändert sich der Mauszeiger in das kontextsensitive Hilfebild, wenn er über das Zeichen oder über das Popupmenü für das Zeichen verschoben wird. Wenn der Benutzer auf das Zeichen klickt oder es zieht oder auf ein Element im Popupmenü des Zeichens klickt, löst der Server das [**IAgentNotifySinkEx::HelpComplete-Ereignis**](https://www.bing.com/search?q=**IAgentNotifySinkEx::HelpComplete**) aus und beendet den Hilfemodus.

Im Hilfemodus sendet der Server keine [**IAgentNotifySink::Click-,**](iagentnotifysink--click.md) [**IAgentNotifySink::D ragStart-,**](iagentnotifysink--dragstart.md) [**IAgentNotifySink::D ragComplete-**](iagentnotifysink--dragcomplete.md)und [**IAgentNotifySink::Command-Ereignisse,**](iagentnotifysink--command.md) es sei denn, die [**GetAutoPopupMenu-Eigenschaft**](https://www.bing.com/search?q=**GetAutoPopupMenu**) gibt **True zurück.** In diesem Fall sendet der Server das **IAgentNotifySink::Click-Ereignis** (beendet den Hilfemodus nicht), sondern nur für die rechte Maustaste, damit Sie das Popupmenü anzeigen können.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md)


 

 




