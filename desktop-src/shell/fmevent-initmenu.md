---
description: Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer das Menü für die Erweiterung in der Menüleiste des Datei-Managers auswählt. Die Erweiterung kann diese Benachrichtigung verwenden, um Menü Elemente zu initialisieren.
title: FMEVENT_INITMENU Meldung (WF. h)
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
ms.openlocfilehash: 4bbb959feeb2c1bf99eaa999b4c51b69b0d0cf63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214304"
---
# <a name="fmevent_initmenu-message"></a>Meldung zu "smevent \_ InitMenu"

Wird an eine Erweiterungs-DLL gesendet, wenn der Benutzer das Menü für die Erweiterung in der Menüleiste des Datei-Managers auswählt. Die Erweiterung kann diese Benachrichtigung verwenden, um Menü Elemente zu initialisieren.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*HMENU* 
</dt> <dd>

Ein Handle für die Menüleiste des Datei-Managers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Erweiterungs-DLL sollte NULL zurückgeben, wenn Sie diese Nachricht verarbeitet.

## <a name="remarks"></a>Bemerkungen

Eine Erweiterungs-DLL empfängt diese Nachricht nur, wenn der Benutzer das Menü der obersten Ebene auswählt. Wenn die Erweiterung Untermenüs enthält, muss Sie gleichzeitig initialisiert werden, wenn Sie das Menü der obersten Ebene initialisieren.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WF. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**"F"**](fmextensionproc.md)
</dt> </dl>

 

 




