---
title: EM_SETOPTIONS (Richedit.h)
description: Legt die Optionen für ein Rich-Edit-Steuerelement fest.
ms.assetid: 98ef2de9-4c34-45ba-8e8a-eaf505f97f56
keywords:
- EM_SETOPTIONS meldungssteuerelemente Windows
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
ms.openlocfilehash: a5d5c4b7fd9e92261cedaf0681523ad0a3e25a37aa2814f6c00d0d9460e94bb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672609"
---
# <a name="em_setoptions-message"></a>EM \_ SETOPTIONS-Meldung

Legt die Optionen für ein Rich-Edit-Steuerelement fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt den Vorgang an, bei dem es sich um einen dieser Werte handelt.



| Wert                                                                                                                                             | Bedeutung                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ECOOP \_ SET**</dt> </dl> | Legt die Optionen auf die von *lParam angegebenen fest.*<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ ODER**</dt> </dl>    | Kombiniert die angegebenen Optionen mit den aktuellen Optionen.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ UND**</dt> </dl> | Behält nur die aktuellen Optionen bei, die auch von *lParam angegeben werden.*<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ XOR**</dt> </dl> | Logisch exklusiv ODER die aktuellen Optionen mit den von *lParam angegebenen*.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Gibt einen oder mehrere der folgenden Werte an.



| Wert                                                                                                                                                                                 | Bedeutung                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="ECO_AUTOWORDSELECTION"></span><span id="eco_autowordselection"></span><dl> <dt>**ECO \_ AUTOWORDSELECTION**</dt> </dl> | Automatische Auswahl des Worts bei Doppelklick.<br/>                                                                           |
| <span id="ECO_AUTOVSCROLL"></span><span id="eco_autovscroll"></span><dl> <dt>**ECO \_ AUTOVSCROLL**</dt> </dl>                   | Identisch mit [**dem ES \_ AUTOVSCROLL-Stil.**](rich-edit-control-styles.md)<br/>                                      |
| <span id="ECO_AUTOHSCROLL"></span><span id="eco_autohscroll"></span><dl> <dt>**ECO \_ AUTOHSCROLL**</dt> </dl>                   | Identisch mit [**dem ES \_ AUTOHSCROLL-Stil.**](rich-edit-control-styles.md)<br/>                                      |
| <span id="ECO_NOHIDESEL"></span><span id="eco_nohidesel"></span><dl> <dt>**ECO \_ NOHIDESEL**</dt> </dl>                         | Identisch mit [**dem ES \_ NOHIDESEL-Stil.**](rich-edit-control-styles.md)<br/>                                          |
| <span id="ECO_READONLY"></span><span id="eco_readonly"></span><dl> <dt>**ECO \_ READONLY**</dt> </dl>                            | Identisch mit [**dem ES \_ READONLY-Stil.**](rich-edit-control-styles.md)<br/>                                            |
| <span id="ECO_WANTRETURN"></span><span id="eco_wantreturn"></span><dl> <dt>**ECO \_ WANTRETURN**</dt> </dl>                      | Identisch mit [**dem ES \_ WANTRETURN-Stil.**](rich-edit-control-styles.md)<br/>                                        |
| <span id="ECO_SELECTIONBAR"></span><span id="eco_selectionbar"></span><dl> <dt>**\_E/A-AUSWAHLLEISTE**</dt> </dl>                | Identisch mit [**dem ES \_ SELECTIONBAR-Stil.**](rich-edit-control-styles.md)<br/>                                    |
| <span id="ECO_VERTICAL"></span><span id="eco_vertical"></span><dl> <dt>**ECO \_ VERTICAL**</dt> </dl>                            | Identisch mit [**DEM ES \_ VERTICAL-Stil.**](rich-edit-control-styles.md) Nur in asiatisch-sprachbasierten Versionen verfügbar.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Meldung gibt die aktuellen Optionen des Bearbeitungssteuer steuerelements zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Rich Edit-Steuerelementstile**](rich-edit-control-styles.md)
</dt> </dl>

 

 





