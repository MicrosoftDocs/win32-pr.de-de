---
description: Gibt die Zielfunktion des angegebenen Imports an und ersetzt den Funktionszeiger im Import Thunk durch das Ziel der Funktions Implementierung.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: Resolvedelta-loadedapi-Funktion
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
ms.openlocfilehash: 019729cacb45cce87de2cc4015c661c494125108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370184"
---
# <a name="resolvedelayloadedapi-function"></a>Resolvedelta-loadedapi-Funktion

Gibt die Zielfunktion des angegebenen Imports an und ersetzt den Funktionszeiger im Import Thunk durch das Ziel der Funktions Implementierung.

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

" *Parametrimodulebase* \[ " in\]
</dt> <dd>

Die Adresse der Basis des Moduls, das eine verzögert geladene Funktion importiert.

</dd> <dt>

*Delta-loaddescriptor* \[ in\]
</dt> <dd>

Der Deskriptor für das Modul, das geladen werden soll.

</dd> <dt>

*Failuredllhook* \[ in, optional\]
</dt> <dd>

Die Adresse des fehlerhaften Hooks. Siehe " [**Delta-loadfailurehook**](delayloadfailurehook.md)".

</dd> <dt>

*Failuresystemhook* \[ in, optional\]
</dt> <dd>

Die Adresse des Systemfehler-Hooks.

</dd> <dt>

*Thunkaddress* \[ vorgenommen\]
</dt> <dd>

Die Thunk-Daten für die Zielfunktion. Wird verwendet, um den Namen der jeweiligen namens Tabelle der Funktion zu suchen.

</dd> <dt>

*Flags* 
</dt> <dd>

Bleiben muss 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Adresse des Imports oder der fehlerstub für die Anwendung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Linker-Unterstützung für Delay-Loaded DLLs](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




