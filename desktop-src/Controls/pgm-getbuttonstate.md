---
title: PGM_GETBUTTONSTATE (Commctrl.h)
description: Ruft den Zustand der angegebenen Schaltfläche in einem Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das \_ Pager-Makro GetButtonState verwenden.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- PGM_GETBUTTONSTATE meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2014b6e36a0ab883155d786760ef54f02c89ee0d17192d6082d40ad19eec95a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830191"
---
# <a name="pgm_getbuttonstate-message"></a>PGM \_ GETBUTTONSTATE-Nachricht

Ruft den Zustand der angegebenen Schaltfläche in einem Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**\_ Pager-Makro GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Gibt an, für welche Schaltfläche der Zustand abgerufen werden soll. Mögliche Werte:



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <dt>**PGB \_ TOPORLEFT**</dt> </dl>             | Gibt die obere Schaltfläche in einem [**PGS VERT-Pager-Steuerelement \_**](pager-control-styles.md) oder die linke Schaltfläche in einem [**PGS HORZ-Pager-Steuerelement \_**](pager-control-styles.md) an. <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <dt>**PGB \_ BOTTOMORRIGHT**</dt> </dl> | Gibt die untere Schaltfläche in einem [**PGS VERT-Pager-Steuerelement \_**](pager-control-styles.md) oder die rechte Schaltfläche in einem [**PGS \_ HORZ-Pager-Steuerelement**](pager-control-styles.md) an. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Zustand der in *lParam* angegebenen Schaltfläche zurück. Dies ist einer oder mehrere der folgenden Werte (wenn mehr als ein Wert zurückgegeben wird, werden sie mit einem bitweisem OR kombiniert):



| Rückgabecode                                                                                   | Beschreibung                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**PGF \_ – UNSICHTBAR**</dt> </dl> | Die Schaltfläche ist nicht sichtbar. <br/>      |
| <dl> <dt>**PGF \_ NORMAL**</dt> </dl>    | Die Schaltfläche befindet sich im normalen Zustand. <br/>  |
| <dl> <dt>**PGF \_ GRAU**</dt> </dl>    | Die Schaltfläche befindet sich im grauen Zustand. <br/>  |
| <dl> <dt>**PGF \_ VERKNRÜCKT**</dt> </dl> | Die Schaltfläche befindet sich im gedrückten Zustand. <br/> |
| <dl> <dt>**PGF \_ HOT**</dt> </dl>       | Die Schaltfläche befindet sich im heißen Zustand. <br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





