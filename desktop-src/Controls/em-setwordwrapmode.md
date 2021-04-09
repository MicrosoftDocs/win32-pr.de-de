---
title: EM_SETWORDWRAPMODE Meldung (RichEdit. h)
description: Legt die Optionen für Wort Umbruch und Wörter Trennung für ein Rich-Edit-Steuerelement fest.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- Windows-Steuerelemente für EM_SETWORDWRAPMODE Meldung
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
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040721"
---
# <a name="em_setwordwrapmode-message"></a>EM \_ setwordwrapmode-Meldung

Legt die Optionen für Wort Umbruch und Wörter Trennung für ein Rich-Edit-Steuerelement fest.

> [!Note]  
> Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt. Sie wird in späteren Versionen nicht unterstützt.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt einen oder mehrere der folgenden Werte an.



| Wert                                                                                                                                                         | Bedeutung                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <dt>**WBF- \_ WordWrap**</dt> </dl>    | Ermöglicht asiatische-spezifische Zeilenumbruch Vorgänge, wie z. b. Kinsoku in Japanisch. <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <dt>**WBF- \_ WordBreak**</dt> </dl> | Ermöglicht englische Wörter brechende Vorgänge in Japanisch und Chinesisch. Aktiviert den Vorgang zum Durchsuchen von Hangeul-Wörtern.<br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <dt>**WBF- \_ Überlauf**</dt> </dl>    | Erkennt eine Überlauf Interpunktions Zeichen. (Wird zurzeit nicht unterstützt.)<br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <dt>**WBF- \_ Level1**</dt> </dl>          | Legt die Satzzeichen Tabelle der Ebene 1 als Standard fest.<br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <dt>**WBF- \_ Level2**</dt> </dl>          | Legt die Satzzeichen Tabelle der Ebene 2 als Standard fest.<br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <dt>**\_benutzerdefiniertes WBF**</dt> </dl>          | Legt die Anwendungs definierte Interpunktions Tabelle fest.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Dieser Parameter wird nicht verwendet. Er muss NULL sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die aktuellen Optionen für Wort Umbruch und Wörter Trennung zurück.

## <a name="remarks"></a>Bemerkungen

Diese Nachricht darf nicht von der von der Anwendung definierten Wörter Trennung gesendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





