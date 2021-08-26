---
title: EM_SETPUNCTUATION (Richedit.h)
description: Legt die Interpunktionszeichen für ein Rich-Edit-Steuerelement fest.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- EM_SETPUNCTUATION von Windows-Steuerelementen
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
ms.openlocfilehash: 9a5e0856c1ee1882695dc5e6d7dfdd6b72ea0f6c4f16ee7396bbfde2b76b49b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062900"
---
# <a name="em_setpunctuation-message"></a>EM \_ SETPUNCTUATION-Meldung

Legt die Interpunktionszeichen für ein Rich-Edit-Steuerelement fest.

> [!Note]  
> Diese Meldung wird nur in asiatisch-sprachbasierten Versionen von Microsoft Rich Edit 1.0 unterstützt. Sie wird in späteren Versionen nicht unterstützt.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Interpunktionstyp an, der einer der folgenden Werte sein kann.



| Wert                                                                                                                                                      | Bedeutung                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**PC \_ LEADING**</dt> </dl>       | Führende Interpunktionszeichen.<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC \_ FOLLOWING**</dt> </dl> | Folgende Interpunktionszeichen.<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**\_PC-TRENNZEICHEN**</dt> </dl> | Trennzeichen.<br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <dt>**PC \_ OVERFLOW**</dt> </dl> | Wird nicht unterstützt.<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**PUNCTUATION-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-punctuation) die die Interpunktionszeichen enthält.

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

**Referenz**
</dt> <dt>

[**EM \_ GETPUNCTUATION**](em-getpunctuation.md)
</dt> <dt>

[**Satzzeichen**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





