---
title: TTM_GETDELAYTIME Meldung (kommstrg. h)
description: Ruft die anfänglichen, Popup-und neuanschau Dauer ab, die aktuell für ein QuickInfo-Steuerelement festgelegt sind.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- Windows-Steuerelemente für TTM_GETDELAYTIME Meldung
topic_type:
- apiref
api_name:
- TTM_GETDELAYTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff8c75f078465646333cae1f519049733a0c9f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342435"
---
# <a name="ttm_getdelaytime-message"></a>TTM \_ getdelta-Zeit Nachricht

Ruft die anfänglichen, Popup-und neuanschau Dauer ab, die aktuell für ein QuickInfo-Steuerelement festgelegt sind.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag, das angibt, welcher Duration-Wert abgerufen wird. Dieser Parameter kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                      | Bedeutung                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**ttdt- \_ autopop**</dt> </dl> | Ruft die Zeitspanne ab, die das QuickInfo-Fenster sichtbar bleibt, wenn der Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär ist.<br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**ttdt- \_ Initial**</dt> </dl> | Ruft die Zeitspanne ab, die der Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär bleiben muss, bevor das QuickInfo-Fenster angezeigt wird.<br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**ttdt \_ erneut anzeigen**</dt> </dl>    | Ruft die Zeitspanne ab, die benötigt wird, bis nachfolgende QuickInfo-Fenster angezeigt werden, wenn der Zeiger von einem Tool zu einem anderen verschoben wird.<br/>         |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen int-Wert mit der angegebenen Dauer in Millisekunden zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TTM \_ setdelta Time**](ttm-setdelaytime.md)
</dt> </dl>

 

 





