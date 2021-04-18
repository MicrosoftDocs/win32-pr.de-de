---
title: MM_MIXM_CONTROL_CHANGE Meldung (MMSYSTEM. h)
description: Die Änderungen an der mm \_ mixm- \_ Steuerungs \_ Änderung werden von einem Mischgerät gesendet, um eine Anwendung zu benachrichtigen, dass sich der Zustand eines Steuer Elements, das einer audiozeile zugeordnet ist, geändert hat. Die Anwendung sollte die Anzeige und die zwischengespeicherten Werte für das angegebene Steuerelement aktualisieren.
ms.assetid: 921c55a7-86c0-43d1-b817-bfbd3c4bb28b
keywords:
- MM_MIXM_CONTROL_CHANGE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIXM_CONTROL_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12daa4d9e107a9ba687331731ee9fd7e6f0dc886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341004"
---
# <a name="mm_mixm_control_change-message"></a>Meldung zum Ändern des mm \_ mixm- \_ Steuer Elements \_

Die **Änderungen an der mm \_ mixm- \_ Steuerungs \_ Änderung** werden von einem Mischgerät gesendet, um eine Anwendung zu benachrichtigen, dass sich der Zustand eines Steuer Elements, das einer audiozeile zugeordnet ist, geändert hat. Die Anwendung sollte die Anzeige und die zwischengespeicherten Werte für das angegebene Steuerelement aktualisieren.


```C++
MM_MIXM_CONTROL_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwControlID 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hmixer*
</dt> <dd>

Handle für das Mischgerät (**hmixer**), das die Benachrichtigungs Meldung gesendet hat.

</dd> <dt>

<span id="dwControlID"></span><span id="dwcontrolid"></span><span id="DWCONTROLID"></span>*dwcontrolid*
</dt> <dd>

Steuerelement Bezeichner für das Mixer-Steuerelement, das den Zustand geändert hat Dieser Bezeichner ist identisch mit dem **dwcontrolid** -Member der **mixercontrol**-Struktur, die von der Funktion "**mixergetlinecontrols**" zurückgegeben wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Anwendung muss ein Mischgerät öffnen und ein Rückruf Fenster angeben, um die Meldung zum **Ändern des mm \_ mixm- \_ Steuer \_** Elements zu empfangen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Audiomixer](audio-mixers.md)
</dt> <dt>

[Audiomischmeldungen](audio-mixer-messages.md)
</dt> </dl>

 

 





