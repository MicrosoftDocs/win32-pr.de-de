---
title: EM_GETIMECOMPTEXT Meldung (RichEdit. h)
description: Ruft den Eingabemethoden-Editor (IME)-Kompositions Text ab.
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- Windows-Steuerelemente für EM_GETIMECOMPTEXT Meldung
topic_type:
- apiref
api_name:
- EM_GETIMECOMPTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 834c55d6b5e40de7dcacfeb3e2d0c2e0878a0f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956825"
---
# <a name="em_getimecomptext-message"></a>EM \_ getimecomptext-Nachricht

Ruft den Eingabemethoden-Editor (IME)-Kompositions Text ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die [**imecomptext**](/windows/desktop/api/Richedit/ns-richedit-imecomptext) -Struktur.

</dd> <dt>

*lParam* 
</dt> <dd>

Der Puffer, der den Kompositions Text empfängt. Die Größe dieses Puffers ist im **CB** -Member der *wParam* -Struktur enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung ist der Rückgabewert die Anzahl von Unicode-Zeichen, die in den Puffer kopiert werden. Andernfalls ist der Wert 0 (null).

## <a name="remarks"></a>Bemerkungen

Diese Meldung nimmt nur Unicode-Zeichen folgen an.

**Sicherheitswarnung:** Stellen Sie sicher, dass ein Puffer für die Größe der Eingabe ausreichend ist. Wenn dies nicht der Fall ist, kann dies zu Problemen mit Ihrer Anwendung führen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imecomptext**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





