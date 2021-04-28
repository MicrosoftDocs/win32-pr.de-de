---
title: TBM_SETPOSNOTIFY Meldung (Commctrl.h)
description: 'TBM_SETPOSNOTIFY Meldung: Legt die aktuelle logische Position des Schiebereglers in einer Trackleiste fest.'
ms.assetid: 02f8899a-55b0-46ae-8642-9e534ab4abf5
keywords:
- TBM_SETPOSNOTIFY Meldung Windows-Steuerelemente
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
ms.openlocfilehash: 7201f3056ed05e6321ab9d9bd726edc3b4470f0b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104078"
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

Neue logische Position des Schiebereglers. Gültige logische Positionen sind die ganzzahligen Werte im Bereich der Trackleiste von minimalen bis maximalen Schiebereglerpositionen. Wenn dieser Wert außerhalb des maximalen und minimalen Bereichs des Steuerelements liegt, wird die Position auf den Maximal- oder Mindestwert festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Durch den Aufruf von **TBM \_ SETPOSNOTIFY** wird die Position des Trackbar-Schiebereglers wie [**bei TBM \_ SETPOS**](tbm-setpos.md) festgelegt. Dies bewirkt jedoch auch, dass die Trackleiste das übergeordnete Element über eine [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) über eine Verschiebung benachrichtigt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ 7-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ R2-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





