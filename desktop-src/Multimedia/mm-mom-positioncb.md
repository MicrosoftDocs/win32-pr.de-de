---
title: MM_MOM_POSITIONCB Meldung (MMSYSTEM. h)
description: Die "mm \_ MOM \_ positioncb"-Nachricht wird an ein Fenster gesendet, wenn ein mevt \_ F- \_ Rückruf Ereignis im MIDI-Ausgabestream erreicht wird.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- MM_MOM_POSITIONCB-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86fd6f34ab44d307bbbb0e5fc9fd61d083ccda4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949481"
---
# <a name="mm_mom_positioncb-message"></a>MM \_ MOM \_ positioncb-Meldung

Die " **mm \_ MOM \_ positioncb** "-Nachricht wird an ein Fenster gesendet, wenn ein mevt \_ F- \_ Rückruf Ereignis im MIDI-Ausgabestream erreicht wird.


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpmidihdr*
</dt> <dd>

Ein Zeiger auf eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, die das Ereignis identifiziert, das den Rückruf verursacht hat. Der **dwOffset** -Member gibt den Offset des Ereignisses an.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*LParam*
</dt> <dd>

Bleiben Verwenden Sie nicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Wiedergabe des Streampuffers wird auch dann fortgesetzt, wenn die Rückruffunktion ausgeführt wird. Alle Ereignisse nach dem mevt \_ F \_ -Rückruf Ereignis im Puffer werden zeitlich geplant und gesendet, unabhängig davon, wie viel Zeit in der Rückruffunktion aufgewendet wird.

Wenn Positions Rückrufe schneller generiert werden, als Sie von Ihrer Anwendung verarbeitet werden können, kann der **dwOffset** -Member der [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur auf ein Ereignis verweisen, das Ihre Anwendung noch nicht verarbeitet hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>MMSYSTEM. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MIDI-Nachrichten](midi-messages.md)
</dt> </dl>

 

