---
title: EM_GETEVENTMASK (Richedit.h)
description: Ruft die Ereignismaske für ein Rich-Edit-Steuerelement ab. Die Ereignismaske gibt an, welche Benachrichtigungscodes das Steuerelement an das übergeordnete Fenster sendet.
ms.assetid: cdf99f2a-e747-4b0e-9235-2719477c3ce2
keywords:
- EM_GETEVENTMASK meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_GETEVENTMASK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4261869276015151e920e96e6c419675a1bce097384d6a918c2eac2b8005393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049230"
---
# <a name="em_geteventmask-message"></a>EM \_ GETEVENTMASK-Nachricht

Ruft die Ereignismaske für ein Rich-Edit-Steuerelement ab. Die Ereignismaske gibt an, welche Benachrichtigungscodes das Steuerelement an das übergeordnete Fenster sendet.

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

Diese Meldung gibt die Ereignismaske für das Rich-Edit-Steuerelement zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**Rich Edit Control-Ereignismaskenflags**](rich-edit-control-event-mask-flags.md)
</dt> </dl>

 

 





