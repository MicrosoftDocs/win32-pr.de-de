---
title: MCM_SETSELRANGE Meldung (kommstrg. h)
description: Legt die Auswahl für ein Monatskalender-Steuerelement auf einen bestimmten Datumsbereich fest. Sie können diese Nachricht explizit oder mit dem monthcal- \_ setselrange-Makro senden.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- Windows-Steuerelemente für MCM_SETSELRANGE Meldung
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad28966ab67a5e7c0d27dd8fc9c367ec30e4cd7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040169"
---
# <a name="mcm_setselrange-message"></a>MCM \_ setselrange-Nachricht

Legt die Auswahl für ein Monatskalender-Steuerelement auf einen bestimmten Datumsbereich fest. Sie können diese Nachricht explizit oder mit dem [**monthcal- \_ setselrange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf ein Array aus zwei Elementen von [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) -Strukturen, die Datumsinformationen enthalten, die die Auswahl Limits darstellen. Das erste ausgewählte Datum muss in *lpsystimearray* \[ 0 angegeben werden \] , und das Datum der letzten Auswahl muss in *lpsystimearray* \[ 1 angegeben werden \] .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL. Diese Nachricht schlägt fehl, wenn Sie auf ein Monatskalender-Steuerelement angewendet wird, das den [**MCS- \_ MultiSelect**](month-calendar-control-styles.md) -Stil nicht verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Uhrzeiten im Monatskalender-Steuerelement](month-calendar-controls.md)
</dt> </dl>

 

