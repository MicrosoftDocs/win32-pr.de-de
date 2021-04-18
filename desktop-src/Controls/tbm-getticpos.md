---
title: TBM_GETTICPOS Meldung (kommstrg. h)
description: Ruft die aktuelle physische Position eines Teil Strichs in einer TrackBar ab.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- Windows-Steuerelemente für TBM_GETTICPOS Meldung
topic_type:
- apiref
api_name:
- TBM_GETTICPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb1346f63e9bb10b919c678373e0e8df0724861
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338544"
---
# <a name="tbm_getticpos-message"></a>TBM- \_ GetTicPos-Nachricht

Ruft die aktuelle physische Position eines Teil Strichs in einer TrackBar ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

NULL basierter Index, der einen Teil Strich identifiziert. Die Positionen des ersten und letzten Teil Strichs sind nicht direkt über diese Meldung verfügbar.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt die Entfernung in Client Koordinaten vom linken oder oberen Rand des Client Bereichs der TrackBar zum angegebenen Teil Strich zurück. Der Rückgabewert ist die x-Koordinate des Teil Strichs für eine horizontale Trackleiste oder die y-Koordinate für eine vertikale TrackBar. Wenn *wParam* kein gültiger Index ist, ist der Rückgabewert-1.

## <a name="remarks"></a>Bemerkungen

Da der erste und der letzte Teil Strich über diese Nachricht nicht verfügbar sind, werden gültige Indizes von der Tick-Position auf der TrackBar versetzt. Wenn der Unterschied zwischen [**TBM \_ getrangemin**](tbm-getrangemin.md) und [**TBM \_ getrangemax**](tbm-getrangemax.md) kleiner als zwei ist, gibt es keinen gültigen Index, und diese Meldung schlägt fehl.

Im folgenden Beispiel wird die Beziehung zwischen den Ticks auf einer TrackBar, den in dieser Meldung verfügbaren Ticks und ihren Null basierten Indizes veranschaulicht.

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





