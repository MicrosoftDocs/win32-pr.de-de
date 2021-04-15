---
title: EM_EXLIMITTEXT Meldung (RichEdit. h)
description: Legt eine Obergrenze für den Text fest, der vom Benutzer in ein Rich-Edit-Steuerelement eingefügt oder eingefügt werden kann.
ms.assetid: 66fcdbb9-99ac-4122-b89c-be4aef80fbae
keywords:
- Windows-Steuerelemente für EM_EXLIMITTEXT Meldung
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
ms.openlocfilehash: 49c4ebb554e3aa3139a66ca63970356e1261a23f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477598"
---
# <a name="em_exlimittext-message"></a>EM \_ exlimittext-Nachricht

Legt eine Obergrenze für den Text fest, der vom Benutzer in ein Rich-Edit-Steuerelement eingefügt oder eingefügt werden kann.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt die maximale Menge an Text an, die eingegeben werden kann. Wenn dieser Parameter NULL ist, wird das Standard Maximum verwendet, das 64 KB groß ist. Ein COM-Objekt zählt als einzelnes Zeichen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das durch die **EM \_ exlimittext** -Nachricht festgelegte Text Limit schränkt nicht die Menge an Text ein, die Sie in ein Rich-Edit-Steuerelement mithilfe der [**EM- \_ StreamIn**](em-streamin.md) -Nachricht streamen können, wobei *LPARAM* auf SF Text festgelegt ist \_ . Allerdings wird die Menge des Texts, den Sie in ein Rich-Edit-Steuerelement streamen können, mithilfe der **EM- \_ StreamIn** -Nachricht mit *LPARAM* , die auf SF RTF festgelegt ist, eingeschränkt \_ .

Bevor **EM \_ exlimittext** aufgerufen wird, ist der Standard Grenzwert für die Text Menge, die ein Benutzer eingeben kann, 32.767 Zeichen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM- \_ StreamIn**](em-streamin.md)
</dt> </dl>

 

 





