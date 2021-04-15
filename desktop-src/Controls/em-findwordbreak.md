---
title: EM_FINDWORDBREAK Meldung (RichEdit. h)
description: Sucht das nächste Wort Umbruch vor oder nach der angegebenen Zeichenposition oder ruft Informationen über das Zeichen an dieser Position ab.
ms.assetid: b5df1365-4672-4c82-8ae4-ebf8b60bf871
keywords:
- Windows-Steuerelemente für EM_FINDWORDBREAK Meldung
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
ms.openlocfilehash: b6533358c0f4f521bc7021e290dfe11d66d4499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477121"
---
# <a name="em_findwordbreak-message"></a>EM \_ findwordbreak-Meldung

Sucht das nächste Wort Umbruch vor oder nach der angegebenen Zeichenposition oder ruft Informationen über das Zeichen an dieser Position ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Suchvorgang an. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                  | Bedeutung                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WB_CLASSIFY"></span><span id="wb_classify"></span><dl> <dt>**WB- \_ Klassifizierung**</dt> </dl>                | Gibt die Zeichenklasse und die Wort Umbruch Flags des Zeichens an der angegebenen Position zurück.<br/>                                                                                                                          |
| <span id="WB_ISDELIMITER"></span><span id="wb_isdelimiter"></span><dl> <dt>**WB- \_ isdelimiter**</dt> </dl>       | Gibt **true** zurück, wenn das Zeichen an der angegebenen Position ein Trennzeichen ist, andernfalls **false** .<br/>                                                                                                                   |
| <span id="WB_LEFT"></span><span id="wb_left"></span><dl> <dt>**WB \_ Links**</dt> </dl>                            | Sucht das nächste Zeichen vor der angegebenen Position, die ein Wort beginnt.<br/>                                                                                                                                         |
| <span id="WB_LEFTBREAK"></span><span id="wb_leftbreak"></span><dl> <dt>**WB \_ leftbreak**</dt> </dl>             | Sucht das nächste Wort Ende vor der angegebenen Position. Dieser Wert entspricht dem Wert von WB \_ prevbreak.<br/>                                                                                                                       |
| <span id="WB_MOVEWORDLEFT"></span><span id="wb_movewordleft"></span><dl> <dt>**WB-" \_ muvewordleft"**</dt> </dl>    | Sucht das nächste Zeichen, das ein Wort vor der angegebenen Position beginnt. Dieser Wert wird bei der Verarbeitung von STRG + nach-links-Pfeiltaste verwendet. Dieser Wert ähnelt dem Wert von "WB" \_ . Weitere Informationen finden Sie unter Hinweise.<br/> |
| <span id="WB_MOVEWORDRIGHT"></span><span id="wb_movewordright"></span><dl> <dt>**WB-" \_ muvewordright"**</dt> </dl> | Sucht das nächste Zeichen, das ein Wort nach der angegebenen Position beginnt. Dieser Wert wird bei der STRG + right Key-Verarbeitung verwendet. Dieser Wert ähnelt dem Wert von WB " \_ muvewordnext". Weitere Informationen finden Sie unter Hinweise.<br/>           |
| <span id="WB_RIGHT"></span><span id="wb_right"></span><dl> <dt>**WB \_ Rechts**</dt> </dl>                         | Sucht das nächste Zeichen, das ein Wort nach der angegebenen Position beginnt.<br/>                                                                                                                                             |
| <span id="WB_RIGHTBREAK"></span><span id="wb_rightbreak"></span><dl> <dt>**WB- \_ rightbreak**</dt> </dl>          | Sucht das nächste Wort Ende-Trennzeichen nach der angegebenen Position. Dieser Wert entspricht dem Wert von WB \_ nextbreak.<br/>                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Anfangsposition des NULL basierten Zeichens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Meldung gibt einen Wert zurück, der auf dem *wParam* -Parameter basiert.



| Rückgabecode                                                                                    | Beschreibung                                                                                                            |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**wParam**</dt> </dl>          | Rückgabewert<br/>                                                                                                |
| <dl> <dt>**WB- \_ Klassifizierung**</dt> </dl>    | Gibt die Zeichenklasse und die Wort Umbruch Flags des Zeichens an der angegebenen Position zurück.<br/>                |
| <dl> <dt>**WB- \_ isdelimiter**</dt> </dl> | Gibt **true** zurück, wenn das Zeichen an der angegebenen Position ein Trennzeichen ist. Andernfalls wird **false** zurückgegeben.<br/> |
| <dl> <dt>**Andere**</dt> </dl>          | Gibt den Zeichen Index des Wort Bruchs zurück.<br/>                                                              |



 

## <a name="remarks"></a>Bemerkungen

Wenn *wParam* den Wert "WB \_ left" und "WB \_ right" hat, sucht die Prozedur "Wort Umbruch" nach Wort Umbrüchen nur nach Trennzeichen. Dies entspricht der Funktionalität eines Bearbeitungs Steuer Elements. Wenn *wParam* den Wert "WB" \_ , "muvewordleft" oder "WB" ist \_ , vergleicht die Prozedur "Wort Umbruch" auch Zeichenklassen und Wörter Trennungs Kennzeichen.

Weitere Informationen zu Zeichenklassen und Flags für das Wort Umbruch finden Sie unter [Wort-und Zeilenumbrüche](using-rich-edit-controls.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





