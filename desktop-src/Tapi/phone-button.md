---
description: Die TAPI PHONE \_ BUTTON-Nachricht wird gesendet, um die Anwendung darüber zu informieren, dass die Überwachung des Tastendrucks aktiviert ist, wenn ein Tastendruck auf dem lokalen Telefon erkannt wurde.
ms.assetid: fe47eed7-89d1-488b-b945-9e1aedc1f63c
title: PHONE_BUTTON Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aec64f754725e5926a8cab1d98b25e4cb379a444bf4208d6e8f3e976dafee82f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073000"
---
# <a name="phone_button-message"></a>\_PHONE BUTTON-Nachricht

Die TAPI **PHONE \_ BUTTON-Nachricht** wird gesendet, um die Anwendung darüber zu informieren, dass die Überwachung des Tastendrucks aktiviert ist, wenn ein Tastendruck auf dem lokalen Telefon erkannt wurde.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPhone* 
</dt> <dd>

Ein Handle für das Telefongerät.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Die Rückrufinstanz der Anwendung, die beim Öffnen des Telefongeräts bereitgestellt wird.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Bezeichner der Schaltfläche/Lampe, die gedrückt wurde. Beachten Sie, dass die Schaltflächenbezeichner 0 bis 11 immer die TASTENPAD-Schaltflächen sind, wobei "0" der Schaltflächenbezeichner 0( 0), "1" der Schaltflächenbezeichner 1 (usw. bis Schaltflächenbezeichner 9) und \* "" der Schaltflächenbezeichner 10 und \# "" der Schaltflächenbezeichner 11 sind. Zusätzliche Informationen zu einem Schaltflächenbezeichner sind mit [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) und [**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)verfügbar.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Der Schaltflächenmodus der Schaltfläche. Dieser Parameter verwendet eine der [**PHONEBUTTONMODE-Konstanten. \_**](phonebuttonmode--constants.md)

</dd> <dt>

*dwParam3* 
</dt> <dd>

Gibt an, ob es sich hierbei um ein Button-Down-Ereignis oder ein Button-up-Ereignis handelt. Dieser Parameter verwendet eine der [**PHONEBUTTONSTATE-Konstanten. \_**](phonebuttonstate--constants.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Wenn sich der Zustand einer Schaltfläche ändert, wird eine **PHONE \_ BUTTON-Nachricht** gesendet. Für eine Anwendung wird garantiert, dass für jedes Schaltflächen-Down-Ereignis schließlich ein entsprechendes Schaltflächen-Up-Ereignis gesendet wird. Ein Dienstanbieter, der nicht in der Lage ist, die tatsächliche Schaltfläche nach oben zu erkennen, ist erforderlich, um die Schaltflächen-up-Nachricht kurz nach der Schaltflächen-Down-Nachricht für jeden Schaltflächen-Klick zu generieren.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**phoneGetButtonInfo**](/windows/desktop/api/Tapi/nf-tapi-phonegetbuttoninfo)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> </dl>

 

 




