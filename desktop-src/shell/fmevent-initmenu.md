---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer das Menü für die Erweiterung in der Menüleiste des Datei-Managers auswählt. Die Erweiterung kann diese Benachrichtigung verwenden, um Menüelemente zu initialisieren.
title: FMEVENT_INITMENU (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_INITMENU
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8074a09f-ad94-4a7a-8c0b-965b0f8f6334
ms.openlocfilehash: 77b9aa668087f0c02042ccb7e5b822f68596404761d53ec682c76ef98d46c18e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459047"
---
# <a name="fmevent_initmenu-message"></a>FMEVENT \_ INITMENU-Nachricht

Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer das Menü für die Erweiterung in der Menüleiste des Datei-Managers auswählt. Die Erweiterung kann diese Benachrichtigung verwenden, um Menüelemente zu initialisieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*Hmenu* 
</dt> <dd>

Ein Handle für die Menüleiste des Datei-Managers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL sollte 0 (null) zurückgeben, wenn sie diese Meldung verarbeitet.

## <a name="remarks"></a>Hinweise

Eine Erweiterungs-DLL empfängt diese Meldung nur, wenn der Benutzer das Menü der obersten Ebene auswählt. Wenn die Erweiterung Untermenüs enthält, muss sie sie gleichzeitig initialisieren, wenn sie das Menü der obersten Ebene initialisiert.

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

 

 




