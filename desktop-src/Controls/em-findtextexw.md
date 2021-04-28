---
title: EM_FINDTEXTEXW (Richedit.h)
description: 'EM_FINDTEXTEXW Meldung: Sucht Unicode-Text in einem Rich-Edit-Steuerelement.'
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- EM_FINDTEXTEXW Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 5278726ca4d3e4748e96d8095a411bcebd5637ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109808"
---
# <a name="em_findtextexw-message"></a>EM \_ FINDTEXTEXW-Nachricht

Sucht Unicode-Text in einem Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt das Verhalten des Suchvorgang an. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Microsoft Rich Edit 2.0 und höher: Wenn festgelegt, wird die Suche von **FINDTEXTEX.hlg.cpMin weitergeleitet.** Wenn dies nicht festgelegt ist, befindet sich die Suche rückwärts von **FINDTEXTEX.chrg.cpMin.** <br/> Microsoft Rich Edit 1.0: Das FR \_ DOWN-Flag wird ignoriert. Die Suche ist immer vorwärts.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Wenn festgelegt, unterscheidet die Suche zwischen Alefs mit unterschiedlichen Akzenten. Wenn dies nicht festgelegt ist, werden arabische und hebräische Alefs mit unterschiedlichen Akzenten durch das Alef-Zeichen übereinstimmen. <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | Wenn festgelegt, wird beim Suchvorgang die Kleinschreibung beachtet. Wenn dies nicht festgelegt ist, wird beim Suchvorgang die Groß-/Kleinschreibung nicht beachtet.<br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDMATCH**</dt> </dl>                | Wenn festgelegt, berücksichtigt der Suchvorgang diakritische Markierungen. Wenn dies nicht festgelegt ist, werden arabische und hebräische diakritische Markierungen ignoriert. <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKDDADA**</dt> </dl>       | Wenn diese Einstellung festgelegt ist, berücksichtigt der Suchvorgang K msidas. Wenn sie nicht festgelegt ist, werden arabische und hebräische K msidas ignoriert. <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Wenn diese Einstellung festgelegt ist, sucht der Vorgang nur nach ganzen Wörtern, die mit der Suchzeichenfolge übereinstimmen. Wenn diese Einstellung nicht festgelegt ist, sucht der Vorgang auch nach Wortfragmenten, die mit der Suchzeichenfolge übereinstimmen.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**FINDTEXTEXW-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) die Informationen zum Suchvorgang enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Zielzeichenfolge gefunden wird, ist der Rückgabewert die nullbasierte Position des ersten Zeichens der Übereinstimmung. Wenn das Ziel nicht gefunden wird, lautet der Rückgabewert -1.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Meldung, um Unicode-Zeichenfolgen zu suchen. Verwenden Sie für ANSI; [**EM \_ FINDTEXTEX**](em-findtextex.md).

Der **cpMin-Member** von **FINDTEXTEX.chg** gibt immer den Startpunkt der Suche und **cpMax** den Endpunkt an. Beim Rückwärtssuchen muss **cpMin** gleich oder größer als **cpMax** sein. Bei der Vorwärtssuche erweitert der Wert -1 in **cpMax** den Suchbereich bis zum Ende des Texts.

Wenn der Suchvorgang eine Übereinstimmung findet, gibt der **chgText-Member** der [**FINDTEXTEX-Struktur**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) den Bereich der Zeichenpositionen zurück, der den übereinstimmenden Text enthält.

**EM \_ FINDTEXTEXW** verwendet die [**FINDTEXTEXW-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) [**während EM \_ FINDTEXTW**](em-findtextw.md) die [**FINDTEXTW-Struktur**](/windows/win32/api/richedit/ns-richedit-findtexta) verwendet. Der Unterschied besteht darin, dass **EM \_ FINDTEXTEXW** den gefundenen Textbereich meldet.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ FINDTEXTW**](em-findtextw.md)
</dt> </dl>

 

 





