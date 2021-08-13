---
title: sh_mutex-Schlüsselwort
description: Das \_ \sh mutex\-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für einen Mutex ist.
keywords:
- sh_mutex-Schlüsselwort MIDL
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a355eb0121875e186a485ee6f7f96519a4fa0cfb1c75c806e1baea895691c914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641365"
---
# <a name="sh_mutex-keyword"></a>sh \_ mutex-Schlüsselwort

Das **\_ sh mutex-Schlüsselwort** gibt an, dass `system_handle` ein ein Handle für einen Mutex enthält.

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
```

## <a name="parameters"></a>Parameter

Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).

Die [**system_handle-Dokumentation**](system-handle.md) enthält auch Details zur optionalen Verwendung des *Access-Rights-Parameters.* Das Standardverhalten entspricht `DUPLICATE_SAME_ACCESS` den [ **DuplicateHandle-Funktionsspezifikationen.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Hinweise

Um dieses Schlüsselwort mit dem -Attribut verwenden zu `system_handle` können, muss das `-target` Flag auf `NT100` (oder höher) festgelegt werden, wenn midl.exe ausgeführt wird.

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

## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Mutex-Objekte](../sync/mutex-objects.md)
</dt> <dt>

[Sicherheit und Zugriffsrechte für Synchronisierungsobjekte](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateMutex-Funktion**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[**CreateMutexEx-Funktion**](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>