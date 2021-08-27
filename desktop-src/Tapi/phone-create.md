---
description: Die TAPI PHONE \_ CREATE-Nachricht wird gesendet, um Anwendungen über die Erstellung eines neuen Telefongeräts zu informieren.
ms.assetid: 62895b10-76ce-456e-ad02-e2b7764616a8
title: PHONE_CREATE Meldung (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18633ca9f3d45e08c3e2e054d51261dabe6494f42055567a5a68707408f94d5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072910"
---
# <a name="phone_create-message"></a>PHONE \_ CREATE-Nachricht

Die TAPI **PHONE \_ CREATE-Nachricht** wird gesendet, um Anwendungen über die Erstellung eines neuen Telefongeräts zu informieren.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hPhone* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Die *hDeviceID* des neu erstellten Geräts.

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

## <a name="remarks"></a>Hinweise

Anwendungen, die API-Version 1.3 ausgehandelt haben, erhalten eine [**PHONE \_ STATE-Nachricht,**](phone-state.md) die PHONESTATE REINIT angibt. Daher \_ müssen sie ihre Verwendung der API herunterfahren und [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize) erneut aufrufen, um die neue Anzahl von Geräten zu erhalten. Tapi Version 1.4 und höher erfordert jedoch nicht, dass alle Anwendungen heruntergefahren werden, bevor anwendungen erneut initialisiert werden können. Die erneute Initialisierung kann sofort erfolgen, wenn ein neues Gerät erstellt wird.

Anwendungen, die TAPI Version 1.4 oder höher unterstützen, erhalten eine **PHONE \_ CREATE-Nachricht.** Dies informiert sie über das Vorhandensein des neuen Geräts und seines neuen Gerätebezeichners. Die Anwendung kann dann auswählen, ob sie versucht, mit dem neuen Gerät am Arbeitsplatz zu arbeiten.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_TELEFONSTATUS**](phone-state.md)
</dt> <dt>

[**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> </dl>

 

 




