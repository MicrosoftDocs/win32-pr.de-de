---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer das Menü für die Erweiterung in der Menüleiste Datei-Manager auswählt. Die Erweiterung kann diese Benachrichtigung verwenden, um Menüelemente zu initialisieren.
title: FMEVENT_INITMENU Nachricht (Wfext.h)
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
ms.openlocfilehash: 82ec9130a681bdfd36ff6259392c0608e4cde9cf
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842281"
---
# <a name="fmevent_initmenu-message"></a>FMEVENT \_ INITMENU-Nachricht

Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer das Menü für die Erweiterung in der Menüleiste Datei-Manager auswählt. Die Erweiterung kann diese Benachrichtigung verwenden, um Menüelemente zu initialisieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*Hmenu* 
</dt> <dd>

Ein Handle für die Menüleiste des Datei-Managers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL sollte 0 (null) zurückgeben, wenn diese Meldung verarbeitet wird.

## <a name="remarks"></a>Hinweise

Eine Erweiterungs-DLL empfängt diese Meldung nur, wenn der Benutzer das Menü der obersten Ebene auswählt. Wenn die Erweiterung Untermenüs enthält, muss sie gleichzeitig initialisiert werden, wenn das Menü der obersten Ebene initialisiert wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wfext.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> </dl>

 

 




