---
title: TBM_GETTICPOS (Commctrl.h)
description: Ruft die aktuelle physische Position eines Teilstrichs in einer Trackleiste ab.
ms.assetid: a4b0ec32-ef4e-4607-ade1-5e2be02bebe4
keywords:
- TBM_GETTICPOS meldungssteuerelemente Windows
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
ms.openlocfilehash: 56d191034fc1551d4ffc1840498e352e2f3cd82985f1bbc5a7ae8d5350a41fb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046340"
---
# <a name="tbm_getticpos-message"></a>TBM \_ GETTICPOS-Nachricht

Ruft die aktuelle physische Position eines Teilstrichs in einer Trackleiste ab.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Nullbasierter Index, der ein Teilstrich identifiziert. Die Positionen der ersten und letzten Teilstriche sind nicht direkt über diese Nachricht verfügbar.

</dd> <dt>

*lParam* 
</dt> <dd>

Muss Null sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt den Abstand in Clientkoordinaten vom linken oder oberen Bereich des Clientbereichs der Trackleiste bis zum angegebenen Teilstrich zurück. Der Rückgabewert ist die x-Koordinate des Teilstrichs für eine horizontale Trackleiste oder die y-Koordinate für eine vertikale Trackbar. Wenn *wParam* kein gültiger Index ist, ist der Rückgabewert -1.

## <a name="remarks"></a>Hinweise

Da die ersten und letzten Teilstriche durch diese Meldung nicht verfügbar sind, werden gültige Indizes von ihrer Teilstrichposition auf der Trackleiste versetzt. Wenn der Unterschied [**zwischen TBM \_ GETRANGEMIN**](tbm-getrangemin.md) und [**TBM \_ GETRANGEMAX**](tbm-getrangemax.md) kleiner als zwei ist, gibt es keinen gültigen Index, und diese Meldung wird fehlschlagen.

Im Folgenden wird die Beziehung zwischen den Ticks auf einer Trackbar, den durch diese Nachricht verfügbaren Ticks und ihren nullbasierten Indizes veranschaulicht.

``` syntax
0 1 2 3 4 5 6 7 8 9    // Tick positions seen on the trackbar.
  1 2 3 4 5 6 7 8      // Tick positions whose position can be identified.
  0 1 2 3 4 5 6 7      // Index numbers for the identifiable positions.
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





