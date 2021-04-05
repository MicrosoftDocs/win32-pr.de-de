---
title: CB_RESETCONTENT Meldung (Winuser. h)
description: Entfernt alle Elemente aus dem Listenfeld und bearbeitet das Steuerelement eines Kombinations Felds.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- Windows-Steuerelemente für CB_RESETCONTENT Meldung
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
ms.openlocfilehash: 3567f31ef98fffe42e53c4811acc786d41ae9f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858890"
---
# <a name="cb_resetcontent-message"></a>CB \_ resetcontent-Meldung

Entfernt alle Elemente aus dem Listenfeld und bearbeitet das Steuerelement eines Kombinations Felds.

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

Diese Meldung gibt immer den Wert CB \_ okay zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie das Kombinations Feld mit einem vom Besitzer gezeichneten Stil, aber ohne den [**CBS \_ hasstrings**](combo-box-styles.md) -Stil erstellen, empfängt der Besitzer des Kombinations Felds eine [**WM \_ DeleteItem**](wm-deleteitem.md) -Meldung für jedes Element im Kombinations Feld.

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

[**CB \_ deletestring**](cb-deletestring.md)
</dt> <dt>

[**WM- \_ DeleteItem**](wm-deleteitem.md)
</dt> </dl>

 

 





