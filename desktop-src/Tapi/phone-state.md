---
description: TAPI sendet die NACHRICHT PHONE \_ STATE an eine Anwendung, wenn sich der Status eines Telefongeräts ändert.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: PHONE_STATE Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90003eaa67cb3384b123c62827fcf52bae524b1e20f9f14c2391c46dc89a367c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796760"
---
# <a name="phone_state-message"></a>\_PHONE STATE-Nachricht

TAPI sendet die **NACHRICHT PHONE \_ STATE** an eine Anwendung, wenn sich der Status eines Telefongeräts ändert.


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

Der geänderte Telefonzustand. Dieser Parameter verwendet eine der [**\_ PHONESTATE-Konstanten.**](phonestate--constants.md)

</dd> <dt>

*dwParam2* 
</dt> <dd>

Telefon zustandsabhängige Informationen, die die Statusänderung detailliert beschreiben. Dieser Parameter wird nicht verwendet, wenn in *dwParam1* mehrere Flags festgelegt sind, da sich mehrere Statuselemente geändert haben. Die Anwendung sollte [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) aufrufen, um einen vollständigen Satz von Informationen abzurufen.

Wenn *dwParam1* PHONESTATE \_ OWNER ist, enthält *dwParam2* die neue Anzahl von Besitzern.

Wenn *dwParam1* PHONESTATE \_ MONITORS ist, enthält *dwParam2* die neue Anzahl von Monitoren.

Wenn *dwParam1* PHONESTATE \_ LAMP ist, enthält *dwParam2* die Schaltflächen-/Lampe-ID der geänderten Lampe.

Wenn *dwParam1* PHONESTATE \_ RINGMODE ist, enthält *dwParam2* den neuen Ringmodus.

Wenn *dwParam1* PHONESTATE \_ HANDSET, SPEAKER oder HEADSET ist, enthält *dwParam2* den neuen hookswitch-Modus dieses hookswitch-Geräts. Dieser Parameter verwendet eine der [**PHONEHOOKSWITCHMODE-Konstanten. \_**](phonehookswitchmode--constants.md)

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Das Senden der **PHONE \_ STATE-Nachricht** an die Anwendung kann mit [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) und [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)gesteuert und abgefragt werden. Standardmäßig ist diese Nachricht für alle Zustandsänderungen deaktiviert, mit Ausnahme von PHONESTATE \_ REINIT, die nicht deaktiviert werden können. Diese Nachricht wird an alle Anwendungen gesendet, die über ein Handle für das Telefon verfügen, einschließlich derjenigen, die [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) aufgerufen haben, wobei der *dwPrivileges-Parameter* auf PHONEPRIVILEGE \_ OWNER oder PHONEPRIVILEGE MONITOR festgelegt \_ ist.

Eine **PHONE \_ STATE-Nachricht** mit der Angabe Besitzer und/oder Monitore wird an Anwendungen gesendet, die bereits über ein Handle für das Telefon verfügen. Dies kann das Ergebnis einer anderen Anwendung sein, die den Besitz oder die Überwachung des Telefongeräts mit [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) oder [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)ändert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PHONE \_ CLOSE**](phone-close.md)
</dt> <dt>

[**PHONECAPS**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**phoneÖffnen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




