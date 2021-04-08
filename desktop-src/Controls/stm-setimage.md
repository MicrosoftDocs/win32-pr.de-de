---
title: STM_SETIMAGE Meldung (Winuser. h)
description: Eine Anwendung sendet eine STM \_ SetImage-Nachricht, um ein neues Bild einem statischen Steuerelement zuzuordnen.
ms.assetid: d3e7c5d4-f621-40f6-9558-7fb699e8b489
keywords:
- Windows-Steuerelemente für STM_SETIMAGE Meldung
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
ms.openlocfilehash: 27c4f9c216d2e987727a1e2fa9bc6de12a823d52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949547"
---
# <a name="stm_setimage-message"></a>STM- \_ abtimage-Nachricht

Eine Anwendung sendet eine **STM \_ SetImage** -Nachricht, um ein neues Bild einem statischen Steuerelement zuzuordnen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Typ des Bilds an, das dem statischen Steuerelement zugeordnet werden soll. Dieser Parameter kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                                     | Bedeutung                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**Bild \_ Bitmap**</dt> </dl>                | Bitmap.<br/>            |
| <span id="IMAGE_CURSOR"></span><span id="image_cursor"></span><dl> <dt>**Bild \_ Cursor**</dt> </dl>                | Hand.<br/>            |
| <span id="IMAGE_ENHMETAFILE"></span><span id="image_enhmetafile"></span><dl> <dt>**Image- \_ enhmetafile**</dt> </dl> | Erweiterte Metadatei.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**Bild \_ Symbol**</dt> </dl>                      | Angezeigt.<br/>              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Bild, das dem statischen Steuerelement zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Handle für das Bild, das zuvor dem statischen Steuerelement zugeordnet ist, sofern vorhanden. Andernfalls ist der Wert **null**.

## <a name="remarks"></a>Bemerkungen

Zum Zuordnen eines Bilds zu einem statischen Steuerelement muss das Steuerelement über den richtigen Stil verfügen. In der folgenden Tabelle wird der für jeden Bildtyp benötigte Stil angezeigt.



| Imagetyp         | Stil des statischen Steuer Elements |
|--------------------|----------------------|
| Bild \_ Bitmap      | SS- \_ Bitmap           |
| Bild \_ Cursor      | SS- \_ Symbol             |
| Image- \_ enhmetafile | SS-" \_ enhmetafile"      |
| Bild \_ Symbol        | SS- \_ Symbol             |



 

> [!IMPORTANT]
>
> In Version 6 der Win32-Steuerelemente von Microsoft war eine Bitmap, die an ein statisches Steuerelement mithilfe der STM-ablaufnachricht übergeben wurde, dieselbe Bitmap, die von einer nachfolgenden **STM \_** -ablaufsnachricht zurückgegeben wurde. **\_** Der Client ist dafür verantwortlich, jede Bitmap zu löschen, die an ein statisches Steuerelement gesendet wird.
>
> Wenn in Windows XP die in der STM-ablaufmeldungs Meldung über gegebene Bitmap Pixel mit einem Alpha Wert ungleich 0 (null) enthält, nimmt das statische Steuerelement eine Kopie der Bitmap an. **\_** Diese kopierte Bitmap wird von der nächsten **STM- \_ logtimage** -Nachricht zurückgegeben. Der Client Code kann die an das statische Steuerelement übergebenen Bitmaps unabhängig nachverfolgen, aber wenn er die von **STM \_ SetImage** -Nachrichten zurückgegebenen Bitmaps nicht überprüft und freigibt, werden die Bitmaps kompromittiert.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**STM \_ GetImage**](stm-getimage.md)
</dt> </dl>

 

 





