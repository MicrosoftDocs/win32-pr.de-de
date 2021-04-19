---
description: TAPI sendet die Telefon \_ Zustands Meldung immer dann an eine Anwendung, wenn sich der Status eines Telefon Geräts ändert.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: PHONE_STATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367421"
---
# <a name="phone_state-message"></a>Telefon \_ Zustands Meldung

TAPI sendet die **Telefon \_ Zustands** Meldung immer dann an eine Anwendung, wenn sich der Status eines Telefon Geräts ändert.


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

Der Telefon Zustand, der geändert wurde. Dieser Parameter verwendet eine der [**phonestate- \_ Konstanten**](phonestate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Telefon Zustands abhängige Informationen, die die Statusänderung beschreiben. Dieser Parameter wird nicht verwendet, wenn mehrere Flags in *dwParam1* festgelegt sind, da sich mehrere Status Elemente geändert haben. Die Anwendung sollte [**phonegetstatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) aufrufen, um einen kompletten Satz von Informationen zu erhalten.

Wenn *dwParam1* der phonestate- \_ Besitzer ist, enthält *dwParam2* die neue Anzahl von Besitzern.

Wenn *dwParam1* phonestate \_ Monitors ist, enthält *dwParam2* die neue Anzahl von Monitoren.

Wenn *dwParam1* "phonestate \_ Lamp" ist, enthält *dwParam2* den Schaltflächen-/Lamp-Bezeichner der geänderten Lamp.

Wenn *dwParam1* phonestate \_ ringmode ist, enthält *dwParam2* den neuen Ring Modus.

Wenn *dwParam1* phonestate \_ Handset, Speaker oder Headset ist, enthält *dwParam2* den neuen Modus "huokswitch" dieses Gerät. Dieser Parameter verwendet eine der [**phonehuokswitchmode- \_ Konstanten**](phonehookswitchmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Das Senden der **Telefon \_ Zustands** Meldung an die Anwendung kann mithilfe von " [**phonesetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) " und " [**phonegetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)" gesteuert und abgefragt werden. Standardmäßig ist diese Meldung für alle Zustandsänderungen deaktiviert, mit Ausnahme von "phonestate \_ Reit", die nicht deaktiviert werden kann. Diese Nachricht wird an alle Anwendungen gesendet, die über ein Handle für das Telefon verfügen, einschließlich derjenigen, die [**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) aufgerufen haben, wobei der *dwprivileges* -Parameter auf phoneprivilege \_ Owner oder phoneprivilege Monitor festgelegt ist \_ .

Eine **Telefon \_ Zustands** Meldung mit einer Anzeige von Besitzern und/oder Monitoren wird an Anwendungen gesendet, die bereits über ein Handle für das Telefon verfügen. Dies kann das Ergebnis einer anderen Anwendung sein, die den Besitz oder die Überwachung des Telefon Geräts mit [**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneclose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) oder [**phoneshutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Telefon \_ Schließen**](phone-close.md)
</dt> <dt>

[**Phonecaps**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneclose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[**phonegetdevcaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[**phonegetstatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[**phonegetstatus Messages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[**phoneinitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**phoneopen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**phonesetstatus-Meldungen**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[**phoneshutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




