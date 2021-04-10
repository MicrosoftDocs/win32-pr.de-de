---
title: EM_FINDTEXTEX Meldung (RichEdit. h)
description: Sucht Text in einem Rich-Edit-Steuerelement.
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- Windows-Steuerelemente für EM_FINDTEXTEX Meldung
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e52f7d51ee7a186a8a9e66f11884d6c2e9bca2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104223"
---
# <a name="em_findtextex-message"></a>EM \_ FINDTEXTEX-Nachricht

Sucht Text in einem Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt das Verhalten des Such Vorgangs an. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**Fr \_ nach unten**</dt> </dl>                               | Microsoft Rich Edit 2,0 und höher: Wenn diese Einstellung festgelegt ist, wird die Suche von **FINDTEXTEX. chrg. cpmin**; weiterleiten. Wenn nicht festgelegt, wird die Suche rückwärts von **FINDTEXTEX. chrg. cpmin** durchgesetzt. <br/> Microsoft Rich Edit 1,0: das FR- \_ down-Flag wird ignoriert. Die Suche erfolgt immer weiter.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**Fr \_ MatchAlefHamza**</dt> </dl> | Microsoft Rich Edit 3,0 und höher: Wenn diese Einstellung festgelegt ist, unterscheidet die Suche zwischen arabischen und hebräischen Alefs mit unterschiedlichen Akzenten. Wenn nicht festgelegt, werden alle Alefs nur mit dem Alef-Zeichen abgeglichen. <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**Fr \_ MatchCase**</dt> </dl>                | Wenn festgelegt, wird bei der Suche die Groß-/Kleinschreibung beachtet. Wenn nicht festgelegt, wird bei der Suche die Groß-/Kleinschreibung nicht beachtet. <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**Fr \_ matchdiac**</dt> </dl>                | Microsoft Rich Edit 3,0 und höher: Wenn festgelegt, betrachtet der Suchvorgang arabische und hebräische diakritische Zeichen. Wenn nicht festgelegt, werden Diakritische Markierungen ignoriert. <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**Fr \_ MatchKashida**</dt> </dl>       | Microsoft Rich Edit 3,0 und höher: Wenn festgelegt, betrachtet der Suchvorgang arabische und hebräische Kashidas. Wenn nicht festgelegt, werden Kashidas ignoriert. <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**"# \_ wholeword"**</dt> </dl>                | Wenn festgelegt, sucht der Vorgang nur nach ganzen Wörtern, die der Such Zeichenfolge entsprechen. Wenn nicht festgelegt, sucht der Vorgang auch nach Word-Fragmenten, die der Such Zeichenfolge entsprechen.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur, die Informationen über den Suchvorgang enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Ziel Zeichenfolge gefunden wird, ist der Rückgabewert die null basierte Position des ersten Zeichens der Entsprechung. Wenn das Ziel nicht gefunden wird, ist der Rückgabewert-1.

## <a name="remarks"></a>Bemerkungen

Mithilfe dieser Meldung können Sie ANSI-Zeichen folgen suchen. Verwenden Sie für Unicode den Eintrag [**EM \_ findtextexw**](em-findtextexw.md).

Der **cpmin** -Member von **FINDTEXTEX. chrg** gibt immer den Anfangspunkt der Suche an, und **cpmax** gibt den Endpunkt an. Bei der Rückwärtssuche muss **cpmin** größer oder gleich **cpmax** sein. Bei der Suche wird durch den Wert-1 in **cpmax** der Suchbereich auf das Ende des Texts erweitert.

Wenn bei der Suche eine Übereinstimmung gefunden wird, gibt der **chrgtext** -Member der [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur den Bereich von Zeichen Positionen zurück, der den übereinstimmenden Text enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM- \_ FindText**](em-findtext.md)
</dt> </dl>

 

 





