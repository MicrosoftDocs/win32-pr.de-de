---
title: sh_thread-Schlüsselwort
description: Das \_ \sh thread\-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für einen Thread ist.
keywords:
- sh_thread-Schlüsselwort MIDL
topic_type:
- apiref
api_name:
- sh_thread keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5cd3f5458e54ccd266f5ef0920b1cc79e1c0b42e35fac51f7ac353d22409aaa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641331"
---
# <a name="sh_thread-keyword"></a>\_sh thread-Schlüsselwort

Das **Schlüsselwort sh \_ thread** gibt an, dass `system_handle` ein ein Handle für einen Thread enthält.

``` syntax
[system_handle(sh_thread)]

[system_handle(sh_thread, access-rights)]
```

## <a name="parameters"></a>Parameter

Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).

Die [**system_handle-Dokumentation**](system-handle.md) enthält auch Details zur optionalen Verwendung des *Access-Rights-Parameters.* Das Standardverhalten entspricht `DUPLICATE_SAME_ACCESS` den [ **DuplicateHandle-Funktionsspezifikationen.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Hinweise

Um dieses Schlüsselwort mit dem -Attribut zu `system_handle` verwenden, muss das `-target` Flag auf `NT100` (oder höher) festgelegt werden, wenn midl.exe ausgeführt wird.

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

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[About Processes and Threads (Informationen zu Prozessen und Threads)](../procthread/about-processes-and-threads.md)
</dt> <dt>

[Threadsicherheit und Zugriffsrechte](../procthread/thread-security-and-access-rights.md)
</dt> <dt>

[**CreateThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
</dt> <dt>

[**OpenThread-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)
</dt> </dl>