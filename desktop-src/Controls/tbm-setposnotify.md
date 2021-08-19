---
title: TBM_SETPOSNOTIFY (Commctrl.h)
description: 'TBM_SETPOSNOTIFY Meldung: Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest.'
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY meldungssteuerelemente Windows
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
ms.openlocfilehash: 677ab818524614f89d16ae851376d8776a4ccca3ef7798d4ac90aa6d36962ca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046080"
---
# <a name="tbm_setposnotify-message"></a>TBM \_ SETPOSNOTIFY-Nachricht

Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

wParam wird nicht verwendet.

</dd> <dt>

*lParam* 
</dt> <dd>

Neue logische Position des Schiebereglers. Gültige logische Positionen sind die ganzzahligen Werte im Bereich von minimalen bis maximalen Schiebereglerpositionen der Trackleiste. Wenn dieser Wert außerhalb des maximalen und minimalen Bereichs des Steuerelements liegt, wird die Position auf den höchst- oder minimalen Wert festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Durch aufrufen von **TBM \_ SETPOSNOTIFY** wird die Position des Trackbar-Schiebereglers wie [**TBM \_ SETPOS**](tbm-setpos.md) festgelegt, aber es wird auch dazu führen, dass die Trackleiste das übergeordnete Element über eine [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) benachrichtigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





