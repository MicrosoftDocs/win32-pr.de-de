---
title: TTM_GETDELAYTIME Nachricht (Commctrl.h)
description: Ruft die anfänglichen, Popup- und Wiederholungsdauern ab, die derzeit für ein QuickInfo-Steuerelement festgelegt sind.
ms.assetid: f89a75ed-ba80-4741-927f-c571f3b2efe7
keywords:
- TTM_GETDELAYTIME Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: f0e63eca126477a6f602e6e23be75495319d30aa2814d2d72b8426a96c078326
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769260"
---
# <a name="ttm_getdelaytime-message"></a>TTM \_ GETDELAYTIME-Nachricht

Ruft die anfänglichen, Popup- und Wiederholungsdauern ab, die derzeit für ein QuickInfo-Steuerelement festgelegt sind.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Flag, das angibt, welcher Wert für die Dauer abgerufen wird. Dieser Parameter kann einen der folgenden Werte aufweisen:



| Wert                                                                                                                                                      | Bedeutung                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTDT_AUTOPOP"></span><span id="ttdt_autopop"></span><dl> <dt>**TTDT \_ AUTOPOP**</dt> </dl> | Rufen Sie den Zeitraum ab, in dem das QuickInfo-Fenster sichtbar bleibt, wenn der Zeiger im umgrenzten Rechteck eines Tools stationär ist.<br/>      |
| <span id="TTDT_INITIAL"></span><span id="ttdt_initial"></span><dl> <dt>**TTDT \_ INITIAL**</dt> </dl> | Rufen Sie ab, wie lange der Zeiger innerhalb des umgrenzenden Rechtecks eines Tools stationär bleiben muss, bevor das QuickInfo-Fenster angezeigt wird.<br/> |
| <span id="TTDT_RESHOW"></span><span id="ttdt_reshow"></span><dl> <dt>**TTDT \_ RESHOW**</dt> </dl>    | Rufen Sie ab, wie lange es dauert, bis nachfolgende QuickInfo-Fenster angezeigt werden, während der Zeiger von einem Tool zu einem anderen bewegt wird.<br/>         |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt und den INT-Wert mit der angegebenen Dauer in Millisekunden zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TTM \_ SETDELAYTIME**](ttm-setdelaytime.md)
</dt> </dl>

 

 





