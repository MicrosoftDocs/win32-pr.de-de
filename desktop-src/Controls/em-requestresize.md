---
title: EM_REQUESTRESIZE Nachricht (Richedit.h)
description: Erzwingt, dass ein Rich Edit-Steuerelement einen EN \_ REQUESTRESIZE-Benachrichtigungscode an das übergeordnete Fenster sendet.
ms.assetid: efc22771-9b9f-4a30-a906-f02095607c21
keywords:
- EM_REQUESTRESIZE Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EM_REQUESTRESIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7113f52e2fa3a293549443f779ba937bf20b85736c6751cd9ab77bdbecd45c3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440160"
---
# <a name="em_requestresize-message"></a>EM \_ REQUESTRESIZE-Nachricht

Erzwingt, dass ein Rich Edit-Steuerelement einen [**EN \_ REQUESTRESIZE-Benachrichtigungscode**](en-requestresize.md) an das übergeordnete Fenster sendet.

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

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung ist während der [**WM \_ SIZE-Verarbeitung**](/windows/desktop/winmsg/wm-size) für das übergeordnete Element eines steuerelements für die bottomless Rich Edit nützlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[**EN \_ REQUESTRESIZE**](en-requestresize.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**\_WM-GRÖßE**](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

