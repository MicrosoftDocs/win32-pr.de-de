---
title: TBM_SETPOSNOTIFY Meldung (kommstrg. h)
description: Legt die aktuelle logische Position des Schiebereglers in einer TrackBar fest.
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- Windows-Steuerelemente für TBM_SETPOSNOTIFY Meldung
topic_type:
- apiref
api_name:
- TBM_SETPOSNOTIFY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 636a2add9f13470a89b312450f1a3dcbc185be2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475912"
---
# <a name="tbm_setposnotify-message"></a>TBM- \_ setposnotify-Nachricht

Legt die aktuelle logische Position des Schiebereglers in einer TrackBar fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

wParam wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Neue logische Position des Schiebereglers. Gültige logische Positionen sind die ganzzahligen Werte in der TrackBar-Bereich der minimalen bis maximalen Schieberegler-Positionen. Wenn dieser Wert außerhalb des maximalen und minimalen Bereichs des Steuer Elements liegt, wird die Position auf den maximalen oder minimalen Wert festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Durch den Aufruf von **TBM \_ setposnotify** wird der Schieberegler für den Schieberegler festgelegt, [**z. b. TBM- \_ SetPos**](tbm-setpos.md) . Dies bewirkt jedoch auch, dass die TrackBar das übergeordnete Element über eine " [**WM \_ HScroll**](wm-hscroll.md) "-oder " [**WM \_ VScroll**](wm-vscroll.md) "-Meldung

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





