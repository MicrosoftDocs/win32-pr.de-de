---
title: EM_SHOWSCROLLBAR (Richedit.h)
description: Blendet eine der Bildlaufleisten im Hostfenster eines Rich-Edit-Steuerelements ein oder aus.
ms.assetid: 0a6ec010-4870-4faf-9dc2-1da961dc8194
keywords:
- EM_SHOWSCROLLBAR meldungssteuerelemente Windows
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
ms.openlocfilehash: dc3988ced825fed457549fc9f662a418295de7df6085f04c3e71255ca4ad54c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831141"
---
# <a name="em_showscrollbar-message"></a>EM \_ SHOWSCROLLBAR-Meldung

Blendet eine der Bildlaufleisten im Hostfenster eines Rich-Edit-Steuerelements ein oder aus.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt an, welche Bildlaufleiste angezeigt werden soll: horizontal oder vertikal. Dieser Parameter muss **SB \_ VERT** oder **SB \_ HORZ sein.**

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt an, ob die Scrollleiste angezeigt oder ausblenden werden soll. Geben **Sie TRUE** an, um die Scrollleiste zu zeigen, und **FALSE,** um sie auszublenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Methode ist nur gültig, wenn das Steuerelement aktiv ist. Aufrufe, die bei inaktiven Steuerelementen vorgenommen werden, können fehlschlagen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ GETSCROLLPOS**](em-getscrollpos.md)
</dt> <dt>

[**EM \_ SETSCROLLPOS**](em-setscrollpos.md)
</dt> </dl>

 

 





