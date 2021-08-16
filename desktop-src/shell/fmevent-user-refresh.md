---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer im Menü Ansicht im Datei-Manager den Befehl Aktualisieren ausgibt. Die Erweiterung kann diese Benachrichtigung verwenden, um ihr Menü zu aktualisieren.
title: FMEVENT_USER_REFRESH-Nachricht (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_USER_REFRESH
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b8fb4ce8-d284-4558-82a4-488d4d833bcb
ms.openlocfilehash: 9e2f514494ae8040c7bdb97f556555bd7f32794e4259300da240956ff6fcfe98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094145"
---
# <a name="fmevent_user_refresh-message"></a>FMEVENT \_ USER \_ REFRESH-Nachricht

Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer im Menü **Ansicht** im Datei-Manager den Befehl **Aktualisieren** ausgibt. Die Erweiterung kann diese Benachrichtigung verwenden, um ihr Menü zu aktualisieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL sollte 0 (null) zurückgeben, wenn sie diese Nachricht verarbeitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




