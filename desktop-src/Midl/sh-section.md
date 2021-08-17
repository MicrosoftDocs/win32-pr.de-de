---
title: sh_section-Schlüsselwort
description: Das Schlüsselwort \sh \_ section\ gibt an, dass das Systemobjekt ein Handle für einen Abschnitt ist.
keywords:
- sh_section MIDL-Schlüsselwort
topic_type:
- apiref
api_name:
- sh_section keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: eab938b414745a24f81c1f61f2320443e7f3e9600eefab5f590598294345d83f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117806249"
---
# <a name="sh_section-keyword"></a>sh \_ section-Schlüsselwort

Das **schlüsselwort \_ sh section** gibt an, dass ein ein Handle für einen Abschnitt `system_handle` enthält.

``` syntax
[system_handle(sh_section)]

[system_handle(sh_section, access-rights)]
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
    HRESULT GiveSection([in, system_handle(sh_section)] HANDLE section);

    HRESULT GetSectionToWatch([out, system_handle(sh_section, SECTION_MAP_READ)] HANDLE* pSection);
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

[Abschnittsobjekte und Ansichten](/windows-hardware/drivers/kernel/section-objects-and-views)
</dt> <dt>

[**ZwCreateSection-Funktion** (einschließlich Zugriffsspezifikationen)](/windows-hardware/drivers/ddi/wdm/nf-wdm-zwcreatesection)
</dt> </dl>
