---
title: LVM_GETSTRINGWIDTH Meldung (kommstrg. h)
description: Bestimmt die Breite einer angegebenen Zeichenfolge unter Verwendung der aktuellen Schriftart des angegebenen Listenansicht-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getstringwidth-Makros senden.
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- Windows-Steuerelemente für LVM_GETSTRINGWIDTH Meldung
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
ms.openlocfilehash: 71e27512eb7a2a260976356ed2a128b48975f9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518653"
---
# <a name="lvm_getstringwidth-message"></a>LVM \_ getstringwidth-Nachricht

Bestimmt die Breite einer angegebenen Zeichenfolge unter Verwendung der aktuellen Schriftart des angegebenen Listenansicht-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getstringwidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) -Makros senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine NULL-terminierte Zeichenfolge.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Zeichen folgen Breite zurück, wenn erfolgreich, andernfalls 0 (null).

## <a name="remarks"></a>Bemerkungen

Die LVM \_ getstringwidth-Nachricht gibt die exakte Breite der angegebenen Zeichenfolge in Pixel zurück. Wenn Sie die zurückgegebene Zeichen folgen Breite als Spaltenbreite in der [**LVM-Nachricht \_ setcolumnwidth**](lvm-setcolumnwidth.md) verwenden, wird die Zeichenfolge abgeschnitten. Um die Spaltenbreite abzurufen, die die Zeichenfolge enthalten kann, ohne Sie zu kürzen, müssen Sie der zurückgegebenen Zeichen folgen Breite Auffüll Zeichen hinzufügen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVM \_ Getstringwidthw** (Unicode) und **LVM \_ getstringwidtha** (ANSI)<br/>     |



 

 





