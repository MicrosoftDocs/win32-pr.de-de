---
title: TBM_GETPAGESIZE-Nachricht (Commctrl.h)
description: Ruft die Anzahl der logischen Positionen ab, die der Schieberegler der Trackleiste als Reaktion auf Tastatureingaben wie die Tasten oder die Mauseingabe bewegt, z. B. Klicks im Kanal der Trackleiste.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- TBM_GETPAGESIZE Windows-Steuerelemente für Nachrichten
topic_type:
- apiref
api_name:
- TBM_GETPAGESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1aa3ef3412fd00c18972b62d4d868ff1dbc97cb4787693b3746281b4884706e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046500"
---
# <a name="tbm_getpagesize-message"></a>TBM \_ GETPAGESIZE-Nachricht

Ruft die Anzahl der logischen Positionen ab, die der Schieberegler der Trackleiste als Reaktion auf Tastatureingaben wie die Tasten oder die Mauseingabe bewegt, z. B. Klicks im Kanal der Trackleiste. Die logischen Positionen sind die ganzzahligen Inkremente im Bereich der Trackleiste von minimalen bis maximalen Schiebereglerpositionen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der die Seitengröße für die Trackleiste angibt.

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

[**TBM \_ SETPAGESIZE**](tbm-setpagesize.md)
</dt> </dl>

 

 





