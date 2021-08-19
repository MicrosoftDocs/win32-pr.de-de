---
title: MM_MIM_ERROR Nachricht (Mmsystem.h)
description: Die MM \_ MIM \_ ERROR-Nachricht wird an ein Fenster gesendet, wenn eine ungültige FEHLERMELDUNG empfangen wird.
ms.assetid: 03760bfc-a4ef-48cd-97a9-1b93b56fc641
keywords:
- MM_MIM_ERROR nachricht Windows Multimedia
topic_type:
- apiref
api_name:
- MM_MIM_ERROR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15b2f615434d47a60297991e170a27acd2c6fabefcb5fed0b71624d373a35ed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117802418"
---
# <a name="mm_mim_error-message"></a>MM \_ MIM \_ FEHLERMELDUNG

Die **MM \_ MIM \_ ERROR-Meldung** wird an ein Fenster gesendet, wenn eine ungültige FEHLERMELDUNG empfangen wird.


```C++
MM_MIM_ERROR 
wParam = (WPARAM) hInput 
lParam = (LPARAM) (DWORD) lMidiMessage 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="hInput"></span><span id="hinput"></span><span id="HINPUT"></span>*hInput*
</dt> <dd>

Handle für das INPUT-Eingabegerät, das die ungültige Nachricht empfangen hat.

</dd> <dt>

<span id="lMidiMessage"></span><span id="lmidimessage"></span><span id="LMIDIMESSAGE"></span>*lMidiMessage*
</dt> <dd>

Ungültige FEHLERMELDUNG. Die Nachricht wird in einen **DWORD-Wert** mit dem ersten Byte der Nachricht im Low-Order-Byte gepackt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Music Instrument Digital Interface (INSTRUMENTS)](musical-instrument-digital-interface--midi.md)
</dt> <dt>

[MELDUNGSMELDUNGEN](midi-messages.md)
</dt> </dl>

 

 





