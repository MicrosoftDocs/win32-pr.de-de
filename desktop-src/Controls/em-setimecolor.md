---
title: EM_SETIMECOLOR Nachricht (Richedit.h)
description: Legt die Kompositionsfarbe des Eingabemethoden-Editors (Input Method Editor, IME) für ein Rich-Edit-Steuerelement fest.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- EM_SETIMECOLOR Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f68e548a36cbdaa28f292feb69b6d56cbc3264b0bea8bdb1938088717bd62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048400"
---
# <a name="em_setimecolor-message"></a>EM \_ SETIMECOLOR-Meldung

Legt die Kompositionsfarbe des Eingabemethoden-Editors (Input Method Editor, IME) für ein Rich-Edit-Steuerelement fest.

> [!Note]  
> Diese Meldung wird nur in asiatisch-sprachigen Versionen von Microsoft Rich Edit 1.0 unterstützt. In späteren Versionen wird dies nicht unterstützt.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**COMPCOLOR-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-compcolor) die die festzulegende Kompositionsfarbe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ GETIMECOLOR**](em-getimecolor.md)
</dt> <dt>

[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





