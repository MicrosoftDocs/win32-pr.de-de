---
description: Sucht die Zielfunktion des angegebenen Imports und ersetzt den Funktionszeiger im Importthunk durch das Ziel der Funktionsimplementierung.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: ResolveDelayLoadedAPI-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 359de5c52417f09c35e2fc994e36f0efd054f2a18dc3063be71dc12d588c60e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571550"
---
# <a name="resolvedelayloadedapi-function"></a>ResolveDelayLoadedAPI-Funktion

Sucht die Zielfunktion des angegebenen Imports und ersetzt den Funktionszeiger im Importthunk durch das Ziel der Funktionsimplementierung.

## <a name="syntax"></a>Syntax


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ParentModuleBase* \[ In\]
</dt> <dd>

Die Adresse der Basis des Moduls, das eine verzögert geladene Funktion importiert.

</dd> <dt>

*DelayloadDescriptor* \[ In\]
</dt> <dd>

Der Deskriptor für das zu ladende Modul.

</dd> <dt>

*FailureDllHook* \[ in, optional\]
</dt> <dd>

Die Adresse des Fehlerhooks. Siehe [**DelayLoadFailureHook**](delayloadfailurehook.md).

</dd> <dt>

*FailureSystemHook* \[ in, optional\]
</dt> <dd>

Die Adresse des Systemfehlerhooks.

</dd> <dt>

*ThunkAddress* \[ out\]
</dt> <dd>

Die Thunkdaten für die Zielfunktion. Wird verwendet, um den spezifischen Namenstabelleneintrag der Funktion zu suchen.

</dd> <dt>

*Flags* 
</dt> <dd>

Reserviert; muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Adresse des Imports oder der Fehlerstub dafür.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Linkerunterstützung für Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




