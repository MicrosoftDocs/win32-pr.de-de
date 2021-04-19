---
title: sh_process-Schlüsselwort
description: Das \ SH \_ Process \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für einen Prozess ist.
keywords:
- sh_process-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3652c6889c687173bbf7b397cddff4659c0329f1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "106362804"
---
# <a name="sh_process-keyword"></a>SH \_ Process-Schlüsselwort

Das **SH \_ Process** -Schlüsselwort gibt an, dass ein ein `system_handle` Handle für einen Prozess enthält.

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
```

## <a name="parameters"></a>Parameter

Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).

Die [**system_handle**](system-handle.md) Dokumentation enthält auch Details zur optionalen Verwendung des *Zugriffsrechte* Parameters. Das Standardverhalten entspricht den `DUPLICATE_SAME_ACCESS` Spezifikationen für [ **Duplikat-andle** -Funktionen](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

## <a name="remarks"></a>Bemerkungen

Um dieses Schlüsselwort mit dem-Attribut zu verwenden `system_handle` , `-target` muss das-Flag `NT100` beim Ausführen von midl.exe auf (oder höher) festgelegt werden.

## <a name="examples"></a>Beispiele

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
}
```

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 10 Anniversary Update (Version 1607, Build 14393) |
| Unterstützte Mindestversion (Server) | Windows Server 2016 (Build 14393) |

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[About Processes and Threads (Informationen zu Prozessen und Threads)](../procthread/about-processes-and-threads.md)
</dt> <dt>

[Prozesssicherheit und Zugriffsrechte](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[Funktion " **deateprocess** "](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[**OpenProcess** -Funktion](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>