---
title: EM_FINDTEXTW Meldung (RichEdit. h)
description: Findet Unicode-Text in einem Rich-Edit-Steuerelement.
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- Windows-Steuerelemente für EM_FINDTEXTW Meldung
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e8bae60269ab3ddb84a17c285c243e00d8117c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742825"
---
# <a name="em_findtextw-message"></a>EM \_ findtextw-Meldung

Findet Unicode-Text in einem Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die Parameter für den Suchvorgang an. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**Fr \_ nach unten**</dt> </dl>                               | Wenn festgelegt, sucht der Vorgang vom Ende der aktuellen Auswahl bis zum Ende des Dokuments. Wenn nicht festgelegt, wird der Vorgang vom Ende der aktuellen Auswahl bis zum Anfang des Dokuments durchsucht.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**Fr \_ MatchAlefHamza**</dt> </dl> | In der Standardeinstellung werden alle arabischen und hebräischen Alefs mit unterschiedlichen Akzenten mit dem Alef-Zeichen übereinstimmen. Legen Sie dieses Flag fest, wenn Sie möchten, dass die Suche zwischen Alefs und unterschiedlichen Akzenten unterscheidet.<br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**Fr \_ MatchCase**</dt> </dl>                | Wenn festgelegt, wird bei der Suche die Groß-/Kleinschreibung beachtet. Wenn nicht festgelegt, wird bei der Suche die Groß-/Kleinschreibung nicht beachtet.<br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**Fr \_ matchdiac**</dt> </dl>                | Standardmäßig werden die diakritischen Zeichen Arabisch und Hebräisch ignoriert. Legen Sie dieses Flag fest, wenn Sie möchten, dass der Suchvorgang diakritische Zeichen berücksichtigt.<br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**Fr \_ MatchKashida**</dt> </dl>       | Standardmäßig werden arabische und hebräische Kashidas ignoriert. Legen Sie dieses Flag fest, wenn der Suchvorgang Kashidas berücksichtigt.<br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**"# \_ wholeword"**</dt> </dl>                | Wenn festgelegt, sucht der Vorgang nur nach ganzen Wörtern, die der Such Zeichenfolge entsprechen. Wenn nicht festgelegt, sucht der Vorgang auch nach Word-Fragmenten, die der Such Zeichenfolge entsprechen.<br/>                                  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**findtextw**](/windows/win32/api/richedit/ns-richedit-findtexta) -Struktur, die Informationen über den Suchvorgang enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Ziel Zeichenfolge gefunden wird, ist der Rückgabewert die null basierte Position des ersten Zeichens der Entsprechung. Wenn das Ziel nicht gefunden wird, ist der Rückgabewert-1.

## <a name="remarks"></a>Bemerkungen

**EM \_ Findtextw** verwendet die [**findtextw**](/windows/win32/api/richedit/ns-richedit-findtexta) -Struktur, während [**EM \_ findtextexw**](em-findtextexw.md) die [**findtextexw**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) -Struktur verwendet. Der Unterschied besteht darin, dass **findtextexw** den Textbereich zurückgibt, der gefunden wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ findtextexw**](em-findtextexw.md)
</dt> </dl>

 

 





