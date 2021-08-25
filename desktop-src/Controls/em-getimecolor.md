---
title: EM_GETIMECOLOR (Richedit.h)
description: Ruft die Kompositionsfarbe des Eingabemethode-Editors (IME) ab.
ms.assetid: 788ac56c-f2d8-4e9a-8829-b92dcd76e6de
keywords:
- EM_GETIMECOLOR meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- EM_GETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46ac9d49f4fe178bdda45359da8aabd40badcd68aceadc4a57890279fc9fda01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049100"
---
# <a name="em_getimecolor-message"></a>EM \_ GETIMECOLOR-Nachricht

Ruft die Kompositionsfarbe des Eingabemethode-Editors (IME) ab.

> [!Note]  
> Diese Meldung wird nur in asiatisch-sprachbasierten Versionen von Microsoft Rich Edit 1.0 unterstützt. Sie wird in späteren Versionen von Rich Edit nicht unterstützt.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Vier-Element-Array von [**COMPCOLOR-Strukturen,**](/windows/desktop/api/Richedit/ns-richedit-compcolor) das die Kompositionsfarbe empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





