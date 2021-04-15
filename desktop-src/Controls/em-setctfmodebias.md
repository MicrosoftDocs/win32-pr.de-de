---
title: EM_SETCTFMODEBIAS Meldung (RichEdit. h)
description: Legt den TSF-Modus (Text Services Framework) für ein Rich-Edit-Steuerelement fest.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- Windows-Steuerelemente für EM_SETCTFMODEBIAS Meldung
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
ms.openlocfilehash: b872fa5489c898ec4482ecdc094de7df6e3180be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518674"
---
# <a name="em_setctfmodebias-message"></a>EM \_ setctf modebias-Nachricht

Legt den TSF-Modus (Text Services Framework) für ein Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Moduswert. Dies kann einer der folgenden Werte sein:



| Wert                                                                                                                                                                                                                     | Bedeutung                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <dt>**CTF modebias ( \_ Standard)**</dt> </dl>                                           | Es gibt keine Modus-Abweichung.<br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <dt>**CTF modebias- \_ Dateiname**</dt> </dl>                                        | Die Verschiebung ist ein Dateiname.<br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <dt>**Name des CTF modebias \_**</dt> </dl>                                                    | Die Verschiebung ist ein Name.<br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <dt>**CTF modebias- \_ Lesevorgang**</dt> </dl>                                           | Die Verschiebung ist das lesen.<br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <dt>**CTF modebias \_ DateTime**</dt> </dl>                                        | Der Bias ist ein Datum oder eine Uhrzeit.<br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <dt>**CTF modebias- \_ Konversation**</dt> </dl>                            | Der Bias ist eine Konversation.<br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <dt>**CTF modebias \_ numerisch**</dt> </dl>                                           | Der Bias ist eine Zahl.<br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <dt>**CTF modebias \_ Hiragana**</dt> </dl>                                        | Die Verschiebung erfolgt auf Hiragana-Zeichen folgen.<br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <dt>**CTF modebias \_ Katakana**</dt> </dl>                                        | Die Verschiebung erfolgt auf Katakana-Zeichen folgen.<br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <dt>**CTF modebias \_ Hangul**</dt> </dl>                                              | Die Verschiebung erfolgt auf Hangul-Zeichen.<br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <dt>**CTF modebias \_ halfwidthkatakana**</dt> </dl>             | Die Verschiebung erfolgt auf Katakana-Zeichen folgen der Hälfte Breite.<br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <dt>**ctfmodebias \_ fullwidthalpha numerisch**</dt> </dl> | Der Bias besteht aus alphanumerischen Zeichen mit voller Breite.<br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <dt>**ctfmodebias \_ halfwidthalpha numerisch**</dt> </dl> | Die Verschiebung erfolgt auf alphanumerische Zeichen mit halber Breite.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Nicht verwendet; muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei erfolgreicher Ausführung ist der Rückgabewert der neue Wert des TSF-Modus-Bias. Wenn nicht erfolgreich, ist der Rückgabewert der alte Wert des TSF-Modus-Bias.

## <a name="remarks"></a>Bemerkungen

Wenn eine Microsoft Rich Edit-Anwendung TSF verwendet, kann Sie den TSF-Modus "Bias" auswählen. In dieser Meldung werden die Kriterien festgelegt, mit denen eine Alternative Auswahl am oberen Rand der Liste zur Auswahl angezeigt wird.

Um die modusabweichung für den Eingabemethoden-Editor (Input Method Editor, IME) festzulegen, verwenden Sie [**EM \_ setimemodebias**](em-setimemodebias.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP1 \[ Desktop-Apps\]<br/>                                  |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**EM \_ getctf modebias**](em-getctfmodebias.md)
</dt> <dt>

[**EM- \_ Zeit modebias**](em-setimemodebias.md)
</dt> </dl>

 

 





