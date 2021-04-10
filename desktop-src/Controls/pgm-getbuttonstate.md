---
title: PGM_GETBUTTONSTATE Meldung (kommstrg. h)
description: Ruft den Zustand der angegebenen Schaltfläche in einem Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das Pager \_ GetButtonState-Makro verwenden.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- Windows-Steuerelemente für PGM_GETBUTTONSTATE Meldung
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
ms.openlocfilehash: 3d8c9eebbc0aa91651a01de1fe193544f0c8afcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956807"
---
# <a name="pgm_getbuttonstate-message"></a>PGM- \_ GetButtonState-Meldung

Ruft den Zustand der angegebenen Schaltfläche in einem Pager-Steuerelement ab. Sie können diese Nachricht explizit senden oder das [**Pager \_ GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) -Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Gibt an, für welche Schaltfläche der Status abgerufen werden soll. Mögliche Werte:



| Wert                                                                                                                                                                     | Bedeutung                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <dt>**PGB- \_ toporleft**</dt> </dl>             | Gibt die oberste Schaltfläche in einem [**PGS \_**](pager-control-styles.md) -Steuerelement "Pager" oder die linke Schaltfläche in einem [**PGS- \_ Horz**](pager-control-styles.md) -Pager-Steuerelement an <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <dt>**PGB \_ bottomorright**</dt> </dl> | Gibt die untere Schaltfläche in einem [**PGS \_**](pager-control-styles.md) -Steuerelement des Pager-Steuer Elements oder die Rechte Taste in einem [**PGS- \_ Horz**](pager-control-styles.md) -Pager-Steuerelement <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Zustand der in *LPARAM* angegebenen Schaltfläche zurück. Dabei handelt es sich um einen oder mehrere der folgenden Werte (wenn mehr als ein Wert zurückgegeben wird, werden Sie mit einem bitweisen OR kombiniert):



| Rückgabecode                                                                                   | Beschreibung                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <dt>**pgf \_ unsichtbar**</dt> </dl> | Die Schaltfläche ist nicht sichtbar. <br/>      |
| <dl> <dt>**pgf \_ Normal**</dt> </dl>    | Die Schaltfläche befindet sich im normalen Zustand. <br/>  |
| <dl> <dt>**pgf-abgeblendet \_**</dt> </dl>    | Die Schaltfläche befindet sich in einem ausgefallenen Zustand. <br/>  |
| <dl> <dt>**pgf- \_ depressiv**</dt> </dl> | Die Schaltfläche befindet sich im gedrückten Zustand. <br/> |
| <dl> <dt>**pgf- \_ heiß**</dt> </dl>       | Die Schaltfläche befindet sich im aktiven Zustand. <br/>     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





