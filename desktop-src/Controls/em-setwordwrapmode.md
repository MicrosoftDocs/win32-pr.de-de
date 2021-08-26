---
title: EM_SETWORDWRAPMODE Nachricht (Richedit.h)
description: Legt die Optionen "Zeilenumbruch" und "Wortumbruch" für ein Umfassendes Bearbeitungssteuerelement fest.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- EM_SETWORDWRAPMODE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b5c750bb83f4f3fb0c1acfc82b67677c36094df461d10787186177fc891df2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047980"
---
# <a name="em_setwordwrapmode-message"></a>EM \_ SETWORDWRAPMODE-Meldung

Legt die Optionen "Zeilenumbruch" und "Wortumbruch" für ein Umfassendes Bearbeitungssteuerelement fest.

> [!Note]  
> Diese Meldung wird nur in asiatisch-sprachigen Versionen von Microsoft Rich Edit 1.0 unterstützt. In späteren Versionen wird dies nicht unterstützt.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt einen oder mehrere der folgenden Werte an.



| Wert                                                                                                                                                         | Bedeutung                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <dt>**WBF \_ WORDWRAP**</dt> </dl>    | Aktiviert asiatisch spezifische Zeilenumbruchvorgänge, z. B. Kinsoku auf Japanisch. <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <dt>**WBF \_ WORDBREAK**</dt> </dl> | Aktiviert englische Wörterbruchvorgänge in Japanisch und Chinesisch. Aktiviert den Hangeul-Vorgang zum Abbrechen von Wörtern.<br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <dt>**WBF \_ OVERFLOW**</dt> </dl>    | Erkennt Überlaufpunktion. (Derzeit nicht unterstützt.)<br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <dt>**WBF \_ LEVEL1**</dt> </dl>          | Legt die Satzzeichentabelle level 1 als Standard fest.<br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <dt>**WBF \_ LEVEL2**</dt> </dl>          | Legt die Satzzeichentabelle der Ebene 2 als Standardwert fest.<br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <dt>**WBF \_ CUSTOM**</dt> </dl>          | Legt die anwendungsdefinierte Interpunktionstabelle fest.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. muss 0 (null) sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die aktuellen Zeilenumbruch- und Wörterumbruchoptionen zurück.

## <a name="remarks"></a>Hinweise

Diese Meldung darf nicht von der von der Anwendung definierten Wörterbruchprozedur gesendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



 

 





