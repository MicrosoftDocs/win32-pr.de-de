---
title: sh_semaphore-Schlüsselwort
description: Das \ SH \_ Semaphore \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für ein Semaphor ist.
keywords:
- sh_semaphore-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2a5c33e4c44b67e3106a48cde244abaf13f41ad5
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "106354251"
---
# <a name="sh_semaphore-keyword"></a>SH \_ Semaphor-Schlüsselwort

Das **SH \_ Semaphor** -Schlüsselwort gibt an, dass ein ein `system_handle` Handle für ein Semaphor enthält.

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
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
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
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

[Semaphore-Objekte](../sync/semaphore-objects.md)
</dt> <dt>

[Sicherheits-und Zugriffsrechte für das Synchronisierungs Objekt](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[Funktion " **kreatesemaphore** "](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[Funktion " **kreatesemaphoreex** "](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
