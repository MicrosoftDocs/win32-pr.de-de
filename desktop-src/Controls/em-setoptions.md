---
title: EM_SETOPTIONS Meldung (RichEdit. h)
description: Legt die Optionen für ein Rich-Edit-Steuerelement fest.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- Windows-Steuerelemente für EM_SETOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_SETOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c43dda8268b42dc264a86600826d2a6b550e35c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103491"
---
# <a name="em_setoptions-message"></a>EM- \_ Nachricht

Legt die Optionen für ein Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Vorgang an, bei dem es sich um einen der folgenden Werte handeln kann.



| Wert                                                                                                                                             | Bedeutung                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ECOOP- \_ Satz**</dt> </dl> | Legt die Optionen auf die von *LPARAM* angegebenen Optionen fest.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ oder**</dt> </dl>    | Kombiniert die angegebenen Optionen mit den aktuellen Optionen.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ und**</dt> </dl> | Behält nur die aktuellen Optionen bei, die auch von *LPARAM* angegeben werden.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP- \_ Xor**</dt> </dl> | Logisch exklusiv oder die aktuellen Optionen mit den von *LPARAM* angegebenen Optionen.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt einen oder mehrere der folgenden Werte an.



| Wert                                                                                                                                                                                 | Bedeutung                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <dt>**" \_ ecoautowordselection"**</dt> </dl> | Automatische Auswahl von Word bei Doppelklick.<br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <dt>**\_ecoautovscroll**</dt> </dl>                   | Identisch mit [**dem \_ autovscroll**](rich-edit-control-styles.md) -Stil von es.<br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <dt>**\_ecoautohscroll**</dt> </dl>                   | Identisch mit [**dem \_ autohscroll**](rich-edit-control-styles.md) -Stil von es.<br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <dt>**Öko- \_ nohidesel**</dt> </dl>                         | Identisch mit [**es \_ nohidesel**](rich-edit-control-styles.md) Style.<br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <dt>**nur für die Umweltschutz \_**</dt> </dl>                            | Identisch mit dem schreibgeschützten Stil von [**es \_**](rich-edit-control-styles.md) .<br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <dt>**\_ecowantreturn**</dt> </dl>                      | Identisch mit [**es \_ wantreturn**](rich-edit-control-styles.md) Style.<br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <dt>**Öko- \_ selectionbar**</dt> </dl>                | Identisch mit dem- [**\_ selectionbar**](rich-edit-control-styles.md) -Stil.<br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <dt>**Umwelt \_ vertikal**</dt> </dl>                            | Identisch mit [**dem \_ vertikalen**](rich-edit-control-styles.md) Stil. Nur in den Versionen der asiatischen Sprache verfügbar.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die aktuellen Optionen des Bearbeitungs Steuer Elements zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rich Edit-Steuerelement Stile**](rich-edit-control-styles.md)
</dt> </dl>

 

 





