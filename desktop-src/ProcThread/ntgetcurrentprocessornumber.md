---
description: Ruft die Nummer des Prozessors ab, auf dem der aktuelle Thread während des Aufrufens dieser Funktion ausgeführt wurde.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: Ntgetcurrentprocessornumber-Funktion
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
ms.openlocfilehash: 96862836d3f9c16034ce1c2e751aebea2884d114
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370790"
---
# <a name="ntgetcurrentprocessornumber-function"></a>Ntgetcurrentprocessornumber-Funktion

\[**Ntgetcurrentprocessornumber** kann geändert werden oder ist in zukünftigen Versionen von Windows nicht verfügbar. Anwendungen sollten stattdessen die [**getcurrentprocessornumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) -Funktion verwenden.\]

Ruft die Nummer des Prozessors ab, auf dem der aktuelle Thread während des Aufrufens dieser Funktion ausgeführt wurde.

## <a name="syntax"></a>Syntax


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt die aktuelle Prozessornummer zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion dient zum Bereitstellen von Informationen zum Schätzen der Prozessleistung.

Diese Funktion verfügt über keine zugeordnete Import Bibliothek. Sie müssen die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.

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

 

 
