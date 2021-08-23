---
title: EM_GETIMEPROPERTY Nachricht (Richedit.h)
description: Ruft die Eigenschaft und die Funktionen des Eingabemethoden-Editors (Input Method Editor, IME) ab, der dem aktuellen Eingabeschema zugeordnet ist.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- EM_GETIMEPROPERTY Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_GETIMEPROPERTY
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b96ad255d9d68cc76869b6f9163aedf549da19ff0c3ddba756f8da42267135c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541110"
---
# <a name="em_getimeproperty-message"></a>\_EM-GETIMEPROPERTY-Nachricht

Ruft die Eigenschaft und die Funktionen des Eingabemethoden-Editors (Input Method Editor, IME) ab, der dem aktuellen Eingabeschema zugeordnet ist.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Typ der abzurufenden Eigenschafteninformationen an. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                     | Bedeutung                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <dt>**\_IGP-EIGENSCHAFT**</dt> </dl>                | Eigenschafteninformationen.<br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <dt>**\_IGP-KONVERTIERUNG**</dt> </dl>          | Konvertierungsfunktionen. <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <dt>**\_IGP-SATZ**</dt> </dl>                | Funktionen des Satzmodus. <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <dt>**\_IGP-Benutzeroberfläche**</dt> </dl>                                  | Funktionen der Benutzeroberfläche. <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <dt>**IGP \_ SETCOMPSTR**</dt> </dl>          | Kompositionszeichenfolgenfunktionen. <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <dt>**IGP \_ SELECT**</dt> </dl>                      | Funktionen der Auswahlvererbung. <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <dt>**IGP \_ GETIMEVERSION**</dt> </dl> | Ruft die Systemversionsnummer ab, für die die angegebene IME erstellt wurde. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt abhängig vom Wert des *lParam-Parameters* die Eigenschaft oder den Funktionswert zurück. Weitere Informationen finden Sie in den Hinweisen.

## <a name="remarks"></a>Hinweise

Wenn *wParam* IGP \_ PROPERTY ist, wird mindestens einer der folgenden Werte zurückgegeben.



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IME \_ PROP \_ AT \_ CARET                | Wenn diese Einstellung festgelegt ist, befindet sich das Konvertierungsfenster an der Caretposition. Wenn diese Einstellung nicht angezeigt wird, befindet sich das Fenster in der Nähe der Caretposition.                                                                                                                                                                  |
| IME \_ PROP \_ SPECIAL \_ UI              | Wenn diese Einstellung festgelegt ist, verfügt IME über eine nicht standardmäßige Benutzeroberfläche. Die Anwendung sollte nicht im IME-Fenster zeichnen.                                                                                                                                                                  |
| IME \_ PROP \_ CANDLIST \_ START FROM \_ \_ 1 | Wenn diese Einstellung festgelegt ist, werden Zeichenfolgen in der Kandidatenliste ab 1 nummeriert. Wenn die Zeichenfolgen eindeutig sind, beginnen sie bei 0 (null).                                                                                                                                                                |
| IME \_ PROP \_ UNICODE                  | Wenn diese Einstellung festgelegt ist, wird die IME als UnicodeIME angezeigt. Das System und die IME kommunizieren über die UnicodeIME-Schnittstelle. Wenn dies klar ist, verwendet IME die ANSI-Schnittstelle für die Kommunikation mit dem System.                                                                    |
| IME \_ PROP \_ COMPLETE \_ ON \_ UNSELECT   | Wenn diese Einstellung festgelegt ist, befindet sich das Konvertierungsfenster an der Caretposition. Wenn diese Einstellung nicht angezeigt wird, befindet sich das Fenster in der Nähe der Caretposition.                                                                                                                                                                  |
| IME \_ PROP \_ ACCEPT \_ WIDE \_ VKEY       | Wenn diese Einstellung festgelegt ist, verarbeitet die IME den eingefügten Unicode-Code, der von der [**SendInput-Funktion**](/windows/desktop/api/winuser/nf-winuser-sendinput) stammt, mithilfe von VK \_ PACKET. Wenn dies klar ist, verarbeitet die IME möglicherweise den eingefügten Unicode-Code nicht, und der eingefügte Unicode-Code wird möglicherweise direkt an die Anwendung gesendet. |



 

Wenn *wParam* die \_ IGP-Benutzeroberfläche ist, wird mindestens einer der folgenden Werte zurückgegeben.



| Anforderung | Wert |
|-----------------|-------------------------------------------------------------------------------------------------------|
| UI \_ CAP \_ 2700   | Unterstützt Text-Escapewerte von 0 oder 2700. Weitere Informationen finden Sie unter **lfEscapement**.             |
| UI \_ CAP \_ ROT90  | Unterstützt Text-Escapewerte von 0, 900, 1800 oder 2700. Weitere Informationen finden Sie unter **lfEscapement**. |
| UI \_ CAP \_ ROTANY | Unterstützt jeden Text-Escapewert. Weitere Informationen finden Sie unter **lfEscapement**.                       |



 

Wenn *wParam* IGP \_ SETCOMPSTR ist, wird mindestens einer der folgenden Werte zurückgegeben.



| Anforderung | Wert |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCS \_ CAP \_ COMPSTR            | Die Kompositionszeichenfolge kann durch Aufrufen der [**ImmSetCompositionString-Funktion**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) mit dem SCS \_ SETSTR-Wert erstellt werden.                                                      |
| SCS \_ CAP \_ MAKEREAD           | Kann die Lesezeichenfolge aus der entsprechenden Kompositionszeichenfolge erstellen, wenn die [**ImmSetCompositionString-Funktion**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) mit SCS \_ SETSTR und ohne Festlegung von *lpRead* verwendet wird. |
| SCS \_ CAP \_ SETRECONVERTSTRING | Diese IME kann die Reconversion unterstützen. Verwenden Sie [**ImmSetCompositionString**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) für die Reconversion.                                                                             |



 

Wenn *wParam* IGP \_ SELECT ist, wird mindestens einer der folgenden Werte zurückgegeben.



| Anforderung | Wert |
|-----------------------|------------------------------------------------------|
| SELECT \_ CAP \_ CONVMODE | Erbt den Konvertierungsmodus, wenn eine neue IME ausgewählt wird. |
| AUSWÄHLEN \_ DES \_ CAP-SATZES | Erbt den Satzmodus, wenn eine neue IME ausgewählt wird.   |



 

Wenn *wParam* IGP \_ GETIMEVERSION ist, wird mindestens einer der folgenden Werte zurückgegeben.



| Anforderung | Wert |
|--------------|---------------------------------------------|
| IMEVER \_ 0310 | Die IME wurde für Windows 3.1 erstellt.        |
| IMEVER \_ 0400 | Die IME wurde für Windows 95 oder höher erstellt. |



 

Diese Meldung ähnelt [**ImmGetProperty,**](/windows/desktop/api/imm/nf-imm-immgetproperty)mit der Ausnahme, dass sie das aktuelle Eingabegebietsschema verwendet. Die Anwendung sollte [**EM \_ ISIME**](em-isime.md) aufrufen, bevor diese Funktion aufgerufen wird.

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

[**EM \_ ISIME**](em-isime.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**ImmGetProperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

