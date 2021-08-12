---
title: EM_SETIMEMODEBIAS Nachricht (Richedit.h)
description: Legen Sie den IME-Modus (Input Method Editor) für ein Rich-Edit-Steuerelement fest.
ms.assetid: 4a3f97eb-fe80-4e84-a73e-3ed6d73644de
keywords:
- EM_SETIMEMODEBIAS Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: b4812c21558fba07be2709c0fd1a011f31d79fad17e0b4146fa0c7d65843a087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672670"
---
# <a name="em_setimemodebias-message"></a>EM \_ SETIMEMODEBIAS-Nachricht

Legen Sie den IME-Modus (Input Method Editor) für ein Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

IME-Modus-Biaswert. Dies kann einer der folgenden Sein:



| Wert                                                                                                                                                                                        | Bedeutung                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="IMF_SMODE_PLAURALCLAUSE"></span><span id="imf_smode_plauralclause"></span><dl> <dt>**\_ÜBERFALL-SMODE \_ PLAURALCLAUSE**</dt> </dl> | Legt den IME-Modus-Bias auf Name fest.<br/> |
| <span id="IMF_SMODE_NONE"></span><span id="imf_smode_none"></span><dl> <dt>**IMF \_ SMODE \_ NONE**</dt> </dl>                            | Keine Voreingenommenheit.<br/>                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dies muss derselbe Wert wie *wParam* sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die neue Einstellung für den IME-Modus zurück.

## <a name="remarks"></a>Hinweise

Wenn die IME eine Liste alternativer Optionen für einen Satz von Zeichen generiert, legt diese Meldung die Kriterien fest, nach denen einige der Optionen am Anfang der Liste angezeigt werden.

Verwenden Sie [**EM \_ SETCTFMODEBIAS,**](em-setctfmodebias.md)um die Voreingenommenheit des Textdienstframework -Modus (TSF) festzulegen.

Die Anwendung sollte [**EM \_ ISIME**](em-isime.md) aufrufen, bevor diese Funktion aufgerufen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

[**EM \_ SETCTFMODEBIAS**](em-setctfmodebias.md)
</dt> </dl>

 

 





