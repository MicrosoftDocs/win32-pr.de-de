---
title: sh_process-Schlüsselwort
description: Das Schlüsselwort \sh \_ process\ gibt an, dass das Systemobjekt ein Handle für einen Prozess ist.
keywords:
- sh_process MIDL-Schlüsselwort
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3dc11f2980e5124bbc76d0b57fce21d8007b0c09905ca47707d5be6fbb112d41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146273"
---
# <a name="sh_process-keyword"></a>sh \_ process-Schlüsselwort

Das **sh \_ process-Schlüsselwort** gibt an, dass `system_handle` ein ein Handle für einen Prozess enthält.

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
```

## <a name="parameters"></a>Parameter

Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).

Die [**system_handle**](system-handle.md) dokumentation enthält auch Details zur optionalen Verwendung des *Access Rights-Parameters.* Das Standardverhalten entspricht `DUPLICATE_SAME_ACCESS` den [ **Spezifikationen der DuplicateHandle-Funktion.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Hinweise

Um dieses Schlüsselwort mit dem -Attribut verwenden zu können, muss das Flag auf (oder höher) festgelegt werden, `system_handle` `-target` wenn sie `NT100` midl.exe.

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

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[About Processes and Threads (Informationen zu Prozessen und Threads)](../procthread/about-processes-and-threads.md)
</dt> <dt>

[Prozesssicherheit und Zugriffsrechte](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[**CreateProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[**OpenProcess-Funktion**](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>