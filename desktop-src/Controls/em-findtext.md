---
title: EM_FINDTEXT Meldung (RichEdit. h)
description: Sucht Text in einem Rich-Edit-Steuerelement.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- Windows-Steuerelemente für EM_FINDTEXT Meldung
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
ms.openlocfilehash: 9e50034337f05d2df17af777986136881c503d05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956644"
---
# <a name="em_findtext-message"></a>EM \_ FindText-Nachricht

Sucht Text in einem Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Geben Sie die Parameter für den Suchvorgang an. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**Fr \_ nach unten**</dt> </dl>                               | Microsoft Rich Edit 2,0 und höher: Wenn festgelegt, erfolgt die Suche vom Ende der aktuellen Auswahl bis zum Ende des Dokuments. Wenn nicht festgelegt, erfolgt die Suche vom Ende der aktuellen Auswahl bis zum Anfang des Dokuments. <br/> Microsoft Rich Edit 1,0: das FR- \_ down-Flag wird ignoriert. Die Suche erfolgt immer vom Ende der aktuellen Auswahl bis zum Ende des Dokuments.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**Fr \_ MatchAlefHamza**</dt> </dl> | Microsoft Rich Edit 3,0 und höher: Wenn diese Einstellung festgelegt ist, unterscheidet die Suche zwischen arabischen Alefs und unterschiedlichen Akzenten. Wenn nicht festgelegt, werden alle Alefs nur mit dem Alef-Zeichen abgeglichen. <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**Fr \_ matchdiac**</dt> </dl>                | Microsoft Rich Edit 3,0 und höher: Wenn festgelegt, betrachtet der Suchvorgang arabische und hebräische diakritische Zeichen. Wenn nicht festgelegt, werden Diakritische Markierungen ignoriert. <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**Fr \_ MatchKashida**</dt> </dl>       | Microsoft Rich Edit 3,0 und höher: Wenn festgelegt, betrachtet der Suchvorgang arabische Kashidas. Wenn nicht festgelegt, werden Kashidas ignoriert. <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <dt>**Fr \_ matchwidth**</dt> </dl>             | Windows 8: Wenn Set, werden Einzel Byte-und Doppelbyte Versionen desselben Zeichens als ungleich betrachtet.<br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**"# \_ wholeword"**</dt> </dl>                | Wenn festgelegt, sucht der Vorgang nur nach ganzen Wörtern, die der Such Zeichenfolge entsprechen. Wenn nicht festgelegt, sucht der Vorgang auch nach Word-Fragmenten, die der Such Zeichenfolge entsprechen.<br/>                                                                                                                                                                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**FindText**](/windows/win32/api/richedit/ns-richedit-findtexta) -Struktur, die Informationen über den Suchvorgang enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Ziel Zeichenfolge gefunden wird, ist der Rückgabewert die null basierte Position des ersten Zeichens der Entsprechung. Wenn das Ziel nicht gefunden wird, ist der Rückgabewert-1.

## <a name="remarks"></a>Bemerkungen

Der **cpmin** -Member von **FindText. chrg** gibt immer den Anfangspunkt der Suche an, und **cpmax** gibt den Endpunkt an. Bei der Rückwärtssuche muss **cpmin** größer oder gleich **cpmax** sein. Bei der Suche wird durch den Wert-1 in **cpmax** der Suchbereich auf das Ende des Texts erweitert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





