---
title: TVN_ASYNCDRAW Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Strukturansicht-Steuerelement an das übergeordnete Steuerelement gesendet, wenn beim Zeichnen eines Symbols oder Overlay ein Fehler aufgetreten ist. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 209bfffb-e57d-435d-98a1-8b117c4969b1
keywords:
- Windows-Steuerelemente für TVN_ASYNCDRAW Benachrichtigungs
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
ms.openlocfilehash: 25a8b04db2e4efbd78d6176214ecd9088f1bc30c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344102"
---
# <a name="tvn_asyncdraw-notification-code"></a>TVN \_ asyncdraw-Benachrichtigungs Code

Wird von einem Strukturansicht-Steuerelement an das übergeordnete Steuerelement gesendet, wenn beim Zeichnen eines Symbols oder Overlay ein Fehler aufgetreten ist. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
TVN_ASYNCDRAW
        
    pnmTVAsynchDraw =  (NMTVASYNCDRAW *) lParam; 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmtvasyncdraw**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) -Struktur. Die **nmtvasyncdraw** -Struktur enthält den Grund, warum das Zeichnen nicht ausgeführt werden konnte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Das Strukturansicht-Steuerelement muss über den erweiterten Stil " [**TVs \_ Ex \_ drawimageasync**](tree-view-control-window-extended-styles.md) " verfügen. Beachten Sie, dass dies dem LVN-LVN-Flag von List-View \_ und dem zugehörigen Stil entspricht.

Dieses Steuerelement wird nicht asynchron gezeichnet. Asynchronous wird in dem Kontext verwendet, in dem das Strukturansicht-Steuerelement ein Bild nicht synchron extrahiert, wenn es nicht verfügbar ist. (Beispielsweise ist das Bild möglicherweise nicht verfügbar, wenn das Strukturansicht-Steuerelement eine Liste mit geringer Dichte verwendet, da das Bild möglicherweise entladen wird.) Wenn ein Bild nicht verfügbar ist, fragt das Steuerelement stattdessen das übergeordnete Element ab, welche Aktion ausgeführt werden soll, indem das übergeordnete Element eine TVN \_ asyncdraw-Benachrichtigung mit einer [**nmtvasyncdraw**](/windows/win32/api/commctrl/ns-commctrl-nmtvasyncdraw) -Struktur gesendet wird. Der **HR** -Member dieser Struktur beschreibt den Grund, warum das Zeichnen des Steuer Elements fehlgeschlagen ist. Ein **HR** -Ergebnis von E \_ Pending bedeutet, dass das Image überhaupt nicht vorhanden ist (das Abbild muss extrahiert werden). Erfolg gibt an, dass das Bild vorhanden ist, aber nicht die erforderliche Bildqualität.

Das übergeordnete Element legt den **dwretflags** -Member der Struktur fest, um dem Steuerelement mitzuteilen, wie der Vorgang fortgesetzt wird Beispielsweise kann das übergeordnete Element ein anderes Bild im **iretimageindex** -Member zurückgeben, damit das Steuerelement gezeichnet wird. In diesem Fall legt das übergeordnete Element den **dwretflags** -Member auf adrf \_ DrawImage fest. Wenn das Steuerelement feststellt, dass das zurückgegebene Bild nicht extrahiert wurde, kann eine andere TVN- \_ asyncdraw-Benachrichtigung vom Steuerelement gesendet werden.

Wenn ein Bild nicht verfügbar ist, besteht die Idee hinter asynchronen darin, dass das übergeordnete Element die Extraktion im Hintergrund durchführen soll, damit der UI-Thread, d. h. der Thread, in dem sich das Steuerelement befindet, durch Extrahieren nicht blockiert wird. Das übergeordnete Element gibt möglicherweise adrf \_ drawnothing an das Steuerelement zurück und startet dann einen Hintergrund Thread, um das Symbol zu extrahieren. Nach dem extrahieren kann das übergeordnete Element das Symbol im TreeView-Steuerelement mit dem Makro [**TreeView \_ SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setitem)festlegen. Dies bewirkt, dass die Strukturansicht das Element für ungültig erklärt und es schließlich mit dem extrahierten Bild in der Bildliste neu zeichnet.

Im folgenden Codebeispiel, das als Teil eines größeren Programms verwendet werden soll, wird veranschaulicht, wie ein übergeordnetes Element in dieser Benachrichtigung zwei mögliche Rückgabecodes von einem-Steuerelement verarbeiten kann und wie Sie entscheiden, welche Aktion das Steuerelement ausführen sollte. Das Festlegen von **dwretflags** wird nicht angezeigt.


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
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





