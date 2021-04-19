---
title: sh_event-Schlüsselwort
description: Das \ SH \_ Event \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für ein Ereignis ist.
keywords:
- sh_event-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1a9b6dc7cc9dc4de4abd5dcc88a53588167db59d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "106367259"
---
# <a name="sh_event-keyword"></a>SH \_ Event-Schlüsselwort

Das **SH- \_ Ereignis** Schlüsselwort gibt an, dass ein `system_handle` ein Handle für ein Ereignis enthält.

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
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

[Ereignis Objekte](../sync/event-objects.md)
</dt> <dt>

[Sicherheits-und Zugriffsrechte für das Synchronisierungs Objekt](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[Funktion " **kreateevent** "](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[Funktion " **kreateeventex** "](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
