---
title: sh_composition-Schlüsselwort
description: Das \ SH \_ Composition \-Schlüsselwort gibt an, dass das Systemobjekt ein Handle für eine Kompositions Oberfläche ist.
keywords:
- sh_composition-Schlüsselwort-Mittel l
topic_type:
- apiref
api_name:
- sh_composition
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5a7e723c65ca6320dbec4a2f8a379cfed2f85f72
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2021
ms.locfileid: "104218918"
---
# <a name="sh_composition-keyword"></a>SH \_ Composition-Schlüsselwort

Das Schlüsselwort **SH \_ Composition** gibt an, dass ein ein `system_handle` Handle für eine Kompositions Oberfläche enthält.

``` syntax
[system_handle(sh_composition)]

[system_handle(sh_composition, access-rights)]
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
    HRESULT GetVisualSurface([out, system_handle(sh_composition)] HANDLE* visual);
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

[DirectComposition](/windows/win32/api/_directcomp/)
</dt> <dt>

[**Dcompositionkreatesurfakehandle** -Funktion](/windows/win32/api/dcomp/nf-dcomp-dcompositioncreatesurfacehandle)
</dt> </dl>
