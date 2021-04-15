---
title: EM_SETIMEMODEBIAS Meldung (RichEdit. h)
description: Legen Sie den Modus für den Eingabemethoden-Editor (IME) für ein Rich-Edit-Steuerelement fest.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- Windows-Steuerelemente für EM_SETIMEMODEBIAS Meldung
topic_type:
- apiref
api_name:
- EM_SETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48fbd93971a57cffa3441c2a3db0816572f761d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477319"
---
# <a name="em_setimemodebias-message"></a>EM- \_ /timemodebias-Nachricht

Legen Sie den Modus für den Eingabemethoden-Editor (IME) für ein Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wert des IME-Modus-Bias. Dies kann einer der folgenden sein:



| Wert                                                                                                                                                                                        | Bedeutung                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <dt>**IMF- \_ smode- \_ plauralklausel**</dt> </dl> | Legt die Verschiebung des IME-Modus auf Name fest.<br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <dt>**IMF- \_ smode- \_ keine**</dt> </dl>                            | Keine Neigung.<br/>                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Wert muss mit dem Wert von *wParam* identisch sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die neue Einstellung für den IME-Modus zurück.

## <a name="remarks"></a>Bemerkungen

Wenn der IME eine Liste alternativer Optionen für einen Satz von Zeichen generiert, legt diese Meldung die Kriterien fest, mit denen einige der Optionen oben in der Liste angezeigt werden.

Um den TSF-Modus (Text Services Framework) festzulegen, verwenden Sie [**EM \_ setctfmodebias**](em-setctfmodebias.md).

Die Anwendung sollte [**EM- \_ isime**](em-isime.md) aufrufen, bevor diese Funktion aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM- \_ isime**](em-isime.md)
</dt> <dt>

[**EM \_ setctf modebias**](em-setctfmodebias.md)
</dt> </dl>

 

 





