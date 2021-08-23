---
title: sh_file-Schlüsselwort
description: Das \_ \sh file\-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für eine Datei ist.
keywords:
- sh_file-Schlüsselwort MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 05b76ad772ca628a28677d9b0da06252d0fec70251a4a197d39b50b9760ef931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013628"
---
# <a name="sh_file-keyword"></a>\_sh file-Schlüsselwort

Das **Schlüsselwort sh \_ file** gibt an, dass `system_handle` ein ein Handle für eine Datei enthält.

``` syntax
[system_handle(sh_file)]

[system_handle(sh_file, access-rights)]
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
    HRESULT WriteThisFile([in, system_handle(sh_file)] HANDLE file);

    HRESULT GetFileToRead([out, system_handle(sh_file, READ_CONTROL | SYNCHRONIZE | FILE_READ_DATA | FILE_READ_keywordS | FILE_READ_EA)] HANDLE* pReadThisFile);
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

[Dateisicherheit und Zugriffsrechte](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[DirectComposition](/windows/win32/api/_directcomp/)
</dt> <dt>

[**DCompositionCreateSurfaceHandle-Funktion**](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> <dt>
