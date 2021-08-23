---
description: Im Folgenden finden Sie die Flicks-Konstanten.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Flicks-Konstanten (Tabflicks.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e927d0715c9f34e7e1db979c32545a0d8c8efad18186192a751f2cdbed13172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092647"
---
# <a name="flicks-constants"></a>Flicks-Konstanten

Im Folgenden finden Sie die Flicks-Konstanten.



| Konstante/Wert                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <dt>**FLICK \_ WM \_ HANDLED \_ MASK**</dt> <dt>0x1</dt> </dl> | Der Wert, der nach der Behandlung der [**WM \_ TABLET \_ FLICK-Meldungsmeldung zurückkommen**](wm-tablet-flick-message.md) soll. Wenn **FLICK \_ WM \_ HANDLED \_ MASK** zurückgegeben wird, erfolgt keine weitere Aktion. Andernfalls sendet Windows Folgebenachrichtigungen, z. B. [**WM \_ APPCOMMAND,**](/windows/desktop/inputdev/wm-appcommand) [**WM \_ VSCROLL**](/windows/desktop/Controls/wm-vscroll)oder [**WM \_ KEYDOWN,**](/windows/desktop/inputdev/wm-keydown)je nachdem, welche Aktion dem Stiftflick zugeordnet ist. <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <dt>**NUM \_ FLICK \_ DIRECTIONS**</dt> <dt>8</dt> </dl>       | Die Anzahl der in der [**FLICKDIRECTION-Enumeration definierten Richtungen.**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)<br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Tabflicks.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**FLICKDIRECTION-Enumeration**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[**WM \_ TABLET \_ FLICK Message**](wm-tablet-flick-message.md)
</dt> <dt>

[Flicks-Gesten](flicks-gestures.md)
</dt> <dt>

[Reagieren auf Stiftflicks](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

