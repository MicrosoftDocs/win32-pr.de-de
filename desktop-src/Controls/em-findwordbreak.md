---
title: EM_FINDWORDBREAK (Richedit.h)
description: Sucht den nächsten Wortbruch vor oder nach der angegebenen Zeichenposition oder ruft Informationen über das Zeichen an dieser Position ab.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- EM_FINDWORDBREAK der Windows Steuerelemente
topic_type:
- apiref
api_name:
- EM_FINDWORDBREAK
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8eaa2a58c8af1181ca22ddd767392749b2c838238e933c52a96268542be0240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541140"
---
# <a name="em_findwordbreak-message"></a>EM \_ FINDWORDBREAK-Nachricht

Sucht den nächsten Wortbruch vor oder nach der angegebenen Zeichenposition oder ruft Informationen über das Zeichen an dieser Position ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Find-Vorgang an. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <dt>**WB \_ CLASSIFY**</dt> </dl>                | Gibt die Zeichenklasse und die Wörterbruchflags des Zeichens an der angegebenen Position zurück.<br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <dt>**WB \_ ISDELIMITER**</dt> </dl>       | Gibt **TRUE zurück,** wenn das Zeichen an der angegebenen Position ein Trennzeichen ist, andernfalls **FALSE.**<br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <dt>**WB \_ LEFT**</dt> </dl>                            | Sucht das nächste Zeichen vor der angegebenen Position, die ein Wort beginnt.<br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <dt>**WB \_ LEFTBREAK**</dt> </dl>             | Sucht das nächste Wortende vor der angegebenen Position. Dieser Wert ist identisch mit WB \_ PREVBREAK.<br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <dt>**WB \_ MOVEWORDLEFT**</dt> </dl>    | Sucht das nächste Zeichen, das ein Wort vor der angegebenen Position beginnt. Dieser Wert wird bei der Tastenverarbeitung von STRG+NACH-LINKS-TASTE verwendet. Dieser Wert ähnelt WB \_ MOVEWORDPREV. Weitere Informationen finden Sie unter Hinweise.<br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <dt>**WB \_ MOVEWORDRIGHT**</dt> </dl> | Sucht das nächste Zeichen, das ein Wort nach der angegebenen Position beginnt. Dieser Wert wird während der Tastenverarbeitung mit STRG+RECHTS verwendet. Dieser Wert ähnelt WB \_ MOVEWORDNEXT. Weitere Informationen finden Sie unter Hinweise.<br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <dt>**WB \_ RIGHT**</dt> </dl>                         | Sucht das nächste Zeichen, das ein Wort nach der angegebenen Position beginnt.<br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <dt>**WB \_ RIGHTBREAK**</dt> </dl>          | Sucht das nächste Wortendetrennzeichen nach der angegebenen Position. Dieser Wert ist identisch mit WB \_ NEXTBREAK.<br/>                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Nullbasierte Zeichenstartposition.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Meldung gibt einen Wert zurück, der auf dem *wParam-Parameter* basiert.



| Rückgabecode                                                                                    | Beschreibung                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Wparam**</dt> </dl>          | Rückgabewert<br/>                                                                                                |
| <dl> <dt>**WB \_ CLASSIFY**</dt> </dl>    | Gibt die Zeichenklasse und die Wörterbruchflags des Zeichens an der angegebenen Position zurück.<br/>                |
| <dl> <dt>**WB \_ ISDELIMITER**</dt> </dl> | Gibt **TRUE zurück,** wenn das Zeichen an der angegebenen Position ein Trennzeichen ist. Andernfalls wird **FALSE zurückgegeben.**<br/> |
| <dl> <dt>**Andere**</dt> </dl>          | Gibt den Zeichenindex der Wörterpause zurück.<br/>                                                              |



 

## <a name="remarks"></a>Hinweise

Wenn *wParam* auf WB LEFT und WB RIGHT festgelegt ist, findet die Wörterumbruchprozedur Wörterumbrüche nur \_ nach \_ Trennzeichen. Dies entspricht der Funktionalität eines Bearbeitungssteuer steuerelements. Wenn *wParam* WB \_ MOVEWORDLEFT oder WB MOVEWORDRIGHT ist, vergleicht die Prozedur für die Wörterpause auch Zeichenklassen und \_ Wörterbruchflags.

Informationen zu Zeichenklassen und Wörterumbruchflags finden Sie unter [Zeilenumbrüche und Zeilenumbrüche.](using-rich-edit-controls.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





