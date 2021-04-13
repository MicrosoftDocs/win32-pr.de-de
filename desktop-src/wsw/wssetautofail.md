---
title: Wssetautfail-Funktion (webservicesdebug. h)
description: Legt den nächsten Punkt für das Einfügen eines Fehlers fest. Dies ist eine reine Debugfunktion.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Wssetauwebfail-funktionsweb Dienste für Windows
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
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518539"
---
# <a name="wssetautofail-function"></a>Wssetauto Fail-Funktion

Legt den nächsten Punkt für das Einfügen eines Fehlers fest. Dies ist eine reine Debugfunktion.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Gibt an, wie viele Vorgänge vor dem Auftreten von Fehlern beginnen.

</dd> <dt>

*Fehler* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf ein [WS- \_ Fehler](ws-error.md) Objekt, in dem zusätzliche Informationen über den Fehler gespeichert werden sollen, wenn die Funktion fehlschlägt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Webservicesdebug. h</dt> </dl> |



 

 





