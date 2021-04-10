---
title: EM_GETIMEMODEBIAS Meldung (RichEdit. h)
description: Ruft den IME-Modus (Eingabemethoden-Editor) für ein Microsoft Rich Edit-Steuerelement ab.
ms.assetid: e8ca899f-3423-4814-86e9-133dfd11f9a6
keywords:
- Windows-Steuerelemente für EM_GETIMEMODEBIAS Meldung
topic_type:
- apiref
api_name:
- EM_GETIMEMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea13e151ae9d487340ee440e3b123ae70b437a02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040804"
---
# <a name="em_getimemodebias-message"></a>EM \_ getimemodebias-Nachricht

Ruft den IME-Modus (Eingabemethoden-Editor) für ein Microsoft Rich Edit-Steuerelement ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die aktuelle Einstellung für den IME-Modus zurück.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**EM \_ getctfmodebias**](em-getctfmodebias.md), um den Text Dienst-Framework-Modus zu erhalten.

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

[**EM \_ getctf modebias**](em-getctfmodebias.md)
</dt> </dl>

 

 





