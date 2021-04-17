---
title: ACM_PLAY Meldung (kommstrg. h)
description: Gibt einen AVI-Clip in einem Animations Steuerelement wieder. Das-Steuerelement spielt den Clip im Hintergrund, während der Thread weiterhin ausgeführt wird. Sie können diese Nachricht explizit oder mit dem animieren Play- \_ Makro senden.
ms.assetid: 738b7305-bb77-441d-a198-17daf3b76039
keywords:
- Windows-Steuerelemente für ACM_PLAY Meldung
topic_type:
- apiref
api_name:
- ACM_PLAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e501f3718e1b8172e2b7b16566f992c26346b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475759"
---
# <a name="acm_play-message"></a>ACM- \_ Wiedergabe Meldung

Gibt einen AVI-Clip in einem Animations Steuerelement wieder. Das-Steuerelement spielt den Clip im Hintergrund, während der Thread weiterhin ausgeführt wird. Sie können diese Nachricht explizit oder mit dem [**animieren \_ Play**](/windows/desktop/api/Commctrl/nf-commctrl-animate_play) -Makro senden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Ein **uint** , das angibt, wie oft der AVI-Clip wiedergegeben werden soll. Der Wert-1 bedeutet, dass der Clip unbegrenzt wiedergegeben wird.

</dd> <dt>

*lParam* 
</dt> <dd>

Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) ist der null basierte Index des Frames, bei dem die Wiedergabe beginnt. Der Wert muss kleiner als 65.536 sein. Der Wert NULL bedeutet, mit dem ersten Frame im AVI-Clip zu beginnen.

Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) ist der null basierte Index des Frames, bei dem die Wiedergabe beendet wird. Der Wert muss kleiner als 65.536 sein. Der Wert-1 bedeutet, dass er mit dem letzten Frame im AVI-Clip endet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg einen Wert ungleich 0 (null) zurück, andernfalls NULL.

## <a name="remarks"></a>Bemerkungen

Mithilfe von [**animieren \_ Seek**](/windows/desktop/api/Commctrl/nf-commctrl-animate_seek) können Sie das Animations Steuerelement so anleiten, dass ein bestimmter Frame des AVI-Clips angezeigt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

