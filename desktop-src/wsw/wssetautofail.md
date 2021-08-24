---
title: WsSetAutoFail-Funktion (WebServicesDebug.h)
description: Legt den nächsten Punkt fest, an dem ein Fehler einzufügen ist. Dies ist eine DEBUG ONLY-Funktion.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Webdienste der WsSetAutoFail-Funktion für Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e2ae3ed731edce429aac78700d52d0e7504a5688d1bf35bbb9c64a5d34bc0a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119838540"
---
# <a name="wssetautofail-function"></a>WsSetAutoFail-Funktion

Legt den nächsten Punkt fest, an dem ein Fehler einzufügen ist. Dies ist eine DEBUG ONLY-Funktion.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*count* \[ In\]
</dt> <dd>

Gibt an, wie viele Vorgänge auftreten, bevor Fehler auftreten.

</dd> <dt>

*Error (Fehler)* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf ein [WS \_ ERROR-Objekt,](ws-error.md) in dem zusätzliche Informationen zum Fehler gespeichert werden sollen, wenn die Funktion fehlschlägt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>WebServicesDebug.h</dt> </dl> |



 

 





