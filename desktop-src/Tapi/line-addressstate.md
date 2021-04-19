---
description: Die Statusmeldung der TAPI-Zeile \_ wird gesendet, wenn sich der Status einer Adresse in einer Zeile ändert, die zurzeit von der Anwendung geöffnet ist. Die Anwendung kann linegetaddressstatus aufrufen, um den aktuellen Status der Adresse zu bestimmen.
ms.assetid: af211fa1-79f8-49ac-a1d8-b62981f50519
title: LINE_ADDRESSSTATE Meldung (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d85b42f6957487ff24706485bd09d1d47880fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359312"
---
# <a name="line_addressstate-message"></a>Zeile \_ addressstate-Meldung

Die Statusmeldung der TAPI- **Zeile \_** wird gesendet, wenn sich der Status einer Adresse in einer Zeile ändert, die zurzeit von der Anwendung geöffnet ist. Die Anwendung kann [**linegetaddressstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus) aufrufen, um den aktuellen Status der Adresse zu bestimmen.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdevice* 
</dt> <dd>

Ein Handle für das liniengerät.

</dd> <dt>

*dwcallbackinstance* 
</dt> <dd>

Die beim Öffnen der Zeile angegebene Rückruf Instanz.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Der Adress Bezeichner der Adresse, die den Status geändert hat.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Der Adress Zustand, der geändert wurde. Kann eine oder mehrere der [**lineaddressstate- \_ Konstanten**](lineaddressstate--constants.md)sein.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Die **Zeile \_ addressstate** wird an jede Anwendung gesendet, die das Zeilen Gerät geöffnet hat und die diese Meldung aktiviert hat. Das Senden dieser Nachricht für die verschiedenen Status Elemente kann mithilfe von [**linegetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages) und [**linesetstatusmessages**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)gesteuert und abgefragt werden. Standardmäßig ist die Adress Status Berichterstattung deaktiviert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Lineaddresscaps**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**linegetaddresscaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**linegetaddressstatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**linegetstatus Messages**](/windows/desktop/api/Tapi/nf-tapi-linegetstatusmessages)
</dt> <dt>

[**linesetstatus-Meldungen**](/windows/desktop/api/Tapi/nf-tapi-linesetstatusmessages)
</dt> </dl>

 

 




