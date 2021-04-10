---
title: TBM_SETPAGESIZE Meldung (kommstrg. h)
description: Legt die Anzahl der logischen Positionen fest, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben bewegt, wie z. b. die-Taste oder die-Taste oder Maus Eingaben, z. b. Klicks im Kanal der Trackleiste.
ms.assetid: 34edb868-4b6b-4b3f-b315-3ce39346b134
keywords:
- Windows-Steuerelemente für TBM_SETPAGESIZE Meldung
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
ms.openlocfilehash: ec5d8a396bb605b4276346e84e7b46bfbefe0657
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040838"
---
# <a name="tbm_setpagesize-message"></a>TBM- \_ setPageSize-Meldung

Legt die Anzahl der logischen Positionen fest, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben bewegt, wie z. b. die-Taste oder die-Taste oder Maus Eingaben, z. b. Klicks im Kanal der Trackleiste. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.

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

## <a name="remarks"></a>Bemerkungen

Die TrackBar sendet außerdem eine [**WM- \_ HScroll**](wm-hscroll.md) -oder [**WM- \_ VScroll**](wm-vscroll.md) -Nachricht mit den e \_ -v-Nachrichten-und TB- \_ PageDown-Benachrichtigungs Codes an das übergeordnete Fenster, wenn Sie Tastatur-oder Maus Eingaben empfängt, die die Seite

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TBM \_ getpagesize**](tbm-getpagesize.md)
</dt> </dl>

 

 





