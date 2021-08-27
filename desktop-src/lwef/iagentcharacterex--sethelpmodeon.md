---
title: IAgentCharacterEx SetHelpModeOn
description: IAgentCharacterEx SetHelpModeOn
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aacbdf9c0ea9737bb73ba7a99e0839e1435379e42536a82aa30c2ca034a28860
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062030"
---
# <a name="iagentcharacterexsethelpmodeon"></a>IAgentCharacterEx::SetHelpModeOn

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

Legt den kontextsensitiven Hilfemodus für das Zeichen auf fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bHelpModeOn*
</dt> <dd>

Hilfemodusflag. Wenn dieser Parameter true **ist,** aktiviert Microsoft Agent den Hilfemodus für das Zeichen.

</dd> </dl>

Wenn Sie diese Eigenschaft auf **True** festlegen, ändert sich der Mauszeiger in das kontextsensitive Hilfebild, wenn er über das Zeichen oder über das Popupmenü für das Zeichen verschoben wird. Wenn der Benutzer auf das Zeichen klickt oder es zieht oder auf ein Element im Popupmenü des Zeichens klickt, löst der Server das [**IAgentNotifySinkEx::HelpComplete-Ereignis**](iagentnotifysinkex--helpcomplete.md) aus und beendet den Hilfemodus.

Im Hilfemodus sendet der Server [](click-event.md)die Click-, [**DragStart-,**](/windows/desktop/lwef/dragstart-event) [**DragComplete-**](https://www.bing.com/search?q=**DragComplete**)und [**Command-Ereignisse**](command-event.md) nur, wenn die [**GetAutoPopupMenu-Eigenschaft**](iagentcharacterex--getautopopupmenu.md) **TRUE zurückgibt.** In diesem Fall sendet der Server das **Click-Ereignis** (beendet den Hilfemodus nicht), sondern nur für die rechte Maustaste, damit Sie das Popupmenü anzeigen können.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch Ihre Clientanwendung. Die Einstellung wirkt sich nicht auf andere Clients des Zeichens oder anderer Zeichen Ihrer Clientanwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacterEx::GetHelpModeOn**](iagentcharacterex--gethelpmodeon.md), [ **IAgentNotifySinkEx::HelpComplete**](iagentnotifysinkex--helpcomplete.md)


 

 