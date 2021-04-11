---
title: EM_SHOWSCROLLBAR Meldung (RichEdit. h)
description: Blendet eine der Bild Lauf leisten im Host Fenster eines Rich-Edit-Steuer Elements ein oder aus.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- Windows-Steuerelemente für EM_SHOWSCROLLBAR Meldung
topic_type:
- apiref
api_name:
- EM_SHOWSCROLLBAR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb569b194be3d744db67f98b71a595ba18a2d3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949775"
---
# <a name="em_showscrollbar-message"></a>EM- \_ ShowScrollbar-Meldung

Blendet eine der Bild Lauf leisten im Host Fenster eines Rich-Edit-Steuer Elements ein oder aus.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, welche Bild Lauf Leiste angezeigt werden soll: horizontal oder vertikal. Dieser Parameter muss **SB \_ Vert** oder **SB \_ Horz** sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt an, ob die Bild Lauf Leiste angezeigt oder ausgeblendet werden soll. Geben Sie **true** an, um die Scrollleiste anzuzeigen, und **false** , um sie auszublenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode ist nur gültig, wenn das Steuerelement direkt aktiv ist. Aufrufe, die während des inaktiven Steuer Elements ausgeführt werden, können fehlschlagen

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ getscrollpos**](em-getscrollpos.md)
</dt> <dt>

[**EM- \_ setscrollpos**](em-setscrollpos.md)
</dt> </dl>

 

 





