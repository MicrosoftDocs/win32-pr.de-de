---
title: EM_SETWORDBREAKPROCEX Meldung (RichEdit. h)
description: Legt die erweiterte Wort Umbruch Prozedur für ein Rich-Edit-Steuerelement fest.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- Windows-Steuerelemente für EM_SETWORDBREAKPROCEX Meldung
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5973836ae173c1a61537b7d3b085fe29c168971f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949708"
---
# <a name="em_setwordbreakprocex-message"></a>EM \_ setwordbreakprocex-Meldung

Legt die erweiterte Wort Umbruch Prozedur für ein Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [*editwordbreakprocex*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) -Funktion oder **null** , um die Standardprozedur zu verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die Adresse der vorherigen erweiterten Wort Umbruch Prozedur zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Editwordbreakprocex**](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[**EM \_ getwordbreakprocex**](em-getwordbreakprocex.md)
</dt> </dl>

 

 





