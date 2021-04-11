---
title: EM_SETPUNCTUATION Meldung (RichEdit. h)
description: Legt die Interpunktions Zeichen für ein Rich-Edit-Steuerelement fest.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- Windows-Steuerelemente für EM_SETPUNCTUATION Meldung
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710392cee7f7a1fb04fce59d6549134255499172
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105567"
---
# <a name="em_setpunctuation-message"></a>EM- \_ setinterpunktions-Nachricht

Legt die Interpunktions Zeichen für ein Rich-Edit-Steuerelement fest.

> [!Note]  
> Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt. Sie wird in späteren Versionen nicht unterstützt.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Interpunktions Typ an, bei dem es sich um einen der folgenden Werte handeln kann.



| Wert                                                                                                                                                      | Bedeutung                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**PC- \_ führend**</dt> </dl>       | Führende Interpunktions Zeichen.<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC \_ nach**</dt> </dl> | Die folgenden Interpunktions Zeichen.<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**PC- \_ Trennzeichen**</dt> </dl> | Trennzeichen.<br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <dt>**PC \_ Überlauf**</dt> </dl> | Wird nicht unterstützt.<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Interpunktions**](/windows/desktop/api/Richedit/ns-richedit-punctuation) Struktur, die die Interpunktions Zeichen enthält.

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

[**EM- \_ Zeichensatz**](em-getpunctuation.md)
</dt> <dt>

[**Interpunktions**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





