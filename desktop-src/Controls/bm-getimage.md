---
title: BM_GETIMAGE Meldung (Winuser. h)
description: Ruft ein Handle für das Bild (Symbol oder Bitmap) ab, das der Schaltfläche zugeordnet ist.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- Windows-Steuerelemente für BM_GETIMAGE Meldung
topic_type:
- apiref
api_name:
- BM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9319f5310b40ff76a011e1a06b2be1d41be611f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340968"
---
# <a name="bm_getimage-message"></a>BM \_ GetImage-Nachricht

Ruft ein Handle für das Bild (Symbol oder Bitmap) ab, das der Schaltfläche zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des Bilds, das der Schaltfläche zugeordnet werden soll. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                      | Bedeutung              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**Bild \_ Bitmap**</dt> </dl> | Eine Bitmap.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**Bild \_ Symbol**</dt> </dl>       | Symbol<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist, sofern vorhanden, ein Handle für das Bild. Andernfalls ist der Wert **null**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**BM- \_ Zeitrahmen**](bm-setimage.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Schaltflächen](buttons.md)
</dt> </dl>

 

 





