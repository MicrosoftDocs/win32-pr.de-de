---
title: EM_FINDTEXTEXW Meldung (RichEdit. h)
description: Findet Unicode-Text in einem Rich-Edit-Steuerelement.
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- Windows-Steuerelemente für EM_FINDTEXTEXW Meldung
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf0857e47c6e98f4be6867ca66baef3472766a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957006"
---
# <a name="em_findtextexw-message"></a>EM \_ findtextexw-Meldung

Findet Unicode-Text in einem Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt das Verhalten des Such Vorgangs an. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**Fr \_ nach unten**</dt> </dl>                               | Microsoft Rich Edit 2,0 und höher: Wenn diese Einstellung festgelegt ist, wird die Suche von **FINDTEXTEX. chrg. cpmin**; weiterleiten. Wenn nicht festgelegt, wird die Suche rückwärts von **FINDTEXTEX. chrg. cpmin** durchgesetzt. <br/> Microsoft Rich Edit 1,0: das FR- \_ down-Flag wird ignoriert. Die Suche erfolgt immer weiter.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**Fr \_ MatchAlefHamza**</dt> </dl> | Wenn festgelegt, unterscheidet die Suche zwischen Alefs und unterschiedlichen Akzenten. Wenn diese Einstellung nicht festgelegt ist, werden alle arabischen und hebräischen Alefs mit unterschiedlichen Akzenten mit dem Alef-Zeichen übereinstimmen. <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**Fr \_ MatchCase**</dt> </dl>                | Wenn festgelegt, wird bei der Suche die Groß-/Kleinschreibung beachtet. Wenn nicht festgelegt, wird bei der Suche die Groß-/Kleinschreibung nicht beachtet.<br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**Fr \_ matchdiac**</dt> </dl>                | Wenn festgelegt, berücksichtigt der Suchvorgang Diakritische Markierungen. Wenn nicht festgelegt, werden die diakritischen Zeichen Arabisch und Hebräisch ignoriert. <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**Fr \_ MatchKashida**</dt> </dl>       | Wenn festgelegt, berücksichtigt der Suchvorgang Kashidas. Wenn nicht festgelegt, werden arabische und hebräische Kashidas ignoriert. <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**"# \_ wholeword"**</dt> </dl>                | Wenn festgelegt, sucht der Vorgang nur nach ganzen Wörtern, die der Such Zeichenfolge entsprechen. Wenn nicht festgelegt, sucht der Vorgang auch nach Word-Fragmenten, die der Such Zeichenfolge entsprechen.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**findtextexw**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur, die Informationen über den Suchvorgang enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Ziel Zeichenfolge gefunden wird, ist der Rückgabewert die null basierte Position des ersten Zeichens der Entsprechung. Wenn das Ziel nicht gefunden wird, ist der Rückgabewert-1.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Meldung, um Unicode-Zeichen folgen zu suchen Verwenden Sie für ANSI; [**EM \_ FINDTEXTEX**](em-findtextex.md).

Der **cpmin** -Member von **FINDTEXTEX. chrg** gibt immer den Anfangspunkt der Suche an, und **cpmax** gibt den Endpunkt an. Bei der Rückwärtssuche muss **cpmin** größer oder gleich **cpmax** sein. Bei der Suche wird durch den Wert-1 in **cpmax** der Suchbereich auf das Ende des Texts erweitert.

Wenn bei der Suche eine Übereinstimmung gefunden wird, gibt der **chrgtext** -Member der [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur den Bereich von Zeichen Positionen zurück, der den übereinstimmenden Text enthält.

**EM \_ Findtextexw** verwendet die [**findtextexw**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur, während [**EM \_ findtextw**](em-findtextw.md) die [**findtextw**](/windows/win32/api/richedit/ns-richedit-findtexta) -Struktur verwendet. Der Unterschied besteht darin, dass **EM \_ findtextexw** den Textbereich meldet, der gefunden wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ findtextw**](em-findtextw.md)
</dt> </dl>

 

 





