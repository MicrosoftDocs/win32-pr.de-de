---
description: Gibt den aktuellen Wert eines Leistungs Zählers und optional die Häufigkeit des Leistungs Zählers zurück.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: Ntqueryperformancecounter-Funktion
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
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369453"
---
# <a name="ntqueryperformancecounter-function"></a>Ntqueryperformancecounter-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden. Verwenden Sie stattdessen die Funktionen **QueryPerformanceCounter** und **QueryPerformanceFrequency** .\]

Gibt den aktuellen Wert eines Leistungs Zählers und optional die Häufigkeit des Leistungs Zählers zurück.

## <a name="syntax"></a>Syntax


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Performance Counter* \[ vorgenommen\]
</dt> <dd>

Die Adresse einer Variablen, die den aktuellen Leistungs Zählers Wert empfangen soll.

</dd> <dt>

*Performance Frequency* \[ Out, optional\]
</dt> <dd>

Die Adresse einer Variablen, die die Häufigkeit des Leistungs Zählers empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt Sie den **NTSTATUS** -Code **Status \_ Erfolg** zurück. andernfalls wird ein Fehlercode zurückgegeben, z. b. eine **Status \_ Zugriffs \_ Verletzung**.

## <a name="remarks"></a>Bemerkungen

Für **ntqueryperformancecounter** ist keine Header Datei verfügbar. Sie sollten die oben genannten alternativen Funktionen verwenden, obwohl Sie auch die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden können, um dynamisch mit Ntdll.dll zu verknüpfen.

Die Leistungs Häufigkeit ist die Häufigkeit des Leistungs Zählers in Hertz, insbesondere in Zählungen pro Sekunde. Dieser Wert ist implementierungsabhängig. Wenn die Implementierung nicht über Hardware zur Unterstützung der Leistungszeit verfügt, wird der zurückgegebene Wert 0 zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
