---
title: MOM_POSITIONCB Meldung (MMSYSTEM. h)
description: Die MOM- \_ Positions Meldung wird gesendet, wenn ein mevt \_ F- \_ Rückruf Ereignis im MIDI-Ausgabestream erreicht wird.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- MOM_POSITIONCB-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MOM_POSITIONCB
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c9528e8f91778c53ed4761c98bb67d405ec14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743353"
---
# <a name="mom_positioncb-message"></a>MOM- \_ positioncb-Meldung

Die **MOM- \_ Positions** Meldung wird gesendet, wenn ein **mevt \_ F- \_ Rückruf** Ereignis im MIDI-Ausgabestream erreicht wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Ein Zeiger auf eine [**midihdr**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) -Struktur, die den Eingabepuffer identifiziert.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die Wiedergabe des Streampuffers wird auch dann fortgesetzt, wenn die Rückruffunktion ausgeführt wird. Alle Ereignisse nach dem **mevt \_ F- \_ Rückruf** Ereignis im Puffer werden zeitlich geplant und gesendet, unabhängig davon, wie viel Zeit in der Rückruffunktion aufgewendet wird.

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

 

