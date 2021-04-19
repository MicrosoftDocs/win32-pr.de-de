---
description: Die TAPI-Telefon \_ Erstellungs Nachricht wird gesendet, um Anwendungen über das Erstellen eines neuen Telefon Geräts zu informieren.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: PHONE_CREATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c92dfaad5d4007279f18890021f5cb39c22c4da9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370979"
---
# <a name="phone_create-message"></a>Meldung zum Erstellen des Telefons \_

Die TAPI **- \_ Telefon** Erstellungs Nachricht wird gesendet, um Anwendungen über das Erstellen eines neuen Telefon Geräts zu informieren.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hphone* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Die *HDE viceid* des neu erstellten Geräts.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Anwendungen, die die API-Version 1,3 ausgehandelt haben, erhalten eine [**Telefon \_ Zustands**](phone-state.md) Meldung, die phonestate \_ REIT angibt. Dies erfordert, dass Sie Ihre Verwendung der API Herunterfahren und [**phoneinitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) erneut aufrufen, um die neue Anzahl von Geräten zu erhalten. Die TAPI-Version 1,4 und höher erfordert jedoch nicht, dass alle Anwendungen heruntergefahren werden, bevor die erneute Initialisierung von Anwendungen zugelassen wird. die erneute Initialisierung kann sofort erfolgen, wenn ein neues Gerät erstellt wird.

Anwendungen, die TAPI-Version 1,4 oder höher unterstützen, erhalten eine Meldung zum **\_ Erstellen eines Telefons** . Dadurch werden Sie darüber informiert, dass das neue Gerät und die neue Gerätekennung vorhanden sind. Die Anwendung kann dann auswählen, ob versucht werden soll, mit dem neuen Gerät zu arbeiten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Telefon \_ Status**](phone-state.md)
</dt> <dt>

[**phoneinitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneinitializeex**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




