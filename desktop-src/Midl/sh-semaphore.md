---
title: sh_semaphore-Schlüsselwort
description: Das Schlüsselwort \sh \_ semaphore\ gibt an, dass das Systemobjekt ein Handle für ein Semaphor ist.
keywords:
- sh_semaphore-Schlüsselwort MIDL
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a48d0b085f3653679c7399ad0f234e7b7a1ecf1b1532480c003923967ac4830a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383220"
---
# <a name="sh_semaphore-keyword"></a>\_sh-Semaphorschlüsselwort

Das **Schlüsselwort sh \_ semaphore** gibt an, dass `system_handle` ein ein Handle für ein Semaphor enthält.

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
```

## <a name="parameters"></a>Parameter

Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).

Die [**system_handle-Dokumentation**](system-handle.md) enthält auch Details zur optionalen Verwendung des *Access-Rights-Parameters.* Das Standardverhalten entspricht `DUPLICATE_SAME_ACCESS` den [ **DuplicateHandle-Funktionsspezifikationen.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Hinweise

Um dieses Schlüsselwort mit dem -Attribut zu `system_handle` verwenden, muss das `-target` Flag bei der Ausführung von midl.exe auf `NT100` (oder höher) festgelegt werden.

## <a name="examples"></a>Beispiele

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
}
```

## <a name="requirements"></a>Anforderungen

| &nbsp; | &nbsp; |
|-|-|
| Unterstützte Mindestversion (Client) | Windows 10 Anniversary Update (Version 1607, Build 14393) |
| Unterstützte Mindestversion (Server) | Windows Server 2016 (Build 14393) |

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Semaphorobjekte](../sync/semaphore-objects.md)
</dt> <dt>

[Sicherheit und Zugriffsrechte für Synchronisierungsobjekte](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateSemaphore-Funktion**](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[**CreateSemaphoreEx-Funktion**](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
