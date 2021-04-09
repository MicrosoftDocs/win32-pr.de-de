---
title: Iagentcharakteriex
description: Iagentcharakteriex
ms.assetid: d4d42122-3d27-40c4-8770-0de105e5d933
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674fc8dcca3bca2f44c0928474d8684e77fc6e9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101498"
---
# <a name="iagentcharacterexsethelpmodeon"></a>Iagentcharakteriex:: Setup

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetHelpModeOn(
   long bHelpModeOn  // help mode setting
);
```

Legt den kontextbezogenen Hilfe Modus für das Zeichen fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bHelpModeOn"></span><span id="bhelpmodeon"></span><span id="BHELPMODEON"></span>*bhelpmudeon*
</dt> <dd>

Hilfe Modus-Flag. Wenn dieser Parameter den Wert **true** hat, schaltet der Microsoft-Agent den Hilfe Modus für das Zeichen ein.

</dd> </dl>

Wenn Sie diese Eigenschaft auf **true** festlegen, ändert sich der Mauszeiger in das kontextabhängige Hilfe Bild, wenn es über das Zeichen oder über das Popup Menü für das Zeichen verschoben wird. Wenn der Benutzer auf das Zeichen klickt oder zieht oder auf ein Element im Popup Menü des Zeichens klickt, löst der Server das [**iagentnotifysinkex:: helpcomplete**](iagentnotifysinkex--helpcomplete.md) -Ereignis aus und beendet den Hilfe Modus.

Im Hilfe Modus sendet der Server das [**Click**](click-event.md)-, [**DragStart**](/windows/desktop/lwef/dragstart-event)-, [**dragcomplete**](https://www.bing.com/search?q=**DragComplete**)-und [**Command**](command-event.md) -Ereignis nicht, es sei denn, die [**GetAutoPopupMenu**](iagentcharacterex--getautopopupmenu.md) -Eigenschaft gibt **true** zurück. In diesem Fall sendet der Server das **Click** -Ereignis (der Hilfe Modus wird nicht beendet), sondern nur für die Rechte Maustaste, sodass Sie das Popup Menü anzeigen können.

Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharakteriex:: gethelpmudeon**](iagentcharacterex--gethelpmodeon.md), [ **iagentnotifysinkex:: helpcomplete**](iagentnotifysinkex--helpcomplete.md)


 

 