---
title: LVM_GETSTRINGWIDTH (Commctrl.h)
description: Bestimmt die Breite einer angegebenen Zeichenfolge unter Verwendung der aktuellen Schriftart des angegebenen Listenansicht-Steuerelements. Sie können diese Nachricht explizit oder mithilfe des \_ ListView-Makros GetStringWidth senden.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- LVM_GETSTRINGWIDTH meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9024cab94f59e543351e06d49ec058435ae369b6b746b1dc3fb2cd0472e3d57e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019308"
---
# <a name="lvm_getstringwidth-message"></a>LVM \_ GETSTRINGWIDTH-Nachricht

Bestimmt die Breite einer angegebenen Zeichenfolge unter Verwendung der aktuellen Schriftart des angegebenen Listenansicht-Steuerelements. Sie können diese Nachricht explizit oder mithilfe des [**\_ ListView-Makros GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine auf NULL beendete Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Zeichenfolgenbreite zurück, wenn erfolgreich, andernfalls 0 (null).

## <a name="remarks"></a>Hinweise

Die LVM \_ GETSTRINGWIDTH-Nachricht gibt die genaue Breite der angegebenen Zeichenfolge in Pixel zurück. Wenn Sie die zurückgegebene Zeichenfolgenbreite als Spaltenbreite in der [**LVM \_ SETCOLUMNWIDTH-Meldung**](lvm-setcolumnwidth.md) verwenden, wird die Zeichenfolge abgeschnitten. Um die Spaltenbreite abzurufen, die die Zeichenfolge enthalten kann, ohne sie zu schneiden, müssen Sie der zurückgegebenen Zeichenfolgenbreite Auf padding hinzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ GETSTRINGWIDTHW** (Unicode) und **LVM \_ GETSTRINGWID WIEGE** (ANSI)<br/>     |



 

 





