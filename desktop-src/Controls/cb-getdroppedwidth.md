---
title: CB_GETDROPPEDWIDTH Meldung (Winuser. h)
description: Ruft die minimale zulässige Breite (in Pixel) des Listen Felds eines Kombinations Felds mit dem Format "CBS \_ Dropdown" oder "CBS DropDownList" in Pixel ab \_ .
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- Windows-Steuerelemente für CB_GETDROPPEDWIDTH Meldung
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 299b360348a6bf7378fdfc9bc9f0959b01366642
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040606"
---
# <a name="cb_getdroppedwidth-message"></a>CB \_ getdroppeer-DTH-Meldung

Ruft die minimale zulässige Breite (in Pixel) des Listen Felds eines Kombinations Felds mit dem Format " [**CBS \_ Dropdown**](combo-box-styles.md) " oder " [**CBS \_ DropDownList**](combo-box-styles.md) " in Pixel ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, entspricht der Rückgabewert der Breite in Pixel.

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

[**CB \_ setdroppeer-DTH**](cb-setdroppedwidth.md)
</dt> </dl>

 

 





