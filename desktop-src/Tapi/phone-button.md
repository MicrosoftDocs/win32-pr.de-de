---
description: Die Meldung für die TAPI-Telefon \_ Schaltfläche wird gesendet, um der Anwendung mitzuteilen, dass die Schaltfläche zum Drücken der Schaltfläche aktiviert ist, wenn auf dem lokalen Telefon ein Schaltflächen-
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: PHONE_BUTTON Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da810630a937f8415e070373f359dca06a694e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368478"
---
# <a name="phone_button-message"></a>Telefon \_ Schaltfläche Meldung

Die Meldung für die TAPI- **Telefon \_ Schaltfläche** wird gesendet, um der Anwendung mitzuteilen, dass die Schaltfläche zum Drücken der Schaltfläche aktiviert ist, wenn auf dem lokalen Telefon ein Schaltflächen-


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hphone* 
</dt> <dd>

Ein Handle für das Telefongerät.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die Rückruf Instanz der Anwendung, die beim Öffnen des Telefon Geräts bereitgestellt wird.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Schaltflächen-/Lamp-Bezeichner der Schaltfläche, die gedrückt wurde. Beachten Sie, dass die Schaltflächen Bezeichner 0 (null) bis 11 immer die Keypad-Schaltflächen sind, wobei "0" den Schaltflächen Bezeichner 0 (null), "1" als Schaltflächen Bezeichner 1 (usw. bis Schaltflächen Bezeichner 9) und "" als Schaltflächen Bezeichner \* \# 11 hat. Weitere Informationen zu einem Schaltflächen Bezeichner sind mit [**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) und [**phonegetbuttoninfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)verfügbar.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Der Schaltflächen Modus der Schaltfläche. Dieser Parameter verwendet eine der [**phonebuttonmode- \_ Konstanten**](phonebuttonmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Gibt an, ob es sich um ein Button-down-Ereignis oder ein Schaltflächen-up-Ereignis handelt. Dieser Parameter verwendet eine der [**phonebuttonstate- \_ Konstanten**](phonebuttonstate--constants.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Wenn sich der Zustand einer Schaltfläche ändert, wird eine **Telefon \_ Schaltfläche** angezeigt. Eine Anwendung ist garantiert, dass Sie für jedes Schaltflächen-nach-unten-Ereignis ein entsprechendes Schaltflächen-up-Ereignis sendet. Ein Dienstanbieter, der nicht in der Lage ist, die tatsächliche Schaltfläche nach oben zu erkennen, ist erforderlich, um die Schaltfläche nach oben zu generieren, die für jede Schaltfläche gedrückt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**phonegetbuttoninfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




