---
title: MM_MIXM_LINE_CHANGE Meldung (MMSYSTEM. h)
description: Die Meldung der mm \_ -mixm- \_ Zeilen \_ Änderung wird von einem Mischgerät gesendet, um eine Anwendung zu benachrichtigen, dass sich der Status einer audiozeile auf dem angegebenen Gerät geändert hat. Die Anwendung sollte die Anzeige und die zwischengespeicherten Werte für die angegebene Audiolinie aktualisieren.
ms.assetid: 68ada0be-9dc5-4edf-b924-ef0d10a1b79a
keywords:
- MM_MIXM_LINE_CHANGE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MIXM_LINE_CHANGE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92c4aa10d9934f8cf5f5747ecb4e4eb736af2655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345910"
---
# <a name="mm_mixm_line_change-message"></a>Meldung zur mm- \_ mixm- \_ Zeilen \_ Änderung

Die Meldung der **mm- \_ mixm- \_ Zeilen \_ Änderung** wird von einem Mischgerät gesendet, um eine Anwendung zu benachrichtigen, dass sich der Status einer audiozeile auf dem angegebenen Gerät geändert hat. Die Anwendung sollte die Anzeige und die zwischengespeicherten Werte für die angegebene Audiolinie aktualisieren.


```C++
MM_MIXM_LINE_CHANGE 
wParam = (WPARAM) hMixer 
lParam = (LPARAM) dwLineID 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hMixer"></span><span id="hmixer"></span><span id="HMIXER"></span>*hmixer*
</dt> <dd>

Handle für das Mischgerät, das die Benachrichtigungs Meldung gesendet hat.

</dd> <dt>

<span id="dwLineID"></span><span id="dwlineid"></span><span id="DWLINEID"></span>*dwlineid*
</dt> <dd>

Zeilen Bezeichner für die audiozeile, die den Zustand geändert hat. Dieser Bezeichner ist identisch mit dem **dwlineid** -Member der **mixerline**-Struktur, die von der **mixergetlineinfo**-Funktion zurückgegeben wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Anwendung muss ein Mischgerät öffnen und ein Rückruf Fenster angeben, um die **mm- \_ mixm- \_ Zeilen \_ Änderungs** Meldung zu empfangen.

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

 

 





