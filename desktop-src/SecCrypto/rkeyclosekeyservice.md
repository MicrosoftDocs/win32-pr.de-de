---
description: Die rkeyclosekeyservice-Funktion wird nicht unterstützt.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Rkeyclosekeyservice-Funktion (rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862623"
---
# <a name="rkeyclosekeyservice-function"></a>Rkeyclosekeyservice-Funktion

Die **rkeyclosekeyservice** -Funktion wird nicht unterstützt.

**Windows Server 2003:** Die Funktion **rkeyclosekeyservice** schließt ein Schlüsseldienst handle, das durch einen vorherigen aufrufsbefehl der [**rkeyopenkeyservice**](rkeyopenkeyservice.md) -Funktion geöffnet wurde. Beachten Sie, dass sich dieses Verhalten in Windows Server 2003 mit Service Pack 1 (SP1) geändert hat.

## <a name="syntax"></a>Syntax


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hkeysvccli* \[ in\]
</dt> <dd>

Ein [**keysvcc \_ handle**](keysvcc-handle.md) -handle, das zuvor von [**rkeyopenkeyservice**](rkeyopenkeyservice.md)geöffnet wurde. Dieser Wert darf nicht **null** sein.

</dd> <dt>

*beibehalten* \[ in, out\]
</dt> <dd>

Reserviert. Legen Sie diesen Wert auf **null** fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein **ulong** -Wert, der den Fehler angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rkeyopenkeyservice**](rkeyopenkeyservice.md)
</dt> <dt>

[**Rkeypfxinstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




