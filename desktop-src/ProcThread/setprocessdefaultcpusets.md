---
description: Legt die STANDARDMÄßIGE CPU Sets-Zuweisung für Threads im angegebenen Prozess fest. Threads, die erstellt werden und deren CPU-Mengen nicht explizit mit SetThreadSelectedCpuSets festgelegt wurden, erben automatisch die von SetProcessDefaultCpuSets angegebenen Sätze.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: SetProcessDefaultCpuSets-Funktion (Processthreadapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 3e085f769e5b086c1f68d721df6463afa7f51a0e5f9f292c7fce1dadd0356535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793177"
---
# <a name="setprocessdefaultcpusets-function"></a>SetProcessDefaultCpuSets-Funktion

Legt die STANDARDMÄßIGE CPU Sets-Zuweisung für Threads im angegebenen Prozess fest. Threads, die erstellt werden und deren CPU-Mengen nicht explizit mit [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md)festgelegt wurden, erben automatisch die von **SetProcessDefaultCpuSets** angegebenen Sätze.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Prozess* \[ In\]
</dt> <dd>

Gibt den Prozess an, für den die STANDARD-CPU-Sätze festgelegt werden. Dieses Handle muss über das Zugriffsrecht PROCESS \_ SET \_ LIMITED INFORMATION \_ verfügen. Der von [**GetCurrentProcess zurückgegebene**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) Wert kann auch hier angegeben werden.

</dd> <dt>

*CpuSetIds* \[ in, optional\]
</dt> <dd>

Gibt die Liste der CPU-Satz-IDs an, die als Standard-CPU-Satz für den Prozess festgelegt werden. Wenn dies NULL ist, gibt **SetProcessDefaultCpuSets** alle Zuweisungen frei.

</dd> <dt>

*CpuSetIdCound* \[ In\]
</dt> <dd>

Gibt die Anzahl der IDs in der Liste an, die im **CpuSetIds-Argument übergeben** werden. Wenn dieser Wert NULL ist, sollte dieser 0 sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann nicht fehlschlagen, wenn gültige Parameter übergeben werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Desktop-Apps \| UWP-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Desktop-Apps \| UWP-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Processthreadsapi.h</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Windows.h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
