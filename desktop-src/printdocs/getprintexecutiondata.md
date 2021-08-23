---
description: GetPrintExecutionData ruft den aktuellen Druckkontext ab.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: GetPrintExecutionData-Funktion (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: 0bbe08e82fb8f753d6e4fd23776618cb5f555b390434fdd0feddd231aaebc635
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971349"
---
# <a name="getprintexecutiondata-function"></a>GetPrintExecutionData-Funktion

**GetPrintExecutionData** ruft den aktuellen Druckkontext ab.

> [!Note]  
> Diese Funktion ist für die Verwendung durch Druckertreiber vorgesehen, die im Kontext des Druckspoolers ausgeführt werden.

 

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Adresse der [**PRINT \_ EXECUTION \_ DATA-Struktur**](print-execution-data.md) empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, wenn die Funktion erfolgreich ausgeführt wird. andernfalls **FALSE**. Wenn der Rückgabewert **FALSE** ist, rufen [**Sie GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um den Fehlerstatus abzurufen.

## <a name="remarks"></a>Hinweise

Druckertreiber sollten [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) für das Modul winspool.drv aufrufen, um die Adresse der **GetPrintExecutionData-Funktion** abzurufen, da **GetPrintExecutionData** auf Windows Vista oder früheren Versionen von Windows nicht unterstützt wird.

**GetPrintExecutionData** schlägt nur fehl, wenn der Wert von *pData* **NULL** ist.

Der Wert des **clientAppPID-Members** von [**PRINT EXECUTION \_ \_ DATA**](print-execution-data.md) ist nur dann sinnvoll, wenn der Wert des **Kontexts** **PRINT EXECUTION CONTEXT \_ \_ \_ WOW64** lautet. Wenn der Wert von **context** nicht **PRINT EXECUTION CONTEXT \_ \_ \_ WOW64** ist, ist der Wert von **clientAppPID** 0.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getlasterror**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**\_ \_ DRUCKAUSFÜHRUNGSKONTEXT**](print-execution-context.md)
</dt> <dt>

[**\_ \_ DRUCKAUSFÜHRUNGSDATEN**](print-execution-data.md)
</dt> </dl>

 

