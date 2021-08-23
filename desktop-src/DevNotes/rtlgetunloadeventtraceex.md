---
description: Ruft die Größe und den Speicherort der dynamisch entladenen Modulliste für den aktuellen Prozess ab.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: RtlGetUnloadEventTraceEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 35c4001851cc12701152f983c51a800d8f1846e015f5cf4d967c6371d9807578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571360"
---
# <a name="rtlgetunloadeventtraceex-function"></a>RtlGetUnloadEventTraceEx-Funktion

Ruft die Größe und den Speicherort der dynamisch entladenen Modulliste für den aktuellen Prozess ab.

## <a name="syntax"></a>Syntax


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ElementSize* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe eines Elements in der Liste enthält.

</dd> <dt>

*ElementCount* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der Elemente in der Liste enthält.

</dd> <dt>

*EventTrace* \[ out\]
</dt> <dd>

Ein Zeiger auf ein Array von **RTL \_ UNLOAD EVENT \_ \_ TRACE-Strukturen.** Weitere Informationen finden Sie in den Hinweisen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Das Lader speichert entladene Ereignisinformationen an Speicherorten, die prozessübergreifend gelesen werden können, indem es die Tatsache nutzt, dass Ntdll.dll in allen Prozessen an derselben Basisadresse geladen wird. Wenn ein Debugger entladene Modulinformationen abfragen muss, ruft er diese Funktion auf, um die Adresse zu bestimmen, unter der sich die Variablen befinden, und fragt dann den virtuellen Arbeitsspeicher im Zielprozess an diesen Adressen ab, um die tatsächlichen Werte zu lesen.

Jedes Element in der Liste wird wie folgt definiert.

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

Dieser Funktion ist keine Headerdatei zugeordnet. Die zugeordnete Importbibliothek Ntdll.lib ist im Windows Driver Kit (WDK) verfügbar. Sie können diese Funktion auch mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
