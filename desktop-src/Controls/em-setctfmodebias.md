---
title: EM_SETCTFMODEBIAS-Nachricht (Richedit.h)
description: Legt die Voreingenommenheit des Textdienstframework -Modus (TSF) für ein Rich-Edit-Steuerelement fest.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- EM_SETCTFMODEBIAS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd6aa0f10b07092d9637d9e5a993848671ab6aa7e7eb610eca48c3df353c4a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019508"
---
# <a name="em_setctfmodebias-message"></a>EM \_ SETCTFMODEBIAS-Nachricht

Legt die Voreingenommenheit des Textdienstframework -Modus (TSF) für ein Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Mode Bias-Wert. Dies kann einer der folgenden Werte sein.



| Wert                                                                                                                                                                                                                     | Bedeutung                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <dt>**CTFMODEBIAS \_ DEFAULT**</dt> </dl>                                           | Es gibt keine Voreingenommenheit im Modus.<br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <dt>**CTFMODEBIAS \_ FILENAME**</dt> </dl>                                        | Die Voreingenommenheit ist auf einen Dateinamen ausgerichtet.<br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <dt>**CTFMODEBIAS-NAME \_**</dt> </dl>                                                    | Die Voreingenommenheit ist auf einen Namen ausgerichtet.<br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <dt>**CTFMODEBIAS \_ READING**</dt> </dl>                                           | Der Voreingenommenheit liegt beim Lesen.<br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <dt>**CTFMODEBIAS \_ DATETIME**</dt> </dl>                                        | Die Verschiebung erfolgt auf ein Datum oder eine Uhrzeit.<br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <dt>**CTFMODEBIAS \_ CONVERSATION**</dt> </dl>                            | Der Voreingenommenheit liegt in einer Konversation.<br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <dt>**CTFMODEBIAS \_ NUMERIC**</dt> </dl>                                           | Die Voreingenommenheit ist auf eine Zahl.<br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <dt>**CTFMODEBIAS \_ HIRAGANA**</dt> </dl>                                        | Die Voreingenommenheit besteht in Hiragana-Zeichenfolgen.<br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <dt>**CTFMODEBIAS \_ KATAKANA**</dt> </dl>                                        | Der Voreingenommenheit liegt in Katakana-Zeichenfolgen.<br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <dt>**CTFMODEBIAS \_ HANGUL**</dt> </dl>                                              | Der Voreingenommenheit liegt in Hangul-Zeichen.<br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHKATAKANA**</dt> </dl>             | Die Verschiebung erfolgt auf Katakana-Zeichenfolgen halber Breite.<br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ FULLWIDTHALPHANUMERIC**</dt> </dl> | Die Verschiebung erfolgt auf alphanumerische Zeichen mit voller Breite.<br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHALPHANUMERIC**</dt> </dl> | Die Verschiebung erfolgt auf alphanumerische Zeichen halber Breite.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn erfolgreich, ist der Rückgabewert der neue TSF-Modus-Biaswert. Wenn der Fehler nicht erfolgreich ist, ist der Rückgabewert der alte TSF-Modus-Biaswert.

## <a name="remarks"></a>Hinweise

Wenn eine Microsoft Rich Edit-Anwendung TSF verwendet, kann sie die Voreingenommenheit des TSF-Modus auswählen. Diese Meldung legt die Kriterien fest, nach denen eine alternative Auswahl am Anfang der Auswahlliste angezeigt wird.

Verwenden Sie [**EM \_ SETIMEMODEBIAS,**](em-setimemodebias.md)um die Modeabweichung für den Eingabemethoden-Editor (IME) festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP1-Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**EM \_ GETCTFMODEBIAS**](em-getctfmodebias.md)
</dt> <dt>

[**EM \_ SETIMEMODEBIAS**](em-setimemodebias.md)
</dt> </dl>

 

 





