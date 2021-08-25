---
title: EM_EXLIMITTEXT Nachricht (Richedit.h)
description: Legt eine Obergrenze auf die Textmenge fest, die der Benutzer in ein Rich-Edit-Steuerelement eingeben oder einfügen kann.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- EM_EXLIMITTEXT Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_EXLIMITTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f9879323f3feade3ece536cd130b274b423c98aebedd6b6f5ef1497d995d07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915680"
---
# <a name="em_exlimittext-message"></a>EM \_ EXLIMITTEXT-Nachricht

Legt eine Obergrenze auf die Textmenge fest, die der Benutzer in ein Rich-Edit-Steuerelement eingeben oder einfügen kann.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die maximale Textmenge an, die eingegeben werden kann. Wenn dieser Parameter 0 (null) ist, wird das Standardmaximum verwendet, d.h. 64.000 Zeichen. Ein COM-Objekt zählt als einzelnes Zeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der von der **EM \_ EXLIMITTEXT-Nachricht** festgelegte Textgrenzwert beschränkt nicht die Textmenge, die Sie mithilfe der [**EM \_ STREAMIN-Nachricht**](em-streamin.md) in ein Rich Edit-Steuerelement streamen können, wobei *lParam* auf SF TEXT festgelegt \_ ist. Sie schränkt jedoch die Textmenge ein, die Sie in ein Rich Edit-Steuerelement streamen können, indem Sie die **EM \_ STREAMIN-Nachricht** verwenden, wobei *lParam* auf SF RTF festgelegt \_ ist.

Bevor **EM \_ EXLIMITTEXT** aufgerufen wird, beträgt das Standardlimit für die Textmenge, die ein Benutzer eingeben kann, 32.767 Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ STREAMIN**](em-streamin.md)
</dt> </dl>

 

 





