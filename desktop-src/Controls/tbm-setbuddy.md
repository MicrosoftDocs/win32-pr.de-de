---
title: TBM_SETBUDDY Meldung (kommstrg. h)
description: Weist ein Fenster als Buddy-Fenster für ein TrackBar-Steuerelement zu. TrackBar-Buddy-Fenster werden automatisch an einem Speicherort relativ zur Ausrichtung des Steuer Elements angezeigt (horizontal oder vertikal).
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- Windows-Steuerelemente für TBM_SETBUDDY Meldung
topic_type:
- apiref
api_name:
- TBM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab33e53117933390d7a34ec75a49724003255108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040308"
---
# <a name="tbm_setbuddy-message"></a>TBM- \_ SetBuddy-Nachricht

Weist ein Fenster als Buddy-Fenster für ein TrackBar-Steuerelement zu. TrackBar-Buddy-Fenster werden automatisch an einem Speicherort relativ zur Ausrichtung des Steuer Elements angezeigt (horizontal oder vertikal).

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

-Wert, der die Position angibt, an der das Buddy-Fenster angezeigt werden soll. Die folgenden Werte sind möglich:



| Wert                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**Fall**</dt> </dl>    | Der Kumpel wird links neben der TrackBar angezeigt, wenn das TrackBar-Steuerelement den [**TSB- \_ Horz**](trackbar-control-styles.md) -Stil verwendet. Wenn die TrackBar den TSB-Stil " [**\_ Vert**](trackbar-control-styles.md) " verwendet, wird der Kumpel oberhalb des TrackBar-Steuer Elements angezeigt.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**Alarm**</dt> </dl> | Der Kumpel wird rechts von der TrackBar angezeigt, wenn das TrackBar-Steuerelement den Stil von " [**TSB \_ Horz**](trackbar-control-styles.md) " verwendet. Wenn die TrackBar den TSB-Stil " [**\_ Vert**](trackbar-control-styles.md) " verwendet, wird der Buddy unterhalb des TrackBar-Steuer Elements angezeigt.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Fenster, das als Buddy des TrackBar-Steuer Elements festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Fenster zurück, das zuvor dem Steuerelement an dieser Position zugewiesen wurde.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> TrackBar-Steuerelemente unterstützen bis zu zwei Buddy-Fenster. Dies kann hilfreich sein, wenn Sie Text oder Bilder an jedem Ende des Steuer Elements anzeigen müssen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





