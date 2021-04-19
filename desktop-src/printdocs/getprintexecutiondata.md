---
description: Getprintexecutiondata Ruft den aktuellen Druck Kontext ab.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Getprintexecutiondata-Funktion (winspool. h)
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
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373330"
---
# <a name="getprintexecutiondata-function"></a>Getprintexecutiondata-Funktion

**Getprintexecutiondata** Ruft den aktuellen Druck Kontext ab.

> [!Note]  
> Diese Funktion ist für die Verwendung durch Druckertreiber vorgesehen, die im Kontext des Druck Spoolers ausgeführt werden.

 

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Adresse der [**Druck \_ Ausführungs \_ Daten**](print-execution-data.md) -Struktur empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die Funktion erfolgreich ausgeführt wurde. andernfalls **false**. Wenn der Rückgabewert **false** ist, können Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen, um den Fehlerstatus abzurufen.

## <a name="remarks"></a>Bemerkungen

Druckertreiber sollten [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) für das winspool. drv-Modul aufrufen, um die Adresse der **getprintexecutiondata** -Funktion abzurufen, da **getprintexecutiondata** unter Windows Vista oder früheren Versionen von Windows nicht unterstützt wird.

**Getprintexecutiondata** schlägt nur fehl, wenn der Wert von *pData* **null** ist.

Der Wert des **clientapppid** -Members der [**Druck \_ Ausführungs \_ Daten**](print-execution-data.md) ist nur sinnvoll, wenn der Wert des **Kontexts** " **Druck \_ Ausführungs \_ Kontext \_ WOW64**" ist. Wenn der Wert des **Kontexts** nicht der **Druck \_ Ausführungs \_ Kontext \_ WOW64** ist, ist der Wert von **clientapppid** 0.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**Druck \_ Ausführungs \_ Kontext**](print-execution-context.md)
</dt> <dt>

[**\_Ausführungs \_ Daten drucken**](print-execution-data.md)
</dt> </dl>

 

