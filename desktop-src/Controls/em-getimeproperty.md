---
title: EM_GETIMEPROPERTY Meldung (RichEdit. h)
description: Ruft die Eigenschaft und die Funktionen des Eingabemethoden-Editors (IME) ab, die dem aktuellen Eingabe Gebiets Schema zugeordnet sind.
ms.assetid: 0cbe52d4-c3e7-40bd-a6f6-da0a11056976
keywords:
- Windows-Steuerelemente für EM_GETIMEPROPERTY Meldung
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
ms.openlocfilehash: 94c081aa99c99f4cd0995c0f9d2f5256e2958dc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105123"
---
# <a name="em_getimeproperty-message"></a>EM \_ getimeproperty-Nachricht

Ruft die Eigenschaft und die Funktionen des Eingabemethoden-Editors (IME) ab, die dem aktuellen Eingabe Gebiets Schema zugeordnet sind.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Typ der abzurufenden Eigenschafts Informationen an. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                     | Bedeutung                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="IGP_PROPERTY"></span><span id="igp_property"></span><dl> <dt>**IGP- \_ Eigenschaft**</dt> </dl>                | Eigenschafts Informationen.<br/>                                                         |
| <span id="IGP_CONVERSION"></span><span id="igp_conversion"></span><dl> <dt>**IGP- \_ Konvertierung**</dt> </dl>          | Konvertierungs Funktionen. <br/>                                                     |
| <span id="IGP_SENTENCE"></span><span id="igp_sentence"></span><dl> <dt>**IGP- \_ Satz**</dt> </dl>                | Satzmodusfunktionen. <br/>                                                  |
| <span id="IGP_UI"></span><span id="igp_ui"></span><dl> <dt>**IGP- \_ Benutzeroberfläche**</dt> </dl>                                  | Benutzeroberflächen Funktionen. <br/>                                                 |
| <span id="IGP_SETCOMPSTR"></span><span id="igp_setcompstr"></span><dl> <dt>**IGP \_ setcompstr**</dt> </dl>          | Kompositions Zeichen folgen Funktionen. <br/>                                             |
| <span id="IGP_SELECT"></span><span id="igp_select"></span><dl> <dt>**IGP- \_ Auswahl**</dt> </dl>                      | Auswahl Vererbungs Funktionen. <br/>                                          |
| <span id="IGP_GETIMEVERSION"></span><span id="igp_getimeversion"></span><dl> <dt>**IGP- \_ getimeversion**</dt> </dl> | Ruft die System Versionsnummer ab, für die der angegebene IME erstellt wurde. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Eigenschafts-oder Funktionswert zurück, abhängig vom Wert des *LPARAM* -Parameters. Weitere Informationen finden Sie in den Hinweisen.

## <a name="remarks"></a>Bemerkungen

Wenn *wParam* eine IGP- \_ Eigenschaft ist, gibt Sie einen oder mehrere der folgenden Werte zurück.



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IME- \_ Prop \_ bei \_ Caretzeichen                | Wenn festgelegt, befindet sich das Konvertierungs Fenster an der Einfügemarke. Wenn diese Option deaktiviert ist, befindet sich das Fenster in der Nähe der Position der                                                                                                                                                                  |
| spezielle IME- \_ Prop- \_ \_ Benutzeroberfläche              | Wenn festgelegt, verfügt IME über eine nicht standardmäßige Benutzeroberfläche. Die Anwendung sollte nicht im IME-Fenster gezeichnet werden.                                                                                                                                                                  |
| Start Seite der IME- \_ Prop-Kerze mit \_ \_ \_ \_ 1 | Wenn festgelegt, werden Zeichen folgen in der Kandidatenliste beginnend mit 1 nummeriert. Wenn Clear, beginnen Zeichen folgen bei Null.                                                                                                                                                                |
| IME- \_ Prop- \_ Unicode                  | Wenn festgelegt, wird der IME als unicodeime angezeigt. Das System und der IME kommunizieren über die unicodeime-Schnittstelle. Wenn Clear, verwendet IME die ANSI-Schnittstelle für die Kommunikation mit dem System.                                                                    |
| IME \_ - \_ Prop \_ bei \_ Auswahl beenden   | Wenn festgelegt, befindet sich das Konvertierungs Fenster an der Einfügemarke. Wenn diese Option deaktiviert ist, befindet sich das Fenster in der Nähe der Position der                                                                                                                                                                  |
| IME-unter \_ Stützung für \_ \_ Wide \_ VKey       | Wenn festgelegt, verarbeitet der IME den eingefügten Unicode, der aus der [**SendInput**](/windows/desktop/api/winuser/nf-winuser-sendinput) -Funktion stammt, mithilfe des VK- \_ Pakets. Wenn Clear, verarbeitet der IME möglicherweise nicht den eingefügten Unicode-Code, und der eingefügte Unicode kann direkt an die Anwendung gesendet werden. |



 

Wenn *wParam* die IGP- \_ Benutzeroberfläche ist, gibt Sie einen oder mehrere der folgenden Werte zurück.



| Anforderung | Wert |
|-----------------|-------------------------------------------------------------------------------------------------------|
| \_Oberfläche \_ 2700   | Unterstützt Text escapeswerte von 0 oder 2700. Weitere Informationen finden Sie unter **LF escapements**.             |
| UI- \_ Obergrenze \_ ROT90  | Unterstützt Text escapeswerte von 0, 900, 1800 oder 2700. Weitere Informationen finden Sie unter **LF escapements**. |
| Oberfläche für die Benutzeroberflächen Abdeckung \_ \_ | Unterstützt jeden Text escapeswert. Weitere Informationen finden Sie unter **LF escapements**.                       |



 

Wenn *wParam* \_ den Wert IGP setcompstr hat, gibt er einen oder mehrere der folgenden Werte zurück.



| Anforderung | Wert |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCS- \_ Cap- \_ compstr            | Kann die Kompositions Zeichenfolge durch Aufrufen der [**immsetcompositionstring**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) -Funktion mit dem SCS \_ setstr-Wert erstellen.                                                      |
| SCS- \_ Cap- \_ makeread           | Kann die Lese Zeichenfolge aus der entsprechenden Kompositions Zeichenfolge erstellen, wenn die [**immsetcompositionstring**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) -Funktion mit SCS \_ setstr und ohne Festlegen von *lpread* verwendet wird. |
| SCS- \_ Cap-abdeckungszeichenfolge \_ | Dieser IME kann eine erneute Konvertierung unterstützen. Verwenden Sie [**immsetcompositionstring**](/windows/desktop/api/imm/nf-imm-immsetcompositionstringa) , um die erneute Konvertierung durchzuführen.                                                                             |



 

Wenn für *wParam* die Option IGP ausgewählt ist, wird mindestens \_ einer der folgenden Werte zurückgegeben.



| Anforderung | Wert |
|-----------------------|------------------------------------------------------|
| Wählen Sie Cap-Verbindungs Modus aus. \_ \_ | Erbt den Konvertierungsmodus, wenn ein neuer IME ausgewählt wird. |
| \_Cap- \_ Satz auswählen | Erbt den Satz Modus, wenn ein neuer IME ausgewählt wird.   |



 

Wenn *wParam* eine IGP- \_ getimeversion ist, gibt Sie einen oder mehrere der folgenden Werte zurück.



| Anforderung | Wert |
|--------------|---------------------------------------------|
| Imever \_ 0310 | Der IME wurde für Windows 3,1 erstellt.        |
| Imever \_ 0400 | Der IME wurde für Windows 95 oder höher erstellt. |



 

Diese Meldung ähnelt " [**immgetproperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)", mit dem Unterschied, dass Sie das aktuelle Eingabe Gebiets Schema verwendet. Die Anwendung sollte [**EM- \_ isime**](em-isime.md) aufrufen, bevor diese Funktion aufgerufen wird.

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

[**EM- \_ isime**](em-isime.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Immgetproperty**](/windows/desktop/api/imm/nf-imm-immgetproperty)
</dt> </dl>

 

