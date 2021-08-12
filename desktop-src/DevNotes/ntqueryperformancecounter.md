---
description: Gibt den aktuellen Wert eines Leistungsindikators und optional die Häufigkeit des Leistungsindikators zurück.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: NtQueryPerformanceCounter-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9c92863adbc0865700dad272bbc299e1f1a667b2fd4afbcd75d548e3330890b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667227"
---
# <a name="ntqueryperformancecounter-function"></a>NtQueryPerformanceCounter-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden. Verwenden Sie stattdessen die Funktionen **QueryPerformanceCounter** und **QueryPerformanceFrequency.**\]

Gibt den aktuellen Wert eines Leistungsindikators und optional die Häufigkeit des Leistungsindikators zurück.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PerformanceCounter* \[ out\]
</dt> <dd>

Die Adresse einer Variablen, die den aktuellen Leistungsindikatorwert empfangen soll.

</dd> <dt>

*PerformanceFrequency* \[ out, optional\]
</dt> <dd>

Die Adresse einer Variablen, die die Häufigkeit des Leistungsindikators empfangen soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, wird der **NTSTATUS-Code** **STATUS \_ SUCCESS** zurückgegeben. Andernfalls wird ein Fehlercode wie **STATUS ACCESS \_ \_ VIOLATION** zurückgegeben.

## <a name="remarks"></a>Hinweise

Für **NtQueryPerformanceCounter** ist keine Headerdatei verfügbar. Sie sollten die oben genannten alternativen Funktionen verwenden, obwohl Sie auch die [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) verwenden können, um dynamisch mit Ntdll.dll zu verknüpfen.

Leistungshäufigkeit ist die Häufigkeit des Leistungsindikators in Hertz, insbesondere bei der Anzahl pro Sekunde. Dieser Wert ist implementierungsabhängig. Wenn die Implementierung nicht über Hardware zur Unterstützung der Leistungssteuerung verfügt, wird der Wert 0 zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
