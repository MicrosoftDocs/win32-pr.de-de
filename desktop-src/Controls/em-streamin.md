---
title: EM_STREAMIN Meldung (RichEdit. h)
description: Ersetzt den Inhalt eines Rich-Edit-Steuer Elements durch einen Datenstrom, der von einer Anwendung bereitgestellt wird, die definiert ist \ 8211; Editstreamcallback-Rückruffunktion.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- Windows-Steuerelemente für EM_STREAMIN Meldung
topic_type:
- apiref
api_name:
- EM_STREAMIN
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40fdcf844cce09cf5c49085a9fcf08a38ad988ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478276"
---
# <a name="em_streamin-message"></a>EM- \_ StreamIn-Meldung

Ersetzt den Inhalt eines Rich-Edit-Steuer Elements durch einen Datenstrom, der von einer Anwendung bereitgestellt wird, die die [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Rückruffunktion definiert.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die Datenformat-und Ersetzungs Optionen an. Dieser Wert muss einer der folgenden Werte sein.



| Wert                                                                                                                                       | Bedeutung         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**SF \_ RTF**</dt> </dl>    | RTF<br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**SF- \_ Text**</dt> </dl> | Text<br/> |



 

Außerdem können Sie die folgenden Flags angeben.



| Wert                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF- \_ plainrtf**</dt> </dl>    | Wenn angegeben, werden nur Schlüsselwörter gestreamt, die allen Sprachen gemeinsam sind. Sprachspezifische RTF-Schlüsselwörter im Stream werden ignoriert. Wenn nicht angegeben, werden alle Schlüsselwörter in gestreamt. Sie können dieses Flag mit dem **SF \_ RTF** -Flag kombinieren.<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**SFF- \_ Auswahl**</dt> </dl> | Wenn angegeben, ersetzt der Datenstrom den Inhalt der aktuellen Auswahl. Wenn nicht angegeben, ersetzt der Datenstrom den gesamten Inhalt des-Steuer Elements. Sie können dieses Flag mit den **SF- \_ Text** -oder **SF \_ RTF** -Flags kombinieren.<br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF ( \_ Unicode)**</dt> </dl>          | **Microsoft Rich Edit 2,0 und höher:** Gibt Unicode-Text an. Sie können dieses Flag mit dem **SF- \_ textflag** kombinieren. <br/>                                                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur. Bei der Eingabe muss der **pfncallback** -Member dieser Struktur auf eine von der Anwendung definierte [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Funktion verweisen. Bei der Ausgabe kann der **dwError** -Member einen Fehlercode ungleich 0 (null) enthalten, wenn ein Fehler aufgetreten ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die Anzahl der gelesenen Zeichen zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine **EM- \_ StreamIn** -Nachricht senden, führt das Rich Edit-Steuerelement wiederholte Aufrufe an die [*editstreamcallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) -Funktion aus, die vom **pfncallback** -Member der [**editstream**](/windows/desktop/api/Richedit/ns-richedit-editstream) -Struktur angegeben wird. Jedes Mal, wenn die Rückruffunktion aufgerufen wird, füllt Sie einen Puffer mit Daten aus, die in das Steuerelement eingelesen werden sollen. Dies wird fortgesetzt, bis die Rückruffunktion anzeigt, dass der Stream-in-Vorgang abgeschlossen wurde oder ein Fehler auftritt.

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

[**EM- \_ StreamOut**](em-streamout.md)
</dt> </dl>

 

 





