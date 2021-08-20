---
title: EM_STREAMOUT (Richedit.h)
description: Bewirkt, dass ein rich edit-Steuerelement seinen Inhalt an eine Anwendung \8211;definierte EditStreamCallback-Rückruffunktion überträgt. Die Rückruffunktion kann dann den Datenstrom in eine Datei oder einen beliebigen anderen Speicherort schreiben.
ms.assetid: 3f14aaac-4b17-47af-8f2b-503390631a88
keywords:
- EM_STREAMOUT von Windows-Steuerelementen
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
ms.openlocfilehash: 63236083c1964d29cb915e4bfc51303b30b730e01f76f2b186cc200d1dcfce6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019468"
---
# <a name="em_streamout-message"></a>EM \_ STREAMOUT-Nachricht

Bewirkt, dass ein umfassendes Bearbeitungssteuerprogramm seinen Inhalt an eine von der Anwendung definierte [*EditStreamCallback-Rückruffunktion*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) überleiten kann. Die Rückruffunktion kann dann den Datenstrom in eine Datei oder einen beliebigen anderen Speicherort schreiben.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt das Datenformat und die Ersetzungsoptionen an.

Dieser Wert muss einer der folgenden Werte sein.



| Wert                                                                                                                                                      | Bedeutung                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**SF \_ RTF**</dt> </dl>                   | Rtf.<br/>                                            |
| <span id="SF_RTFNOOBJS"></span><span id="sf_rtfnoobjs"></span><dl> <dt>**SF \_ RTFNOOBJS**</dt> </dl> | RTF mit Leerzeichen statt COM-Objekten.<br/>        |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**SF \_ TEXT**</dt> </dl>                | Text mit Leerzeichen statt COM-Objekten.<br/>       |
| <span id="SF_TEXTIZED"></span><span id="sf_textized"></span><dl> <dt>**SF \_ TEXTIZED**</dt> </dl>    | Text mit einer Textdarstellung von COM-Objekten.<br/> |



 

Die **SF \_ RTFNOOBJS-Option** ist nützlich, wenn eine Anwendung COM-Objekte selbst speichert, da die RTF-Darstellung von COM-Objekten nicht sehr kompakt ist. Das Steuerelementwort \\ objattph, gefolgt von einem Leerzeichen, gibt die Objektposition an.

Darüber hinaus können Sie die folgenden Flags angeben.



| Wert                                                                                                                                                            | Bedeutung                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF \_ PLAINRTF**</dt> </dl>       | Wenn angegeben, gibt das Rich-Edit-Steuerelement nur die Schlüsselwörter aus, die allen Sprachen gemeinsam sind, und ignoriert sprachspezifische Schlüsselwörter. Wenn keine Angabe erfolgt, gibt das Rich-Edit-Steuerelement alle Schlüsselwörter aus. Sie können dieses Flag mit dem **SF \_ RTF-** oder **SF \_ RTFNOOBJS-Flag** kombinieren.<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**\_SFF-AUSWAHL**</dt> </dl>    | Wenn angegeben, gibt das Rich-Edit-Steuerelement nur den Inhalt der aktuellen Auswahl aus. Wenn keine Angabe erfolgt, streamt das Steuerelement den gesamten Inhalt aus. Sie können dieses Flag mit beliebigen Datenformatwerten kombinieren.<br/>                                                        |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF \_ UNICODE**</dt> </dl>             | **Microsoft Rich Edit 2.0 und höher:** Gibt Unicode-Text an. Sie können dieses Flag mit dem **SF \_ TEXT-Flag** kombinieren.<br/>                                                                                                                                                        |
| <span id="SF_USECODEPAGE"></span><span id="sf_usecodepage"></span><dl> <dt>**SF \_ USECODEPAGE**</dt> </dl> | **Rich Edit 3.0 und höher:** Generiert UTF-8 RTF sowie Text mithilfe anderer Codepages. Die Codepage wird im hohen Wort *von wParam festgelegt.* Legen Sie beispielsweise für UTF-8 RTF *wParam* auf SF \_ \| \_ USECODEPAGE SF RTF (CP UTF8 << 16) \| \_ fest.<br/>                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**EDITSTREAM-Struktur.**](/windows/desktop/api/Richedit/ns-richedit-editstream) Bei der Eingabe muss **der pfnCallback-Member** dieser Struktur auf eine von der Anwendung definierte [*EditStreamCallback-Funktion*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) verweisen. Bei der Ausgabe kann **das dwError-Element** einen Fehlercode ungleich 0 (null) enthalten, wenn ein Fehler aufgetreten ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die Anzahl der Zeichen zurück, die in den Datenstrom geschrieben werden.

## <a name="remarks"></a>Hinweise

Wenn Sie eine **EM \_ STREAMOUT-Nachricht** senden, führt das Rich Edit-Steuerelement wiederholte Aufrufe der [*EditStreamCallback-Funktion*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) durch, die vom **pfnCallback-Member** der [**EDITSTREAM-Struktur angegeben**](/windows/desktop/api/Richedit/ns-richedit-editstream) wird. Jedes Mal, wenn die Rückruffunktion aufruft, übergibt das Steuerelement einen Puffer, der einen Teil des Inhalts des Steuerelements enthält. Dieser Prozess wird fortgesetzt, bis das Steuerelement seinen ganzen Inhalt an die Rückruffunktion übergeben hat oder bis ein Fehler auftritt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

**Referenz**
</dt> <dt>

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**EM \_ STREAMIN**](em-streamin.md)
</dt> </dl>

 

 





