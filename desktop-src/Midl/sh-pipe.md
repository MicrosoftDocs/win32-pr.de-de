---
title: sh_pipe-Schlüsselwort
description: Das Schlüsselwort \sh \_ pipe\ gibt an, dass das Systemobjekt ein Handle für eine Pipe ist.
keywords:
- sh_pipe MIDL-Schlüsselwort
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 15bee0e34525d83af10e5c42199116dc6080a6a7b7f4e2af3de565f62a9c6a5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383345"
---
# <a name="sh_pipe-keyword"></a>sh \_ pipe-Schlüsselwort

Das **Sh \_ Pipe-Schlüsselwort** gibt an, dass `system_handle` ein ein Handle für eine Pipe enthält.

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
```

## <a name="parameters"></a>Parameter

Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).

Die [**system_handle**](system-handle.md) dokumentation enthält auch Details zur optionalen Verwendung des *Access Rights-Parameters.* Das Standardverhalten entspricht `DUPLICATE_SAME_ACCESS` den [ **Spezifikationen der DuplicateHandle-Funktion.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Hinweise

Um dieses Schlüsselwort mit dem -Attribut zu verwenden, muss das -Flag auf (oder höher) festgelegt werden, `system_handle` `-target` wenn `NT100` midl.exe.

## <a name="examples"></a>Beispiele

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
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

[Informationen zu Pipes](../ipc/about-pipes.md)
</dt> <dt>

[Dateisicherheit und Zugriffsrechte](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[**CreatePipe-Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[**CreateNamedPipe-Funktion**](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
