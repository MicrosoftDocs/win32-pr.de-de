---
title: EM_STREAMIN Nachricht (Richedit.h)
description: Ersetzt den Inhalt eines Rich Edit-Steuerelements durch einen Datenstrom, der von einer Anwendung bereitgestellt wird, die \8211 definiert ist; EditStreamCallback-Rückruffunktion.
ms.assetid: b8d3a108-b415-4f5e-99e7-0e0e7a82a778
keywords:
- EM_STREAMIN Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: 597d6483ef02f0c9f6f4e4459cd6780b91e04c39160c8057e88fc537fde3b173
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576340"
---
# <a name="em_streamin-message"></a>EM \_ STREAMIN-Nachricht

Ersetzt den Inhalt eines Rich Edit-Steuerelements durch einen Datenstrom, der von einer anwendungsdefiniert [*EditStreamCallback-Rückruffunktion*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) bereitgestellt wird.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt das Datenformat und die Ersetzungsoptionen an. Dieser Wert muss einer der folgenden Werte sein.



| Wert                                                                                                                                       | Bedeutung         |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------------|
| <span id="SF_RTF"></span><span id="sf_rtf"></span><dl> <dt>**SF \_ RTF**</dt> </dl>    | RTF<br/>  |
| <span id="SF_TEXT"></span><span id="sf_text"></span><dl> <dt>**SF \_ TEXT**</dt> </dl> | Text<br/> |



 

Darüber hinaus können Sie die folgenden Flags angeben.



| Wert                                                                                                                                                         | Bedeutung                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFF_PLAINRTF"></span><span id="sff_plainrtf"></span><dl> <dt>**SFF \_ PLAINRTF**</dt> </dl>    | Wenn angegeben, werden nur Schlüsselwörter gestreamt, die allen Sprachen gemeinsam sind. Sprachspezifische RTF-Schlüsselwörter im Stream werden ignoriert. Wenn keine Angabe erfolgt, werden alle Schlüsselwörter in gestreamt. Sie können dieses Flag mit dem **SF \_ RTF-Flag** kombinieren.<br/> |
| <span id="SFF_SELECTION"></span><span id="sff_selection"></span><dl> <dt>**\_SFF-AUSWAHL**</dt> </dl> | Wenn angegeben, ersetzt der Datenstrom den Inhalt der aktuellen Auswahl. Wenn keine Angabe erfolgt, ersetzt der Datenstrom den gesamten Inhalt des Steuerelements. Sie können dieses Flag mit den **SF \_ TEXT-** oder **SF \_ RTF-Flags** kombinieren.<br/>  |
| <span id="SF_UNICODE"></span><span id="sf_unicode"></span><dl> <dt>**SF \_ UNICODE**</dt> </dl>          | **Microsoft Rich Edit 2.0 und höher:** Gibt Unicode-Text an. Sie können dieses Flag mit dem **SF \_ TEXT-Flag** kombinieren. <br/>                                                                                                               |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**EDITSTREAM-Struktur.**](/windows/desktop/api/Richedit/ns-richedit-editstream) Bei der Eingabe muss der **pfnCallback-Member** dieser Struktur auf eine von der Anwendung definierte [*EditStreamCallback-Funktion*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) verweisen. Bei der Ausgabe kann der **dwError-Member** einen Fehlercode ungleich 0 (null) enthalten, wenn ein Fehler aufgetreten ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die Anzahl der gelesenen Zeichen zurück.

## <a name="remarks"></a>Hinweise

Wenn Sie eine **EM \_ STREAMIN-Nachricht** senden, führt das Rich Edit-Steuerelement wiederholt Aufrufe der [*EditStreamCallback-Funktion*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback) durch, die vom **pfnCallback-Member** der [**EDITSTREAM-Struktur**](/windows/desktop/api/Richedit/ns-richedit-editstream) angegeben wird. Jedes Mal, wenn die Rückruffunktion aufgerufen wird, füllt sie einen Puffer mit Daten, die in das Steuerelement gelesen werden sollen. Dies wird fortgesetzt, bis die Rückruffunktion angibt, dass der Stream-In-Vorgang abgeschlossen wurde oder ein Fehler auftritt.

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

[**EDITSTREAM**](/windows/desktop/api/Richedit/ns-richedit-editstream)
</dt> <dt>

[*EditStreamCallback*](/windows/desktop/api/Richedit/nc-richedit-editstreamcallback)
</dt> <dt>

[**EM \_ STREAMOUT**](em-streamout.md)
</dt> </dl>

 

 





