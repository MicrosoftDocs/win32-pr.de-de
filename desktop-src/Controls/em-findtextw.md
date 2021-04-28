---
title: EM_FINDTEXTW (Richedit.h)
description: 'EM_FINDTEXTW Meldung: Sucht Unicode-Text in einem Rich-Edit-Steuerelement.'
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 325ff948c4c8f03e8051248f15928d8e8c56e52f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109798"
---
# <a name="em_findtextw-message"></a>EM \_ FINDTEXTW-Nachricht

Sucht Unicode-Text in einem Rich-Edit-Steuerelement.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt die Parameter des Suchvorgang an. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_ DOWN**</dt> </dl>                               | Wenn festgelegt, durchsucht der Vorgang vom Ende der aktuellen Auswahl bis zum Ende des Dokuments. Wenn nicht festgelegt, durchsucht der Vorgang vom Ende der aktuellen Auswahl bis zum Anfang des Dokuments.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**FR \_ MATCHALEFHAMZA**</dt> </dl> | Standardmäßig werden arabische und hebräische Alefs mit unterschiedlichen Akzenten durch das Alef-Zeichen übereinstimmen. Legen Sie dieses Flag fest, wenn bei der Suche zwischen Alefs mit unterschiedlichen Akzenten unterschieden werden soll.<br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ MATCHCASE**</dt> </dl>                | Wenn festgelegt, wird beim Suchvorgang die Kleinschreibung beachtet. Wenn dies nicht festgelegt ist, wird beim Suchvorgang die Groß-/Kleinschreibung nicht beachtet.<br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**FR \_ MATCHDMATCH**</dt> </dl>                | Standardmäßig werden arabische und hebräische diakritische Markierungen ignoriert. Legen Sie dieses Flag fest, wenn der Suchvorgang diakritische Markierungen berücksichtigen soll.<br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Standardmäßig werden arabische und hebräische Kashdas ignoriert. Legen Sie dieses Flag fest, wenn der Suchvorgang Kashdas berücksichtigen soll.<br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**FR \_ WHOLEWORD**</dt> </dl>                | Wenn diese Einstellung festgelegt ist, sucht der Vorgang nur nach ganzen Wörtern, die mit der Suchzeichenfolge übereinstimmen. Wenn diese Einstellung nicht festgelegt ist, sucht der Vorgang auch nach Wortfragmenten, die mit der Suchzeichenfolge übereinstimmen.<br/>                                  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Eine [**FINDTEXTW-Struktur,**](/windows/win32/api/richedit/ns-richedit-findtexta) die Informationen zum Suchvorgang enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Zielzeichenfolge gefunden wird, ist der Rückgabewert die nullbasierte Position des ersten Zeichens der Übereinstimmung. Wenn das Ziel nicht gefunden wird, lautet der Rückgabewert -1.

## <a name="remarks"></a>Bemerkungen

**EM \_ FINDTEXTW** verwendet die [**FINDTEXTW-Struktur,**](/windows/win32/api/richedit/ns-richedit-findtexta) [**während EM \_ FINDTEXTEXW**](em-findtextexw.md) die [**FINDTEXTEXW-Struktur**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) verwendet. Der Unterschied besteht darin, dass **FINDTEXTEXW** den gefundenen Textbereich zurückmeldet.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EM \_ FINDTEXTEXW**](em-findtextexw.md)
</dt> </dl>

 

 





