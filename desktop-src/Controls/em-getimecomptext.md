---
title: EM_GETIMECOMPTEXT (Richedit.h)
description: Ruft den Kompositionstext des Eingabemethode-Editors (Input Method Editor, IME) ab.
ms.assetid: 1516305c-5f87-4ae0-97db-8709c71abacc
keywords:
- EM_GETIMECOMPTEXT message Windows Controls
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
ms.openlocfilehash: 5dd915f037275d428df37ca02a206b936a63bfd2f6ac8fbb605d1573b9535789
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049070"
---
# <a name="em_getimecomptext-message"></a>EM \_ GETIMECOMPTEXT-Nachricht

Ruft den Kompositionstext des Eingabemethode-Editors (Input Method Editor, IME) ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die [**IMECOMPTEXT-Struktur.**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)

</dd> <dt>

*lParam* 
</dt> <dd>

Der Puffer, der den Kompositionstext empfängt. Die Größe dieses Puffers ist im **cb-Member** der *wParam-Struktur* enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei Erfolg ist der Rückgabewert die Anzahl der Unicode-Zeichen, die in den Puffer kopiert werden. Andernfalls ist es 0 (null).

## <a name="remarks"></a>Hinweise

Diese Meldung verwendet nur Unicode-Zeichenfolgen.

**Sicherheitswarnung:** Stellen Sie sicher, dass ein Puffer vorhanden ist, der für die Größe der Eingabe ausreicht. Wenn Sie dies nicht tun, kann dies zu Problemen für Ihre Anwendung führen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMECOMPTEXT**](/windows/desktop/api/Richedit/ns-richedit-imecomptext)
</dt> </dl>

 

 





