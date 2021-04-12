---
title: sh_thread-Schlüsselwort
description: Das \ SH \_ Thread \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für einen Thread ist.
keywords:
- sh_thread-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_thread keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2c82dc41d2b1c7cba740c897ef6cea9094979cc3
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104218923"
---
# <a name="sh_thread-keyword"></a>SH \_ Thread-Schlüsselwort

Das Schlüsselwort **SH \_ Thread** gibt an, dass ein ein `system_handle` Handle für einen Thread enthält.

``` syntax
[system_handle(sh_thread)]

[system_handle(sh_thread, access-rights)]
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
    HRESULT SetThread([in, system_handle(sh_process)] HANDLE threadHandle);
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

[Thread Sicherheit und Zugriffsrechte](../procthread/thread-security-and-access-rights.md)
</dt> <dt>

[Funktion " **foratethread** "](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
</dt> <dt>

[**Openthread** -Funktion](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)
</dt> </dl>