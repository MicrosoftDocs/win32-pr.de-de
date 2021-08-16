---
description: Die RKeyCloseKeyService-Funktion wird nicht unterstützt.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: RKeyCloseKeyService-Funktion (Rkeysvcc.h)
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
ms.openlocfilehash: 5c7a075cf4869e350d90e278d009098cf4716d6518b1970c15b8b8264c93cd22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900555"
---
# <a name="rkeyclosekeyservice-function"></a>RKeyCloseKeyService-Funktion

Die **RKeyCloseKeyService-Funktion** wird nicht unterstützt.

**Windows Server 2003:** Die **Funktion RKeyCloseKeyService** schließt ein Schlüsseldiensthand handle, das durch einen vorherigen Aufruf der [**RKeyOpenKeyService-Funktion geöffnet**](rkeyopenkeyservice.md) wurde. Beachten Sie, dass sich dieses Verhalten mit Windows Server 2003 mit Service Pack 1 (SP1) geändert hat.

## <a name="syntax"></a>Syntax


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hKeySvcCli* \[ In\]
</dt> <dd>

Ein [**KEYSVCC \_ HANDLE-Handle,**](keysvcc-handle.md) das zuvor von [**RKeyOpenKeyService geöffnet wurde.**](rkeyopenkeyservice.md) Dieser Wert darf nicht **NULL sein.**

</dd> <dt>

*pReserved* \[ in, out\]
</dt> <dd>

Reserviert. Legen Sie diesen Wert auf **NULL fest.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert S \_ OK.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein **ULONG-Wert,** der den Fehler angibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> </dl>

 

 




