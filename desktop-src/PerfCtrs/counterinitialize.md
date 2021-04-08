---
description: Registriert den Anbieter und initialisiert die Indikatorensätze.
ms.assetid: edcf8df3-0f6d-4849-b41d-270509499b8e
title: Counterinitialize-Funktion
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
ms.openlocfilehash: 18996fc4349a120069a9b38293a11faf70632033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959769"
---
# <a name="counterinitialize-function"></a>Counterinitialize-Funktion

Registriert den Anbieter und initialisiert die Indikatorensätze.

## <a name="syntax"></a>Syntax


```C++
ULONG WINAPI CounterInitialize(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt \_ bei Erfolg einen Erfolg des Fehlers zurück, andernfalls einen Standard-Win32-Fehlercode.

## <a name="remarks"></a>Bemerkungen

Der Anbieter ruft diese Funktion auf. Die Funktion enthält Aufrufe der Funktion [**perfstartprovider**](/windows/desktop/api/Perflib/nf-perflib-perfstartprovider) und der Funktion [**perfsetcountersetinfo**](/windows/desktop/api/Perflib/nf-perflib-perfsetcountersetinfo) .

Das [**ctrpp**](ctrpp.md) -Tool generiert diese Inline Funktion, wenn Sie das **-o-** Argument angeben. Der Name der Funktion enthält eine *Präfix* Zeichenfolge, wenn Sie das **-prefix-** Argument angeben.

Wenn Sie die Argumente **-memoryroutinen** oder **-notificationcallback** angeben (oder das **Rückruf** Attribut für das [**Provider**](/windows/desktop/PerfCtrs/performance-counters-provider--counters--element) -Element angeben), ändert sich die **counterinitialize** -Signatur wie folgt:

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

<span id="NotificationCallback"></span><span id="notificationcallback"></span><span id="NOTIFICATIONCALLBACK"></span>Notificationcallback
</dt> <dd>

Der Name der [*controlcallback*](/windows/desktop/api/Perflib/nc-perflib-perflibrequest) -Rückruffunktion, die Sie implementieren, um Benachrichtigungen über Consumer-Anforderungen zu empfangen (z. b. Anforderungen zum Hinzufügen oder Entfernen von Indikatoren aus der Abfrage). Legen Sie diesen Wert auf **null** fest, wenn Sie die *controlcallback* -Rückruffunktion nicht implementieren.

</dd> <dt>

<span id="MemoryAllocationFunction"></span><span id="memoryallocationfunction"></span><span id="MEMORYALLOCATIONFUNCTION"></span>Memoryzuweisung-Funktion
</dt> <dd>

Der Name der [*AllocateMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) -Rückruffunktion, die von Perflib zum Zuordnen von Arbeitsspeicher aufgerufen wird. Legen Sie diesen Wert auf **null** fest, wenn Sie das **-memoryroutinen-** Argument nicht angegeben haben.

</dd> <dt>

<span id="MemoryFreeFunction"></span><span id="memoryfreefunction"></span><span id="MEMORYFREEFUNCTION"></span>Memoryfrefunction
</dt> <dd>

Der Name der [*FreeMemory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_free) -Rückruffunktion, die von Perflib aufgerufen wird, um den Speicher freizugeben, der mit der Funktion " [*belegcatememory*](/windows/desktop/api/Perflib/nc-perflib-perf_mem_alloc) " belegt wird Auf **null** festgelegt, wenn *memoryzucationfunction* **null** ist.

</dd> <dt>

<span id="MemoryFunctionContext"></span><span id="memoryfunctioncontext"></span><span id="MEMORYFUNCTIONCONTEXT"></span>Memoryfunctioncontext
</dt> <dd>

Kontextinformationen, die an die Speicher Belegung und die freien Routinen übergeben werden. Kann **null** sein.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



 

