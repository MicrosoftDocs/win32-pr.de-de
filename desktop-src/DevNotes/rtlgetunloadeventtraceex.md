---
description: Ruft die Größe und den Speicherort der Liste der dynamisch entladenen Module für den aktuellen Prozess ab.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: Rtlgetunloadeventtraceex-Funktion
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
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367730"
---
# <a name="rtlgetunloadeventtraceex-function"></a>Rtlgetunloadeventtraceex-Funktion

Ruft die Größe und den Speicherort der Liste der dynamisch entladenen Module für den aktuellen Prozess ab.

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

*Element Size* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe eines Elements in der Liste enthält.

</dd> <dt>

*Element count* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Anzahl der Elemente in der Liste enthält.

</dd> <dt>

*EventTrace* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von **RTL- \_ Entlade \_ Ereignis \_** -Ablauf Verfolgungs Strukturen. Weitere Informationen finden Sie in den Hinweisen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das Lade Modul speichert Informationen zu entladenen Ereignissen an Standorten, die über Prozesse hinweg gelesen werden können, indem die Tatsache genutzt wird, dass Ntdll.dll an derselben Basisadresse in allen Prozessen geladen wird. Wenn ein Debugger Informationen zu entladenen Modulen Abfragen muss, wird diese Funktion aufgerufen, um die Adresse zu bestimmen, in der sich die Variablen befinden. Anschließend wird der virtuelle Arbeitsspeicher im Ziel Prozess an diesen Adressen abgefragt, um die tatsächlichen Werte zu lesen.

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

Dieser Funktion ist keine Header Datei zugeordnet. Die zugehörige Import Bibliothek ntdll. lib ist im Windows-Treiberkit (WDK) verfügbar. Sie können diese Funktion auch mit der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
