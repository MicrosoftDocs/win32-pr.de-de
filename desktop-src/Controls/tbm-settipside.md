---
title: TBM_SETTIPSIDE Meldung (kommstrg. h)
description: Positioniert ein QuickInfo-Steuerelement von einem TrackBar-Steuerelement. TrackBar-Steuerelemente, die den TSB-Tooltips-Stil verwenden, zeigen Quick Infos an \_ .
ms.assetid: 40a0eeb0-7bb4-4102-98ea-ee664799b934
keywords:
- Windows-Steuerelemente für TBM_SETTIPSIDE Meldung
topic_type:
- apiref
api_name:
- TBM_SETTIPSIDE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56c3ab1f6c601d9b243977d147f7503ce99788e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391714"
---
# <a name="tbm_settipside-message"></a>TBM- \_ Nachricht

Positioniert ein QuickInfo-Steuerelement von einem TrackBar-Steuerelement. TrackBar-Steuerelemente, die den [**TSB- \_ Tooltips**](trackbar-control-styles.md) -Stil verwenden, zeigen Quick Infos an.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wert, der die Position darstellt, an der das QuickInfo-Steuerelement angezeigt werden soll Die folgenden Werte sind möglich:



| Wert                                                                                                                                                   | Bedeutung                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBTS_TOP"></span><span id="tbts_top"></span><dl> <dt>**tbts- \_ Top**</dt> </dl>          | Das QuickInfo-Steuerelement befindet sich über der TrackBar. Dieses Flag ist für die Verwendung mit horizontalen trackbars vorgesehen.<br/>         |
| <span id="TBTS_LEFT"></span><span id="tbts_left"></span><dl> <dt>**tbts \_ Links**</dt> </dl>       | Das ToolTip-Steuerelement wird auf der linken Seite der TrackBar positioniert. Dieses Flag ist für die Verwendung mit vertikalen trackbars vorgesehen.<br/>  |
| <span id="TBTS_BOTTOM"></span><span id="tbts_bottom"></span><dl> <dt>**tbts \_ unten**</dt> </dl> | Das QuickInfo-Steuerelement befindet sich unterhalb der TrackBar. Dieses Flag ist für die Verwendung mit horizontalen trackbars vorgesehen.<br/>         |
| <span id="TBTS_RIGHT"></span><span id="tbts_right"></span><dl> <dt>**tbts \_ right**</dt> </dl>    | Das QuickInfo-Steuerelement wird auf der rechten Seite der TrackBar positioniert. Dieses Flag ist für die Verwendung mit vertikalen trackbars vorgesehen.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der die vorherige Position des QuickInfo-Steuer Elements darstellt. Der Rückgabewert ist mit einem der möglichen Werte für *wParam* gleich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





