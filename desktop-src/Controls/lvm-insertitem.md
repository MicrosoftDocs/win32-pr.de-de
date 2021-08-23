---
title: LVM_INSERTITEM-Nachricht (Commctrl.h)
description: Fügt ein neues Element in ein Listenansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des ListView \_ InsertItem-Makros senden.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- LVM_INSERTITEM Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9408a8d09adca2a097281b13e56241c66a68521dcef0892502d7f8d0e14d25e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575710"
---
# <a name="lvm_insertitem-message"></a>LVM \_ INSERTITEM-Nachricht

Fügt ein neues Element in ein Listenansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ InsertItem-Makros**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**LVITEM-Struktur,**](/windows/win32/api/commctrl/ns-commctrl-lvitema) die die Attribute des Listenansichtselements angibt. Verwenden Sie das **iItem-Element,** um den nullbasierten Index anzugeben, an dem das neue Element eingefügt werden soll. Wenn dieser Wert größer als die Anzahl der elemente ist, die derzeit in der Listenansicht enthalten sind, wird das neue Element am Ende der Liste angefügt und dem richtigen Index zugewiesen. Überprüfen Sie den Rückgabewert der Nachricht, um den tatsächlichen Index zu ermitteln, der dem Element zugewiesen ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg den Index des neuen Elements zurück, andernfalls -1.

## <a name="remarks"></a>Hinweise

Sie können [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) oder **LVM \_ INSERTITEM** nicht verwenden, um Unteritems einzufügen. Der **iSubItem-Member** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) muss 0 (null) sein. Informationen zum Festlegen von Unteritems finden Sie unter [**LVM \_ SETITEM.**](lvm-setitem.md)

Wenn für ein Listenansichtssteuerelement der [**LVS \_ EX \_ CHECKBOXES-Stil**](extended-list-view-styles.md) festgelegt ist, werden alle Werte ignoriert, die in den Bits 12 bis 15 des **Zustandsmembers** der [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) platziert werden. Wenn ein Element mit diesem Stilsatz hinzugefügt wird, wird es immer auf den status unchecked festgelegt.

Wenn ein Listenansichtssteuerelement entweder über das Fensterformat [**LVS \_ SORTASCENDING**](list-view-window-styles.md) oder [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) verfügt, schlägt eine **LVM \_ INSERTITEM-Nachricht** fehl, wenn Sie versuchen, ein Element einzufügen, das LPSTR \_ TEXTCALLBACK als Wert für das **pszText-Element** enthält.

Die **LVM \_ INSERTITEM-Nachricht** fügt das neue Element an der richtigen Position in der Sortierreihenfolge ein, wenn die folgenden Bedingungen gelten:

-   Sie verwenden einen der LVS \_ SORTXXX-Stile.
-   Sie verwenden nicht den [**LVS \_ OWNERDRAW-Stil.**](list-view-window-styles.md)
-   Der **pszText-Member** der Struktur, auf die von **pitem** gezeigt wird, ist nicht auf LPSTR \_ TEXTCALLBACK festgelegt.

Wenn die [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) keine LVIF \_ GROUPID im **Maskenmember** enthält, lautet der Wert des **iGroupId-Members** standardmäßig I \_ GROUPIDCALLBACK.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ INSERTITEMW** (Unicode) und **LVM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





