---
title: BM_GETIMAGE Meldung (Winuser.h)
description: Ruft ein Handle für das Bild (Symbol oder Bitmap) ab, das der Schaltfläche zugeordnet ist.
ms.assetid: 766ea1b0-418d-41b8-b31d-0fcc58e03893
keywords:
- BM_GETIMAGE Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 4b98ede304499aa97d9129957aa69a0991dee98565ff7827cdad4d0c1a82f19b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921260"
---
# <a name="bm_getimage-message"></a>BM \_ GETIMAGE-Nachricht

Ruft ein Handle für das Bild (Symbol oder Bitmap) ab, das der Schaltfläche zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des Bilds, das der Schaltfläche zugeordnet werden soll. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                      | Bedeutung              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="IMAGE_BITMAP"></span><span id="image_bitmap"></span><dl> <dt>**\_BILDBITMAP**</dt> </dl> | Eine Bitmap.<br/> |
| <span id="IMAGE_ICON"></span><span id="image_icon"></span><dl> <dt>**\_BILDSYMBOL**</dt> </dl>       | Symbol<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ggf. ein Handle für das Bild. Andernfalls ist es **NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**BM \_ SETIMAGE**](bm-setimage.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Schaltflächen](buttons.md)
</dt> </dl>

 

 





