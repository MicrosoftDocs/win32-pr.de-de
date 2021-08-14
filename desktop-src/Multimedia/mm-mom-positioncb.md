---
title: MM_MOM_POSITIONCB Meldung (Mmsystem.h)
description: Die MM \_ MOM \_ POSITIONCB-Nachricht wird an ein Fenster gesendet, wenn ein MEVT \_ F \_ CALLBACK-Ereignis im AUSGABESTREAM erreicht wird.
ms.assetid: afd2ba4c-ff6a-4e47-a7e8-a0da62650963
keywords:
- MM_MOM_POSITIONCB nachricht Windows Multimedia
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
ms.openlocfilehash: 4f68afecddd9b6ca8a0e5f6305b430b059b93db5a2abb966c0a7aed9ab350f7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807160"
---
# <a name="mm_mom_positioncb-message"></a>MM \_ MOM \_ POSITIONCB-Meldung

Die **MM \_ MOM \_ POSITIONCB-Nachricht** wird an ein Fenster gesendet, wenn ein MEVT \_ F \_ CALLBACK-Ereignis im AUSGABESTREAM erreicht wird.


```C++
MM_MOM_POSITIONCB 
wParam = (WPARAM) lpMidiHdr 
lParam = reserved 
```



## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="lpMidiHdr"></span><span id="lpmidihdr"></span><span id="LPMIDIHDR"></span>*lpMidiHdr*
</dt> <dd>

Zeiger auf eine [**CURSORHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) die das Ereignis identifiziert, das den Rückruf verursacht hat. Der **dwOffset-Member** gibt den Offset des Ereignisses an.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Reserviert; nicht verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die Wiedergabe des Streampuffers wird auch während der Ausführung der Rückruffunktion fortgesetzt. Alle Ereignisse nach dem MEVT \_ F \_ CALLBACK-Ereignis im Puffer werden geplant und rechtzeitig gesendet, unabhängig davon, wie viel Zeit in der Rückruffunktion aufgewendet wird.

Wenn Positionsrückrufe schneller generiert werden, als ihre Anwendung sie verarbeiten kann, verweist der **dwOffset-Member** der [**CABHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) möglicherweise auf ein Ereignis, das Ihre Anwendung noch nicht verarbeitet hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[MELDUNGSMELDUNGEN](midi-messages.md)
</dt> </dl>

 

