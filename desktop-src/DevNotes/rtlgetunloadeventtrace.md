---
description: Ermöglicht dem dumpcode, die entladenen Modul Informationen aus Ntdll.dll für den Speicher im Minidump zu erhalten.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: Rtlgetunloadeventtrace-Funktion
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
ms.openlocfilehash: 9297ba0019c89c5e93961d4b36e0fe16da04d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362037"
---
# <a name="rtlgetunloadeventtrace-function"></a>Rtlgetunloadeventtrace-Funktion

\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]

Ermöglicht dem dumpcode, die entladenen Modul Informationen aus Ntdll.dll für den Speicher im Minidump zu erhalten.

## <a name="syntax"></a>Syntax


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt einen Zeiger auf ein Array zurück. Weitere Informationen finden Sie in den Hinweisen.

## <a name="remarks"></a>Bemerkungen

Das rtlpunloadeventtrace-Array wird wie folgt definiert:

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

Dieser Funktion ist keine Header Datei zugeordnet. Die zugehörige Import Bibliothek ntdll. lib ist im Windows-Treiberkit (WDK) verfügbar. Sie können diese Funktion auch mit der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
