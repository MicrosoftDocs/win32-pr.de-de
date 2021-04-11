---
title: EM_GETPUNCTUATION Meldung (RichEdit. h)
description: Ruft die aktuellen Interpunktions Zeichen für das Rich Edit-Steuerelement ab.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- Windows-Steuerelemente für EM_GETPUNCTUATION Meldung
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105297"
---
# <a name="em_getpunctuation-message"></a>EM \_ getinterinterationmeldung

Ruft die aktuellen Interpunktions Zeichen für das Rich Edit-Steuerelement ab.

> [!Note]  
> Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt. Sie wird in höheren Versionen der Rich-Edit-Version nicht unterstützt.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Interpunktions Typ kann einer der folgenden Werte sein.



| Wert                                                                                                                                                      | Bedeutung                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**PC- \_ führend**</dt> </dl>       | Führende Interpunktions Zeichen<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC \_ nach**</dt> </dl> | Die folgenden Interpunktions Zeichen<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**PC- \_ Trennzeichen**</dt> </dl> | Trennzeichen<br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <dt>**PC- \_ Überlauf**</dt> </dl>    | Nicht unterstützt<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**Interpunktions**](/windows/desktop/api/Richedit/ns-richedit-punctuation) Struktur, die die Interpunktions Zeichen empfängt.

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

[**EM- \_ setinterpunktions Zeichen**](em-setpunctuation.md)
</dt> <dt>

[**Interpunktions**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





