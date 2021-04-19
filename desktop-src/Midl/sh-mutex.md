---
title: sh_mutex-Schlüsselwort
description: Das \ SH \_ Mutex \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für einen Mutex ist.
keywords:
- sh_mutex-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363052"
---
# <a name="sh_mutex-keyword"></a>SH \_ Mutex-Schlüsselwort

Das **SH \_ Mutex** -Schlüsselwort gibt an, dass ein ein `system_handle` Handle für einen Mutex enthält.

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
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
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
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

[Mutex-Objekte](../sync/mutex-objects.md)
</dt> <dt>

[Sicherheits-und Zugriffsrechte für das Synchronisierungs Objekt](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[Funktion " **kreatemutex** "](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[Funktion "up- **MUTEXEX** "](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>