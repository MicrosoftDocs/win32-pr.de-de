---
description: Im folgenden finden Sie die Flicks-Konstanten.
ms.assetid: 21aaf8f0-13b7-4f97-ad4a-3557a7020337
title: Flicks-Konstanten (tabflicks. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9a83f9a35a2c1a9cbd7c4b048a8c985f5eea34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129536"
---
# <a name="flicks-constants"></a>Flicks-Konstanten

Im folgenden finden Sie die Flicks-Konstanten.



| Konstante/Wert                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FLICK_WM_HANDLED_MASK"></span><span id="flick_wm_handled_mask"></span><dl> <dt>**Flicke \_ Mit WM \_ behandelte \_ Maske**</dt> <dt>0x1</dt> </dl> | Der Wert, der nach der Verarbeitung der [**WM- \_ Tablet- \_ Nachricht**](wm-tablet-flick-message.md) zurückgegeben werden soll. Wenn die von **Flick \_ WM \_ behandelte \_ Maske** zurückgegeben wird, erfolgt keine weitere Aktion. Andernfalls sendet Windows nach Verfolgungs Benachrichtigungen, wie z. b. [**WM \_ appcommand**](/windows/desktop/inputdev/wm-appcommand), [**WM \_ VScroll**](/windows/desktop/Controls/wm-vscroll)oder [**WM \_ KeyDown**](/windows/desktop/inputdev/wm-keydown), je nachdem, welche Aktion dem Stift Flick zugeordnet ist. <br/> |
| <span id="NUM_FLICK_DIRECTIONS"></span><span id="num_flick_directions"></span><dl> <dt>**NUM \_ \_Richtung**</dt> <dt>8</dt> </dl>       | Die Anzahl der Richtungen, die in der [**flieration der flimerrichtung**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection) definiert sind.<br/>                                                                                                                                                                                                                                                                                                                                                              |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Tabflicks. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Flickdirection-Enumeration**](/windows/desktop/api/tabflicks/ne-tabflicks-flickdirection)
</dt> <dt>

[**WM- \_ Tablet \_ Flick-Nachricht**](wm-tablet-flick-message.md)
</dt> <dt>

[Gesten Flicks](flicks-gestures.md)
</dt> <dt>

[Reagieren auf Pen-Flicks](/previous-versions//dd356077(v=vs.85))
</dt> </dl>

 

