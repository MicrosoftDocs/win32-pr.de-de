---
title: Wsdumpmemory-Funktion (webservicesdebug. h)
description: Diese Funktion sichert alle Speicher Belegungen in der Konsole.
ms.assetid: 84a4f1e7-7d62-48c2-a8a3-ee4573bde5e4
keywords:
- Wsdumpmemory-funktionsweb Dienste für Windows
topic_type:
- apiref
api_name:
- WsDumpMemory
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70af8d34b3ee04a9db4128ce1063bd31e81306eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956942"
---
# <a name="wsdumpmemory-function"></a>Wsdumpmemory-Funktion

Diese Funktion sichert alle Speicher Belegungen in der Konsole.

> [!Note]  
> Diese Funktion dient nur zum Debuggen.

 

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI  WsDumpMemory(
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Fehler* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf ein [WS- \_ Fehler](ws-error.md) Objekt, in dem zusätzliche Informationen über den Fehler gespeichert werden sollen, wenn die Funktion fehlschlägt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ -Desktop-Apps \| UWP-apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Webservicesdebug. h</dt> </dl> |



 

 





