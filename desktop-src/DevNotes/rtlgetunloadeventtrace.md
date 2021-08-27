---
description: Ermöglicht es dem Dumpcode, die entladenen Modulinformationen aus Ntdll.dll für die Speicherung im Minidump zu erhalten.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: RtlGetUnloadEventTrace-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d8575610ab34b62c9228f87fa64fbd6a40fa0201b7fe1a70ab95c7daae706854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058590"
---
# <a name="rtlgetunloadeventtrace-function"></a>RtlGetUnloadEventTrace-Funktion

\[Diese Funktion kann ohne weitere Ankündigung geändert oder Windows entfernt werden.\]

Ermöglicht es dem Dumpcode, die entladenen Modulinformationen aus Ntdll.dll für die Speicherung im Minidump zu erhalten.

## <a name="syntax"></a>Syntax


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen Zeiger auf ein Array zurück. Weitere Informationen finden Sie in den Hinweisen.

## <a name="remarks"></a>Hinweise

Das RtlpUnloadEventTrace-Array ist wie folgt definiert:

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

Dieser Funktion ist keine Headerdatei zugeordnet. Die zugeordnete Importbibliothek Ntdll.lib ist im Windows Driver Kit (WDK) verfügbar. Sie können diese Funktion auch mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
