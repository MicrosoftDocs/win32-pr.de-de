---
title: EM_FINDTEXTEX (Richedit.h)
description: 'EM_FINDTEXTEX Meldung: Sucht Text in einem Rich-Edit-Steuerelement.'
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- EM_FINDTEXTEX meldungssteuerelemente Windows
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
ms.openlocfilehash: 41f5121108fcd75d3b57b3ef61a8dc789bd92f731a3593314036d4d9507e6252
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119541190"
---
# <a name="em_findtextex-message"></a>EM \_ FINDTEXTEX-Nachricht

Sucht Text in einem Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt das Verhalten des Suchvorgang an. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Microsoft Rich Edit 2.0 und höher: Wenn festgelegt, wird die Suche von **FINDTEXTEX.hlg.cpMin weitergeleitet.** Wenn dies nicht festgelegt ist, befindet sich die Suche rückwärts von **FINDTEXTEX.chrg.cpMin.** <br/> Microsoft Rich Edit 1.0: Das FR \_ DOWN-Flag wird ignoriert. Die Suche ist immer vorwärts.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3.0 und höher: Wenn festgelegt, unterscheidet die Suche zwischen arabischen und hebräischen Alefs mit unterschiedlichen Akzenten. Wenn nicht festgelegt, werden alle Alefs allein durch das Alef-Zeichen übereinstimmen. <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | Wenn festgelegt, wird beim Suchvorgang die Kleinschreibung beachtet. Wenn dies nicht festgelegt ist, wird beim Suchvorgang die Groß-/Kleinschreibung nicht beachtet. <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDMATCH**</dt> </dl>                | Microsoft Rich Edit 3.0 und höher: Wenn festgelegt, berücksichtigt der Suchvorgang arabische und hebräische diakritische Markierungen. Wenn nicht festgelegt, werden diakritische Markierungen ignoriert. <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Microsoft Rich Edit 3.0 und höher: Wenn festgelegt, berücksichtigt der Suchvorgang arabische und hebräische Kungdas. Wenn dies nicht festgelegt ist, werden k seit dem Festlegen ignoriert. <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Wenn festgelegt, sucht der Vorgang nur nach ganzen Wörtern, die mit der Suchzeichenfolge übereinstimmen. Wenn nicht festgelegt, sucht der Vorgang auch nach Wortfragmenten, die mit der Suchzeichenfolge übereinstimmen.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**FINDTEXTEX-Struktur,**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) die Informationen zum Find-Vorgang enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Zielzeichenfolge gefunden wird, ist der Rückgabewert die nullbasierte Position des ersten Zeichens der Übereinstimmung. Wenn das Ziel nicht gefunden wird, ist der Rückgabewert -1.

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Meldung, um ANSI-Zeichenfolgen zu suchen. Verwenden Sie für Unicode [**EM \_ FINDTEXTEXW**](em-findtextexw.md).

Der **cpMin-Member** **von FINDTEXTEX.chrg** gibt immer den Ausgangspunkt der Suche an, und **cpMax** gibt den Endpunkt an. Bei der Rückwärtssuche **muss cpMin** gleich oder größer als **cpMax sein.** Bei der Vorwärtssuche erweitert der Wert -1 in **cpMax** den Suchbereich bis zum Ende des Texts.

Wenn der Suchvorgang eine Übereinstimmung findet, gibt das **Member "chrgText"** der [**FINDTEXTEX-Struktur**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) den Bereich der Zeichenpositionen zurück, der den übereinstimmenden Text enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ FINDTEXT**](em-findtext.md)
</dt> </dl>

 

 





