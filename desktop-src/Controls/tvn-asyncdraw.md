---
title: TVN_ASYNCDRAW Benachrichtigungscode (Commctrl.h)
description: Wird von einem Strukturansicht-Steuerelement an das übergeordnete Element gesendet, wenn das Zeichnen eines Symbols oder einer Überlagerung fehlgeschlagen ist. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- TVN_ASYNCDRAW Benachrichtigungscode Windows Steuerelementen
topic_type:
- apiref
api_name:
- TVN_ASYNCDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4d929977e1a14a5ada96232fa054c2689d27f1eaa026b64c974d51f5a2c38c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060100"
---
# <a name="tvn_asyncdraw-notification-code"></a>TVN \_ ASYNCDRAW-Benachrichtigungscode

Wird von einem Strukturansicht-Steuerelement an das übergeordnete Element gesendet, wenn das Zeichnen eines Symbols oder einer Überlagerung fehlgeschlagen ist. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMTVASYNCDRAW-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) Die **NMTVASYNCDRAW-Struktur** enthält den Grund für den Fehler beim Zeichnen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Das Strukturansicht-Steuerelement muss über den erweiterten [**TVS \_ EX \_ DRAWIMAGEASYNC-Stil**](tree-view-control-window-extended-styles.md) verfügen. Beachten Sie, dass dies dem LVN ASYNCDRAWN-Flag der Listenansicht und dem \_ entsprechenden Stil entspricht.

Dieses Steuerelement wird nicht asynchron ge zeichnen. Asynchron wird in dem Kontext verwendet, in dem das Strukturansicht-Steuerelement ein Bild nicht synchron extrahiert, wenn es nicht verfügbar ist. (Beispielsweise ist das Bild möglicherweise nicht verfügbar, wenn das Strukturansicht-Steuerelement eine Sparsebildliste verwendet, da das Bild entladen werden kann.) Wenn ein Bild nicht verfügbar ist, fragt das Steuerelement das übergeordnete Element stattdessen synchron, welche Aktion ausgeführt werden soll, indem es dem übergeordneten Element eine \_ TVN-ASYNCDRAW-Benachrichtigung mit einer [**NMTVASYNCDRAW-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) sendet. Der **hr-Member** dieser -Struktur beschreibt den Grund für den Fehler beim Zeichnen des Steuerelements. Ein **Hr-Ergebnis** von E PENDING bedeutet, dass das Bild überhaupt nicht vorhanden \_ ist (das Bild muss extrahiert werden). Erfolg gibt an, dass das Bild vorhanden ist, aber nicht mit der erforderlichen Imagequalität.

Das übergeordnete Element legt das **dwRetFlags-Element** der -Struktur fest, um das Steuerelement darüber zu informieren, wie fortzufahren ist. Beispielsweise kann das übergeordnete Element ein anderes Bild im **iRetImageIndex-Element** zurückgeben, damit das Steuerelement ge zeichnen kann. In diesem Fall legt das übergeordnete Element das **dwRetFlags-Element** auf ADRF \_ DRAWIMAGE fest. Wenn das Steuerelement ermittelt, dass das zurückgegebene Bild nicht extrahiert wurde, kann das Steuerelement eine weitere \_ TVN-ASYNCDRAW-Benachrichtigung senden.

Wenn ein Bild nicht verfügbar ist, ist die Idee hinter asynchron, dem übergeordneten Element die Extraktion im Hintergrund zu ermöglichen, damit die Extraktion den UI-Thread nicht blockiert, d.&a0;b. den Thread, in dem sich das Steuerelement befindet. Das übergeordnete Element kann ADRF DRAWNOTHING an das Steuerelement zurückgeben und dann einen \_ Hintergrundthread starten, um das Symbol zu extrahieren. Nach der Extraktion kann das übergeordnete Element das Symbol im Treeview-Steuerelement mit dem Makro [**TreeView \_ SetItem festlegen.**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem) Dies führt dazu, dass die Strukturansicht das Element ungültig macht und es schließlich mit dem extrahierten Bild in der Bildliste neu anpaint.

Das folgende Codebeispiel, das als Teil eines größeren Programms verwendet werden soll, zeigt, wie ein übergeordnetes Element zwei mögliche Rückgabecodes in dieser Benachrichtigung durch ein -Steuerelement verarbeiten und entscheiden kann, welche Aktion das Steuerelement ausführen soll. Das **Festlegen von dwRetFlags** wird nicht angezeigt.


```
case TVN_ASYNCDRAW:

   NMTVASYNCDRAW *pnm =  (NMTVASYNCDRAW *)lParam
   short dwDrawSuccessFlags = ShortFromResult(pnm->hr);

   if (dwDrawSuccessFlags & ILDRF_IMAGELOWQUALITY)
   {
        // Need to re-extract the icon
   }

   if (dwDrawSuccessFlags & ILDRF_OVERLAYLOWQUALITY)
   {
        // Need to re-extract the overlay
   }
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





