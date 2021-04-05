---
title: CB_SETDROPPEDWIDTH Meldung (Winuser. h)
description: Eine Anwendung sendet die CB- \_ setdroppeer-DTH-Nachricht, um die minimale zulässige Breite (in Pixel) des Listen Felds eines Kombinations Felds mit dem Format "CBS \_ Dropdown" oder "CBS \_ DropDownList" festzulegen.
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- Windows-Steuerelemente für CB_SETDROPPEDWIDTH Meldung
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c4f5ce64bfb1b48e9e811027792a11e4358edc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858888"
---
# <a name="cb_setdroppedwidth-message"></a>CB- \_ setdroppeer-DTH-Meldung

Eine Anwendung sendet die **CB- \_ setdroppeer-DTH** -Nachricht, um die minimale zulässige Breite (in Pixel) des Listen Felds eines Kombinations Felds mit dem Format " [**CBS \_ Dropdown**](combo-box-styles.md) " oder " [**CBS \_ DropDownList**](combo-box-styles.md) " festzulegen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die minimale zulässige Breite des Listen Felds in Pixel.

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, entspricht der Rückgabewert der neuen Breite des Listen Felds.

Wenn die Nachricht fehlschlägt, ist der Rückgabewert CB \_ Err.

## <a name="remarks"></a>Bemerkungen

Standardmäßig ist die zulässige Mindestbreite für das Dropdown-Listenfeld NULL. Die Breite des Listen Felds ist entweder die minimale zulässige Breite oder die Kombinations Feldbreite, je nachdem, welcher Wert größer ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CB \_ getdroppeer-DTH**](cb-getdroppedwidth.md)
</dt> </dl>

 

 





