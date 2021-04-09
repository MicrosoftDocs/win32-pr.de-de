---
title: EM_STREAMOUT Meldung (RichEdit. h)
description: Bewirkt, dass ein Rich Edit-Steuerelement seinen Inhalt an eine Application \ 8211; defined editstreamcallback-Rückruffunktion übergibt. Die Rückruffunktion kann dann den Datenstrom in eine Datei oder an einen beliebigen anderen Speicherort schreiben, den Sie auswählt.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- Windows-Steuerelemente für EM_STREAMOUT Meldung
topic_type:
- apiref
api_name:
- EM_STREAMOUT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbdef51348593f8dbcfdb1ef579aca7dba6f96e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956509"
---
# <a name="em_streamout-message"></a>EM- \_ StreamOut-Meldung

Bewirkt, dass ein Rich Edit-Steuerelement seinen Inhalt an eine von der Anwendung definierte [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Rückruffunktion übergibt. Die Rückruffunktion kann dann den Datenstrom in eine Datei oder an einen beliebigen anderen Speicherort schreiben, den Sie auswählt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die Datenformat-und Ersetzungs Optionen an.

Dieser Wert muss einer der folgenden Werte sein.



| Wert                                                                                                                                                      | Bedeutung                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**SF \_ RTF**</dt> </dl>                   | RTF.<br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <dt>**SF \_ RTF noobjs**</dt> </dl> | RTF mit Leerzeichen anstelle von COM-Objekten.<br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**SF- \_ Text**</dt> </dl>                | Text mit Leerzeichen anstelle von COM-Objekten.<br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <dt>**SF \_ textisiert**</dt> </dl>    | Text mit einer Textdarstellung von COM-Objekten.<br/> |



 

Die Option " **SF \_ RTF noobjs** " ist nützlich, wenn eine Anwendung com-Objekte selbst speichert, da die RTF-Darstellung von COM-Objekten nicht sehr kompakt ist. Das Steuerwort \\ objattph, gefolgt von einem Leerzeichen, deutet auf die Objektposition hin.

Außerdem können Sie die folgenden Flags angeben.



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF- \_ plainrtf**</dt> </dl>       | Wenn angegeben, werden durch das Rich Edit-Steuerelement nur die Schlüsselwörter gestreamt, die für alle Sprachen gelten, wobei sprachspezifische Schlüsselwörter ignoriert werden. Wenn nicht angegeben, werden durch das Rich Edit-Steuerelement alle Schlüsselwörter gestreamt. Sie können dieses Flag mit dem **SF \_ RTF** -oder **SF \_ RTF** -Flag kombinieren.<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**SFF- \_ Auswahl**</dt> </dl>    | Wenn diese Option angegeben ist, wird das Rich Edit-Steuerelement nur den Inhalt der aktuellen Auswahl auslagern. Wenn nichts angegeben ist, streamt das Steuerelement den gesamten Inhalt. Sie können dieses Flag mit einem beliebigen Datenformat Wert kombinieren.<br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF ( \_ Unicode)**</dt> </dl>             | **Microsoft Rich Edit 2,0 und höher:** Gibt Unicode-Text an. Sie können dieses Flag mit dem **SF- \_ textflag** kombinieren.<br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <dt>**SF \_ useCodepage**</dt> </dl> | **Rich Edit 3,0 und höher:** Generiert UTF-8 RTF sowie Text, der andere Codepages verwendet. Die Codepage wird im großen Wort von *wParam* festgelegt. Legen Sie z. b. für UTF-8 RTF *wParam* auf (CP \_ UTF8 << 16) \| SF \_ useCodepage \| SF \_ RTF fest.<br/>                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur. Bei der Eingabe muss der **pfncallback** -Member dieser Struktur auf eine von der Anwendung definierte [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Funktion verweisen. Bei der Ausgabe kann der **dwError** -Member einen Fehlercode ungleich 0 (null) enthalten, wenn ein Fehler aufgetreten ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die Anzahl der Zeichen zurück, die in den Datenstrom geschrieben werden.

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine **EM- \_ StreamOut** -Nachricht senden, führt das Rich Edit-Steuerelement wiederholte Aufrufe an die [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Funktion aus, die vom **pfncallback** -Member der [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur angegeben wird. Jedes Mal, wenn die Rückruffunktion aufgerufen wird, übergibt das Steuerelement einen Puffer, der einen Teil des Inhalts des Steuer Elements enthält. Dieser Prozess wird fortgesetzt, bis das Steuerelement seinen gesamten Inhalt an die Rückruffunktion weitergegeben hat oder bis ein Fehler auftritt.

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

[**Editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*Editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**EM- \_ StreamIn**](em-streamin.md)
</dt> </dl>

 

 





