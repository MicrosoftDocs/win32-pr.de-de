---
title: TBM_SETPAGESIZE Meldung (Commctrl.h)
description: Legt die Anzahl der logischen Positionen fest, die der Schieberegler der Trackleiste als Reaktion auf Tastatureingaben wie die Tasten oder oder Mauseingaben bewegt, z. B. Klicks im Kanal der Trackleiste.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- TBM_SETPAGESIZE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TBM_SETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87cf41547a996e9726002101998ea859b7dbc6cc3e7ed3f87927fdae8bdadd2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046100"
---
# <a name="tbm_setpagesize-message"></a>TBM \_ SETPAGESIZE-Meldung

Legt die Anzahl der logischen Positionen fest, die der Schieberegler der Trackleiste als Reaktion auf Tastatureingaben wie die Tasten oder oder Mauseingaben bewegt, z. B. Klicks im Kanal der Trackleiste. Die logischen Positionen sind die ganzzahligen Inkremente im Bereich der Trackleiste von minimalen bis maximalen Schiebereglerpositionen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>

Neue Seitengröße.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der die vorherige Seitengröße angibt.

## <a name="remarks"></a>Hinweise

Die Trackleiste sendet auch eine [**WM \_ HSCROLL-**](wm-hscroll.md) oder [**WM \_ VSCROLL-Nachricht**](wm-vscroll.md) mit den TB \_ PAGEUP- und TB \_ PAGEDOWN-Benachrichtigungscodes an das übergeordnete Fenster, wenn sie Tastatur- oder Mauseingaben empfängt, die auf der Seite scrollen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TBM \_ GETPAGESIZE**](tbm-getpagesize.md)
</dt> </dl>

 

 





