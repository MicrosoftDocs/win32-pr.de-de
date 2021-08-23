---
title: TBM_SETBUDDY Meldung (Commctrl.h)
description: Weist ein Fenster als Fenster für ein Trackbar-Steuerelement zu. Trackbar-Fenster werden automatisch an einer Position relativ zur Ausrichtung des Steuerelements (horizontal oder vertikal) angezeigt.
ms.assetid: ab35911f-bf81-47f3-98aa-0901aa877dea
keywords:
- TBM_SETBUDDY Windows-Steuerelemente für Nachrichten
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
ms.openlocfilehash: e4f2586c84740cb2d5e8b1f1aadfb910cd241270d3e18363accf1f166c3c35ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167186"
---
# <a name="tbm_setbuddy-message"></a>TBM \_ SETBUDDY-Nachricht

Weist ein Fenster als Fenster für ein Trackbar-Steuerelement zu. Trackbar-Fenster werden automatisch an einer Position relativ zur Ausrichtung des Steuerelements (horizontal oder vertikal) angezeigt.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Wert, der den Speicherort angibt, an dem das Fenster angezeigt werden soll. Die folgenden Werte sind möglich:



| Wert                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>**STIMMT**</dt> </dl>    | Die Leiste wird links von der Trackleiste angezeigt, wenn das Trackbar-Steuerelement den [**TBS \_ HORZ-Stil**](trackbar-control-styles.md) verwendet. Wenn die Trackleiste den [**\_ TBS-VERT-Stil**](trackbar-control-styles.md) verwendet, wird die Leiste über dem Trackbar-Steuerelement angezeigt.<br/>  |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>**FALSE**</dt> </dl> | Die Leiste wird rechts neben der Trackleiste angezeigt, wenn das Trackbar-Steuerelement den [**TBS \_ HORZ-Stil**](trackbar-control-styles.md) verwendet. Wenn die Trackleiste den [**\_ TBS-VERT-Stil**](trackbar-control-styles.md) verwendet, wird die Leiste unterhalb des Trackbar-Steuerelements angezeigt.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle für das Fenster, das als Ziehpunkt des Trackbar-Steuerelements festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt das Handle für das Fenster zurück, das zuvor dem Steuerelement an dieser Position zugewiesen wurde.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Trackbar-Steuerelemente unterstützen bis zu zwei Fenster. Dies kann nützlich sein, wenn Sie Text oder Bilder an jedem Ende des Steuerelements anzeigen müssen.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





