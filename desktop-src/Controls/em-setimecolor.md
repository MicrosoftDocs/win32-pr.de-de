---
title: EM_SETIMECOLOR Meldung (RichEdit. h)
description: Legt die Zusammensetzung der Eingabemethoden-Editor (IME) für ein Rich-Edit-Steuerelement fest.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- Windows-Steuerelemente für EM_SETIMECOLOR Meldung
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
ms.openlocfilehash: 3c020bb3af2b1197afc005bd0b6efec82b609b88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477322"
---
# <a name="em_setimecolor-message"></a>EM- \_ Zeit Farb Meldung

Legt die Zusammensetzung der Eingabemethoden-Editor (IME) für ein Rich-Edit-Steuerelement fest.

> [!Note]  
> Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt. Sie wird in späteren Versionen nicht unterstützt.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf eine [**compcolor**](/windows/desktop/api/Richedit/ns-richedit-compcolor) -Struktur, die die festzulegende Kompositions Farbe enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

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

[**EM \_ getimecolor**](em-getimecolor.md)
</dt> <dt>

[**Compcolor**](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





