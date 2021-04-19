---
title: LVM_INSERTITEM Meldung (kommstrg. h)
description: Fügt ein neues Element in ein Listenansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des ListView \_ InsertItem-Makros senden.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- Windows-Steuerelemente für LVM_INSERTITEM Meldung
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
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346748"
---
# <a name="lvm_insertitem-message"></a>LVM \_ InsertItem-Nachricht

Fügt ein neues Element in ein Listenansicht-Steuerelement ein. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur, die die Attribute des Listen Ansichts Elements angibt. Verwenden Sie den **iItem** -Member, um den NULL basierten Index anzugeben, an dem das neue Element eingefügt werden soll. Wenn dieser Wert größer als die Anzahl der aktuell in der ListView enthaltenen Elemente ist, wird das neue Element an das Ende der Liste angefügt und dem richtigen Index zugewiesen. Überprüfen Sie den Rückgabewert der Nachricht, um den dem Element zugewiesenen tatsächlichen Index zu bestimmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Index des neuen Elements zurück, wenn erfolgreich, andernfalls-1.

## <a name="remarks"></a>Bemerkungen

Sie können " [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) " oder " **LVM \_ InsertItem** " nicht verwenden, um unter Elemente einzufügen. Der **iSubItem** -Member der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur muss NULL sein. Weitere Informationen zum Festlegen von unter Elementen finden Sie unter [**LVM \_**](lvm-setitem.md) -Element.

Wenn für ein Listenansicht-Steuerelement die [**LVS \_ Ex- \_ Kontrollkästchen**](extended-list-view-styles.md) festgelegt sind, werden alle Werte, die in Bits 12 bis 15 des **State** -Members der [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur platziert werden, ignoriert. Wenn ein Element mit diesem Stilsatz hinzugefügt wird, wird es immer auf den deaktivierten Zustand festgelegt.

Wenn ein Listenansicht-Steuerelement entweder den [**LVS \_ SortAscending**](list-view-window-styles.md) -oder [**LVS \_ sortabsteig**](list-view-window-styles.md) enden Fenster Stil aufweist, schlägt eine **LVM \_ InsertItem** -Nachricht fehl, wenn Sie versuchen, ein Element einzufügen, das LPSTR \_ textcallback als Wert für das zugehörige **pszText** -Element aufweist.

Die **LVM- \_ InsertItem** -Nachricht fügt das neue Element an der richtigen Position in der Sortierreihenfolge ein, wenn die folgenden Bedingungen erfüllt sind:

-   Sie verwenden einen der LVS \_ sortxxx-Stile.
-   Sie verwenden nicht den [**LVS-Besitzer \_ Zeichnungs**](list-view-window-styles.md) Stil.
-   Der **pszText** -Member der Struktur, auf die von **pitem** gezeigt wird, ist nicht auf "LPSTR textcallback" festgelegt \_ .

Wenn die [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur keine lvif- \_ GroupID im **Mask** -Member enthält, ist der Wert des **igroupid** -Members \_ standardmäßig "groupidcallback".

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ Insertitemw** (Unicode) und **LVM \_ insertitema** (ANSI)<br/>             |



 

 





