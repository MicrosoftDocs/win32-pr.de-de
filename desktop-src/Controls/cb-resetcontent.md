---
title: CB_RESETCONTENT (Winuser.h)
description: Entfernt alle Elemente aus dem Listenfeld und bearbeitet das Steuerelement eines Kombinationsfelds.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- CB_RESETCONTENT von Windows-Steuerelementen
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4918437d7b0d347e071386486b31e5f4b9d948b4ff55b4c6eea6e3afe93fb1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832248"
---
# <a name="cb_resetcontent-message"></a>CB \_ RESETCONTENT-Nachricht

Entfernt alle Elemente aus dem Listenfeld und bearbeitet das Steuerelement eines Kombinationsfelds.

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

Diese Meldung gibt immer CB \_ OK zurück.

## <a name="remarks"></a>Hinweise

Wenn Sie das Kombinationsfeld mit einem vom Besitzer gezeichneten Stil erstellen, aber ohne den [**CBS \_ HASSTRINGS-Stil,**](combo-box-styles.md) erhält der Besitzer des Kombinationsfelds für jedes Element im Kombinationsfeld eine [**WM \_ DELETEITEM-Meldung.**](wm-deleteitem.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ DELETESTRING**](cb-deletestring.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





