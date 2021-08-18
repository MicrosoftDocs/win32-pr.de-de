---
title: sh_token-Schlüsselwort
description: Das Schlüsselwort \sh \_ token\gibt an, dass das Systemobjekt ein Handle für ein Token ist.
keywords:
- sh_token MIDL-Schlüsselwort
topic_type:
- apiref
api_name:
- sh_token keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8305a8073d03eb90bbd214f1b56cb1174ffef66953bb170fb7f28ebf1b84d35c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066772"
---
# <a name="sh_token-keyword"></a>\_Sh-Tokenschlüsselwort

Das **\_ sh-Tokenschlüsselwort** gibt an, `system_handle` dass ein ein Handle für ein Token enthält.

``` syntax
[system_handle(sh_token)]

[system_handle(sh_token, access-rights)]
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
    HRESULT SetToken([in, system_handle(sh_token)] HANDLE token);

    HRESULT GetToken([out, system_handle(sh_token, TOKEN_QUERY)] HANDLE* pToken);
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

[Zugriffstoken](../secauthz/access-tokens.md)
</dt> <dt>

[Zugriffsrechte für Access-Token Objekte](../secauthz/access-rights-for-access-token-objects.md)
</dt> </dl>
