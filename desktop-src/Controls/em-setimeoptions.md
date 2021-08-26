---
title: EM_SETIMEOPTIONS-Nachricht (Richedit.h)
description: Legt die Optionen des Eingabemethoden-Editors (Input Method Editor, IME) fest.
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- EM_SETIMEOPTIONS Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83ffae9586c3ee05f951672f0927c4f10ad2115684643af8418062bb7724c7b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048390"
---
# <a name="em_setimeoptions-message"></a>EM \_ SETIMEOPTIONS-Meldung

Legt die Optionen des Eingabemethoden-Editors (Input Method Editor, IME) fest.

> [!Note]  
> Diese Meldung wird nur in asiatisch-sprachigen Versionen von Microsoft Rich Edit 1.0 unterstützt. In späteren Versionen wird dies nicht unterstützt.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt einen der folgenden Werte an.



| Wert                                                                                                                                             | Bedeutung                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ECOOP \_ SET**</dt> </dl> | Legt die Optionen auf die von *lParam* angegebenen fest.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ ODER**</dt> </dl>    | Kombiniert die angegebenen Optionen mit den aktuellen Optionen.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ UND**</dt> </dl> | Behält nur die aktuellen Optionen bei, die auch von *lParam* angegeben werden.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ XOR**</dt> </dl> | Logisch exklusiv ODER die aktuellen Optionen mit den von *lParam* angegebenen Optionen.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt einen von mehreren der folgenden Werte an.



| Wert                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <dt>**IMF \_ CLOSESTATUSWINDOW**</dt> </dl> | Schließt das IME-Statusfenster, wenn das Steuerelement den Eingabefokus erhält.<br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <dt>**ERZWINGEN \_ VON FORCEACTIVE**</dt> </dl>                   | Aktiviert das IME, wenn das Steuerelement den Eingabefokus empfängt.<br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <dt>**IMF \_ FORCEDISABLE**</dt> </dl>                | Deaktiviert den IME, wenn das Steuerelement den Eingabefokus empfängt.<br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <dt>**\_FORCEENABLE(ERZWINGEN)**</dt> </dl>                   | Aktiviert den IME, wenn das Steuerelement den Eingabefokus empfängt.<br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <dt>**ERZWINGEN \_ VON FORCEINACTIVE**</dt> </dl>             | Deaktiviert die IME, wenn das Steuerelement den Eingabefokus empfängt.<br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <dt>**ERZWINGEN \_ VON FORCENONE**</dt> </dl>                         | Deaktiviert die IME-Verarbeitung.<br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <dt>**DIE \_ FORCEREMEMBER-ENTSENKUNG**</dt> </dl>             | Stellt den vorherigen IME-Status wieder her, wenn das Steuerelement den Eingabefokus erhält.<br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <dt>**\_VERERZUNGS MULTIPLEEDIT**</dt> </dl>                | Gibt an, dass die Kompositionszeichenfolge nicht abgebrochen oder durch Fokusänderungen bestimmt wird. Dadurch kann eine Anwendung über separate Kompositionszeichenfolgen für jedes Rich Edit-Steuerelement verfügen.<br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <dt>**VERTICAL \_ (VERTIKAL)**</dt> </dl>                            | Hinweis, der in Rich Edit 2.0 und höher verwendet wird. <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ GETIMEOPTIONS**](em-getimeoptions.md)
</dt> </dl>

 

 





