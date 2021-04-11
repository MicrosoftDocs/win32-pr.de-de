---
title: BM_SETIMAGE Meldung (Winuser. h)
description: Verknüpft ein neues Bild (Symbol oder Bitmap) mit der Schaltfläche.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- Windows-Steuerelemente für BM_SETIMAGE Meldung
topic_type:
- apiref
api_name:
- BM_SETIMAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65d083c4fb509d51eb017bb7d3d38fab07b4c006
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103134"
---
# <a name="bm_setimage-message"></a>BM- \_ abtimage-Nachricht

Verknüpft ein neues Bild (Symbol oder Bitmap) mit der Schaltfläche.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des Bilds, das der Schaltfläche zugeordnet werden soll. Dieser Parameter kann einen der folgenden Werte aufweisen:

-   Bild \_ Bitmap
-   Bild \_ Symbol

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle (**HICON** oder **hBitmap**) für das Bild, das der Schaltfläche zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Handle für das Bild, das zuvor der Schaltfläche zugeordnet ist, sofern vorhanden. Andernfalls ist der Wert **null**.

## <a name="remarks"></a>Bemerkungen

Die Darstellung von Text, ein Symbol oder beides auf einem Schaltflächen-Steuerelement hängt vom Buch [**-und dem Karten- \_**](button-styles.md) [**\_ Bitmapformat**](button-styles.md) ab und gibt an, ob die BM-ablaufnachricht aufgerufen wird. **\_** Die folgenden Ergebnisse sind möglich:



| Das SB-Symbol oder das SB- \_ \_ bitmapset? | BM- \_ Image aufgerufen? | Ergebnis              |
|-----------------------------|----------------------|---------------------|
| Ja                         | Ja                  | Nur Symbol anzeigen.     |
| Nein                          | Ja                  | Symbol und Text anzeigen. |
| Ja                         | Nein                   | Nur Text anzeigen.     |
| Nein                          | Nein                   | Nur Text anzeigen      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BM- \_ GetImage**](bm-getimage.md)
</dt> </dl>

 

 





