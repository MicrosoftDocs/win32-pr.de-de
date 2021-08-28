---
title: sh_event-Schlüsselwort
description: Das Schlüsselwort \sh \_ event\ gibt an, dass das Systemobjekt ein Handle für ein Ereignis ist.
keywords:
- sh_event-Schlüsselwort MIDL
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: b2f489c27d32c40f80cef326b99131158df92cad2183cee1dc5a3dd74310cf6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013648"
---
# <a name="sh_event-keyword"></a>\_sh event-Schlüsselwort

Das **schlüsselwort sh \_ event** gibt an, dass `system_handle` ein ein Handle für ein Ereignis enthält.

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
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
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
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

[Ereignisobjekte](../sync/event-objects.md)
</dt> <dt>

[Sicherheit und Zugriffsrechte für Synchronisierungsobjekte](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[**CreateEvent-Funktion**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**CreateEventEx-Funktion**](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
