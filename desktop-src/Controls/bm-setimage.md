---
title: BM_SETIMAGE (Winuser.h)
description: Ordnet der Schaltfläche ein neues Bild (Symbol oder Bitmap) zu.
ms.assetid: bf05e684-63d0-4583-960b-f329edafb151
keywords:
- BM_SETIMAGE meldungssteuerelemente Windows
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
ms.openlocfilehash: 7b8948c73c04d3b01230a47ab91529764c9e20281e4f45803f71d82f59dedb14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674813"
---
# <a name="bm_setimage-message"></a>BM \_ SETIMAGE-Nachricht

Ordnet der Schaltfläche ein neues Bild (Symbol oder Bitmap) zu.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des Bilds, das der Schaltfläche zugeordnet werden soll. Dieser Parameter kann einer der folgenden Werte sein:

-   \_BILDBITMAP
-   \_BILDSYMBOL

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Handle (**HICON** oder **HBITMAP**) zum Bild, das der Schaltfläche zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Der Rückgabewert ist ein Handle für das Bild, das zuvor der Schaltfläche zugeordnet war, sofern dies der Fall ist. andernfalls ist es **NULL.**

## <a name="remarks"></a>Hinweise

Die Darstellung von Text, einem Symbol oder beidem auf einem Schaltflächen-Steuerelement hängt von den [**BS \_ ICON-**](button-styles.md) und [**BS \_ BITMAP-Formatvorlagen**](button-styles.md) ab und davon, ob die **BM \_ SETIMAGE-Nachricht** aufgerufen wird. Die möglichen Ergebnisse lauten wie folgt:



| BS \_ ICON oder BS BITMAP \_ Set? | BM \_ SETIMAGE aufgerufen? | Ergebnis              |
|-----------------------------|----------------------|---------------------|
| Ja                         | Ja                  | Nur Symbol anzeigen.     |
| Nein                          | Ja                  | Symbol und Text anzeigen. |
| Ja                         | Nein                   | Nur Text anzeigen.     |
| Nein                          | Nein                   | Nur Text anzeigen      |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**BM \_ GETIMAGE**](bm-getimage.md)
</dt> </dl>

 

 





