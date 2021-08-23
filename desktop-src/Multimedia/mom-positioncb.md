---
title: MOM_POSITIONCB Meldung (Mmsystem.h)
description: Die MOM \_ POSITION-Nachricht wird gesendet, wenn ein MEVT \_ F \_ CALLBACK-Ereignis im AUSGABEstream von CSV erreicht wird.
ms.assetid: 0464d74d-7d1f-4aab-a9e7-03397872f3c0
keywords:
- MOM_POSITIONCB nachricht Windows Multimedia
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
ms.openlocfilehash: d403d9d913628f6b00a7b36dba96d0f4d491f486ef9c3edf7a5c3d5a30c345f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807000"
---
# <a name="mom_positioncb-message"></a>MOM \_ POSITIONCB-Nachricht

Die **MOM \_ POSITION-Nachricht** wird gesendet, wenn ein **MEVT \_ F \_ CALLBACK-Ereignis** im AUSGABEstream von CSV erreicht wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="dwParam1"></span><span id="dwparam1"></span><span id="DWPARAM1"></span>*dwParam1*
</dt> <dd>

Ein Zeiger auf eine [**ACRYLHDR-Struktur,**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) die den Eingabepuffer identifiziert.

</dd> <dt>

<span id="dwParam2"></span><span id="dwparam2"></span><span id="DWPARAM2"></span>*dwParam2*
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die Wiedergabe des Streampuffers wird auch während der Ausführung der Rückruffunktion fortgesetzt. Alle Ereignisse nach dem **MEVT \_ F \_ CALLBACK-Ereignis** im Puffer werden geplant und rechtzeitig gesendet, unabhängig davon, wie viel Zeit in der Rückruffunktion aufgewendet wird.

Wenn Positionsrückrufe schneller generiert werden, als ihre Anwendung sie verarbeiten kann, verweist der **dwOffset-Member** der [**CABHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) möglicherweise auf ein Ereignis, das Ihre Anwendung noch nicht verarbeitet hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Mmsystem.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MELDUNGSMELDUNGEN](midi-messages.md)
</dt> </dl>

 

