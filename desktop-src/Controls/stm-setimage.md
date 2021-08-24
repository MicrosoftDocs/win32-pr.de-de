---
title: STM_SETIMAGE (Winuser.h)
description: Eine Anwendung sendet eine STM \_ SETIMAGE-Nachricht, um einem statischen Steuerelement ein neues Image zu zuordnen.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- STM_SETIMAGE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- STM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d48cc8aeb5e28ac67a6bbe25636be1a2f6f9b89f225568be02e517e1ad04dc55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078454"
---
# <a name="stm_setimage-message"></a>STM \_ SETIMAGE-Nachricht

Eine Anwendung sendet eine **STM \_ SETIMAGE-Nachricht,** um einem statischen Steuerelement ein neues Image zu zuordnen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Typ des Bilds an, das dem statischen Steuerelement zugeordnet werden soll. Dieser Parameter kann einen der folgenden Werte haben:



| Wert                                                                                                                                                                     | Bedeutung                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**\_BILDBITMAP**</dt> </dl>                | Bitmap.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**\_BILDCURSOR**</dt> </dl>                | Cursor.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**IMAGE \_ ENHMETAFILE**</dt> </dl> | Erweiterte Metadatei.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**\_BILDSYMBOL**</dt> </dl>                      | Symbol.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Bild, das dem statischen Steuerelement zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Handle für das Bild, das zuvor dem statischen Steuerelement zugeordnet war, sofern dies der Fall ist. andernfalls ist es **NULL.**

## <a name="remarks"></a>Hinweise

Um ein Bild einem statischen Steuerelement zuordnen zu können, muss das Steuerelement den richtigen Stil haben. In der folgenden Tabelle ist der für die einzelnen Bildtypen benötigte Stil dargestellt.



| Imagetyp         | Statisches Steuerelementformat |
|--------------------|----------------------|
| \_BILDBITMAP      | \_SS-BITMAP           |
| \_BILDCURSOR      | \_SS-SYMBOL             |
| IMAGE \_ ENHMETAFILE | SS \_ ENHMETAFILE      |
| \_BILDSYMBOL        | \_SS-SYMBOL             |



 

> [!IMPORTANT]
>
> In Version 6 der Microsoft Win32-Steuerelemente war eine Bitmap, die mithilfe der **STM \_ SETIMAGE-Nachricht** an ein statisches Steuerelement übergeben wurde, dieselbe Bitmap, die von einer nachfolgenden **STM \_ SETIMAGE-Nachricht zurückgegeben** wurde. Der Client ist dafür verantwortlich, alle Bitmaps zu löschen, die an ein statisches Steuerelement gesendet werden.
>
> Wenn Windows XP die in der **STM \_ SETIMAGE-Nachricht** übergebene Bitmap Pixel mit einem Alpha ungleich 0 (null) enthält, nimmt das statische Steuerelement eine Kopie der Bitmap an. Diese kopierte Bitmap wird von der nächsten **STM \_ SETIMAGE-Nachricht** zurückgegeben. Der Clientcode kann die an das statische Steuerelement übergebenen Bitmaps unabhängig nachverfolgen. Wenn jedoch die von **STM \_ SETIMAGE-Nachrichten** zurückgegebenen Bitmaps nicht überprüft und veröffentlicht werden, werden die Bitmaps weitergegeben.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**STM \_ GETIMAGE**](stm-getimage.md)
</dt> </dl>

 

 





