---
description: Ruft die Anzahl des Prozessors ab, auf dem der aktuelle Thread während des Aufrufs dieser Funktion ausgeführt wurde.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: NtGetCurrentProcessorNumber-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: f45ee39e9599e2d77d77131eb64c2a9037de1f4ba31f907ac5c9ea562a706c27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032190"
---
# <a name="ntgetcurrentprocessornumber-function"></a>NtGetCurrentProcessorNumber-Funktion

\[**NtGetCurrentProcessorNumber** kann in zukünftigen Versionen von Windows geändert oder nicht verfügbar sein. Anwendungen sollten stattdessen die [**GetCurrentProcessorNumber-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) verwenden.\]

Ruft die Anzahl des Prozessors ab, auf dem der aktuelle Thread während des Aufrufs dieser Funktion ausgeführt wurde.

## <a name="syntax"></a>Syntax


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt die aktuelle Prozessornummer zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion wird verwendet, um Informationen zum Schätzen der Prozessleistung bereitzustellen.

Dieser Funktion ist keine Importbibliothek zugeordnet. Sie müssen die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mehrere Prozessoren](multiple-processors.md)
</dt> <dt>

[Prozess- und Threadfunktionen](process-and-thread-functions.md)
</dt> <dt>

[Prozesse](child-processes.md)
</dt> </dl>

 

 
