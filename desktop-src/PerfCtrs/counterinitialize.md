---
description: Registriert den Anbieter und initialisiert die Indikatorensätze.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: CounterInitialize-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterInitialize
api_type:
- NA
api_location: ''
ms.openlocfilehash: e7c2fb61b53ca1847eefcc453a91f69b3c0602e06277b4858b8f0b733be7f71b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517680"
---
# <a name="counterinitialize-function"></a>CounterInitialize-Funktion

Registriert den Anbieter und initialisiert die Indikatorensätze.

## <a name="syntax"></a>Syntax


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt ERROR \_ SUCCESS bei Erfolg zurück, andernfalls einen standardmäßigen Win32-Fehlercode.

## <a name="remarks"></a>Hinweise

Ihr Anbieter ruft diese Funktion auf. Die Funktion enthält Aufrufe der [**PerfStartProvider-Funktion**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) und der [**PerfSetCounterSetInfo-Funktion.**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo)

Das [**CTRPP-Tool**](ctrpp.md) generiert diese Inlinefunktion, wenn Sie das **Argument -o** angeben. Der Name der Funktion enthält eine *Präfixzeichenfolge,* wenn Sie das Argument **-prefix** angeben.

Wenn Sie die Argumente **-MemoryRoutines** oder **-NotificationCallback** angeben (oder das **Rückrufattribut** für das [**Anbieterelement**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) angeben), ändert sich die **CounterInitialize-Signatur** wie folgt:

``` syntax
ULONG WINAPI CounterInitialize(
    __in_opt PERFLIBREQUEST NotificationCallback,
    __in_opt PERF_MEM_ALLOC MemoryAllocationFunction,
    __in_opt PERF_MEM_FREE MemoryFreeFunction,
    __inout_opt PVOID MemoryFunctionContext
);
```

Erläuterungen:

<dl> <dt>

<span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>NotificationCallback
</dt> <dd>

Der Name ihrer [*ControlCallback-Rückruffunktion,*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) die Sie implementieren, um Benachrichtigungen über Consumeranforderungen zu erhalten (z. B. Anforderungen zum Hinzufügen oder Entfernen von Leistungsindikatoren aus der Abfrage). Legen Sie auf **NULL** fest, wenn Sie die *ControlCallback-Rückruffunktion* nicht implementieren.

</dd> <dt>

<span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>MemoryAllocationFunction
</dt> <dd>

Der Name Ihrer [*AllocateMemory-Rückruffunktion,*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) die PERFLIB aufruft, um Arbeitsspeicher zu belegen. Legen Sie auf **NULL** fest, wenn Sie das **Argument -MemoryRoutines** nicht angegeben haben.

</dd> <dt>

<span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>MemoryFreeFunction
</dt> <dd>

Der Name Ihrer [*FreeMemory-Rückruffunktion,*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) die PERFLIB aufruft, um den mit der [*AllocateMemory-Funktion*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) belegten Arbeitsspeicher freizugeben. Wird auf **NULL** festgelegt, wenn *MemoryAllocationFunction* **NULL** ist.

</dd> <dt>

<span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>MemoryFunctionContext
</dt> <dd>

Kontextinformationen, die an Ihre Speicherbelegungs- und freien Routinen übergeben werden sollen. Kann **NULL** sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



 

