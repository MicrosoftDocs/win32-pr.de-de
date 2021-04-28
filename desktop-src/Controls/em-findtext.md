---
title: EM_FINDTEXT Nachricht (Richedit.h)
description: 'EM_FINDTEXT Meldung: Sucht Text in einem Rich Edit-Steuerelement.'
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT Meldung Windows-Steuerelemente
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 452d4e2534fb05cbbbf4c02ac4146f2f8914c9bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109848"
---
# <a name="em_findtext-message"></a>\_EM-FINDTEXT-Nachricht

Sucht Text in einem Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Geben Sie die Parameter des Suchvorgangs an. Bei diesem Parameter kann es sich um einen oder mehrere der folgenden Werte handelt.



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Microsoft Rich Edit 2.0 und höher: Bei Festlegung erfolgt die Suche vom Ende der aktuellen Auswahl bis zum Ende des Dokuments. Wenn diese Option nicht festgelegt ist, erfolgt die Suche vom Ende der aktuellen Auswahl bis zum Anfang des Dokuments. <br/> Microsoft Rich Edit 1.0: Das FR \_ DOWN-Flag wird ignoriert. Die Suche erfolgt immer vom Ende der aktuellen Auswahl bis zum Ende des Dokuments.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3.0 und höher: Bei Festlegung unterscheidet die Suche zwischen arabischen Alefs mit unterschiedlichen Akzenten. Wenn sie nicht festgelegt ist, werden alle Alefs allein durch das Alef-Zeichen abgegleichen. <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDAKA**</dt> </dl>                | Microsoft Rich Edit 3.0 und höher: Wenn festgelegt, berücksichtigt der Suchvorgang arabische und hebräische diakritische Markierungen. Wenn sie nicht festgelegt ist, werden diakritische Markierungen ignoriert. <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKDDADA**</dt> </dl>       | Microsoft Rich Edit 3.0 und höher: Falls festgelegt, berücksichtigt der Suchvorgang arabische Kashdas. Wenn dies nicht festgelegt ist, werden k seit dem Festlegen ignoriert. <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <dt>**FR \_ MATCHWIDTH**</dt> </dl>             | Windows 8: Wenn festgelegt, werden Einzel-Byte- und Doppel-Byte-Versionen desselben Zeichens als nicht gleich betrachtet.<br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Wenn festgelegt, sucht der Vorgang nur nach ganzen Wörtern, die mit der Suchzeichenfolge übereinstimmen. Wenn nicht festgelegt, sucht der Vorgang auch nach Wortfragmenten, die mit der Suchzeichenfolge übereinstimmen.<br/>                                                                                                                                                                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**FINDTEXT-Struktur,**](/windows/win32/api/richedit/ns-richedit-findtexta) die Informationen zum Find-Vorgang enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Zielzeichenfolge gefunden wird, ist der Rückgabewert die nullbasierte Position des ersten Zeichens der Übereinstimmung. Wenn das Ziel nicht gefunden wird, ist der Rückgabewert -1.

## <a name="remarks"></a>Bemerkungen

Der **cpMin-Member** **von FINDTEXT.chrg** gibt immer den Ausgangspunkt der Suche an, und **cpMax** gibt den Endpunkt an. Bei der Rückwärtssuche **muss cpMin** gleich oder größer als **cpMax sein.** Bei der Vorwärtssuche erweitert der Wert -1 in **cpMax** den Suchbereich bis zum Ende des Texts.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Findtext**](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





