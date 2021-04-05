---
title: EM_SETIMEOPTIONS Meldung (RichEdit. h)
description: Legt die Optionen für den Eingabemethoden-Editor (IME) fest.
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- Windows-Steuerelemente für EM_SETIMEOPTIONS Meldung
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
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859013"
---
# <a name="em_setimeoptions-message"></a>EM- \_ /timeoptions-Meldung

Legt die Optionen für den Eingabemethoden-Editor (IME) fest.

> [!Note]  
> Diese Meldung wird nur in asiatischen Sprachversionen von Microsoft Rich Edit 1,0 unterstützt. Sie wird in späteren Versionen nicht unterstützt.

 

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt einen der folgenden Werte an.



| Wert                                                                                                                                             | Bedeutung                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ECOOP- \_ Satz**</dt> </dl> | Legt die Optionen auf die von *LPARAM* angegebenen Optionen fest.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ oder**</dt> </dl>    | Kombiniert die angegebenen Optionen mit den aktuellen Optionen.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ und**</dt> </dl> | Behält nur die aktuellen Optionen bei, die auch von *LPARAM* angegeben werden.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP- \_ Xor**</dt> </dl> | Logisch exklusiv oder die aktuellen Optionen mit den von *LPARAM* angegebenen Optionen.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt einen der folgenden Werte an.



| Wert                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <dt>**IMF \_ closestatus Window**</dt> </dl> | Schließt das Fenster "IME-Status", wenn das Steuerelement den Eingabefokus erhält.<br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <dt>**IMF \_ forceactive**</dt> </dl>                   | Aktiviert den IME, wenn das Steuerelement den Eingabefokus erhält.<br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <dt>**IMF \_ forcedeaktivieren**</dt> </dl>                | Deaktiviert den IME, wenn das Steuerelement den Eingabefokus erhält.<br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <dt>**IMF \_ forceenable**</dt> </dl>                   | Aktiviert den IME, wenn das Steuerelement den Eingabefokus erhält.<br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <dt>**IMF \_ forceingeactive**</dt> </dl>             | Deaktiviert den IME, wenn das Steuerelement den Eingabefokus erhält.<br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <dt>**IMF ( \_ forcenone)**</dt> </dl>                         | Deaktiviert die IME-Behandlung.<br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <dt>**IMF- \_ forceremember**</dt> </dl>             | Stellt den vorherigen IME-Status wieder her, wenn das Steuerelement den Eingabefokus erhält.<br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <dt>**IWF \_ multipleedit**</dt> </dl>                | Gibt an, dass die Kompositions Zeichenfolge nicht abgebrochen oder durch Fokus Änderungen bestimmt wird. Dies ermöglicht es einer Anwendung, separate Kompositions Zeichenfolgen für jedes Rich Edit-Steuerelement zu haben.<br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <dt>**IMF ( \_ vertikal)**</dt> </dl>                            | Hinweis wird in Rich Edit 2,0 und höher verwendet. <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich ist, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn der Vorgang fehlschlägt, ist der Rückgabewert 0 (null).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ getIMEOptions**](em-getimeoptions.md)
</dt> </dl>

 

 





