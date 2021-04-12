---
title: TBM_GETPAGESIZE Meldung (kommstrg. h)
description: Ruft die Anzahl logischer Positionen ab, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben bewegt, z. b. die-Taste oder die-Taste, oder Maus Eingaben, z. b. Klicks im Kanal der Trackleiste.
ms.assetid: f0c5feac-2723-440e-96c0-dac37b0531ed
keywords:
- Windows-Steuerelemente für TBM_GETPAGESIZE Meldung
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
ms.openlocfilehash: ac58c0b935b468cf8af565fba2db67c88418ee4f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103755"
---
# <a name="tbm_getpagesize-message"></a>TBM- \_ getpagesize-Meldung

Ruft die Anzahl logischer Positionen ab, die der Schieberegler der TrackBar als Reaktion auf Tastatureingaben bewegt, z. b. die-Taste oder die-Taste, oder Maus Eingaben, z. b. Klicks im Kanal der Trackleiste. Bei den logischen Positionen handelt es sich um die ganzzahligen Inkremente in der TrackBar im Bereich der minimalen bis zum maximalen Schieberegler.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>Muss Null sein.</dd> <dt>

*lParam* 
</dt> <dd>Muss Null sein.</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen 32-Bit-Wert zurück, der die Seitengröße für die TrackBar angibt.

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

[**TBM \_ setPageSize**](tbm-setpagesize.md)
</dt> </dl>

 

 





