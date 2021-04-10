---
title: STM_GETIMAGE Meldung (Winuser. h)
description: Eine Anwendung sendet eine STM \_ GetImage-Nachricht zum Abrufen eines Handles zum Bild (Symbol oder Bitmap), das einem statischen Steuerelement zugeordnet ist.
ms.assetid: eb5fe67a-09be-4c13-89c6-0e2f23e8c081
keywords:
- Windows-Steuerelemente für STM_GETIMAGE Meldung
topic_type:
- apiref
api_name:
- STM_GETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77fe0c3d00a2a957530160a5ce5a21b8a1cf84e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040161"
---
# <a name="stm_getimage-message"></a>STM \_ GetImage-Nachricht

Eine Anwendung sendet eine **STM \_ GetImage** -Nachricht zum Abrufen eines Handles zum Bild (Symbol oder Bitmap), das einem statischen Steuerelement zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Typ des abzurufenden Bilds an. Dieser Parameter kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                                     | Bedeutung                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**Bild \_ Bitmap**</dt> </dl>                | Bitmap.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**Bild \_ Cursor**</dt> </dl>                | Hand.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**Image- \_ enhmetafile**</dt> </dl> | Erweiterte Metadatei.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**Bild \_ Symbol**</dt> </dl>                      | Angezeigt.<br/>              |



 

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

[**STM- \_ Zeitrahmen**](stm-setimage.md)
</dt> </dl>

 

 





