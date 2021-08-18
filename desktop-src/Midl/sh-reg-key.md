---
title: sh_reg_key-Schlüsselwort
description: Das Schlüsselwort \sh \_ reg \_ key\ gibt an, dass das Systemobjekt ein Handle für einen Registrierungsschlüssel ist.
keywords:
- sh_reg_key-Schlüsselwort MIDL
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 321745879645f3f6346d1e4c5ba7047df203430041f2d8903b8ff506229bb1e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013608"
---
# <a name="sh_reg_key-keyword"></a>schlüsselwort sh \_ reg \_ key

Das Schlüsselwort **sh \_ reg \_ key** gibt an, dass `system_handle` ein ein Handle für einen Registrierungsschlüssel enthält.

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
```

## <a name="parameters"></a>Parameter

Dieses Schlüsselwort ist ein Parameter für [**system_handle**](system-handle.md).

Die [**system_handle-Dokumentation**](system-handle.md) enthält auch Details zur optionalen Verwendung des *Access-Rights-Parameters.* Das Standardverhalten entspricht `DUPLICATE_SAME_ACCESS` den [ **DuplicateHandle-Funktionsspezifikationen.**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)

## <a name="remarks"></a>Hinweise

Um dieses Schlüsselwort mit dem -Attribut verwenden zu `system_handle` können, muss das `-target` Flag beim Ausführen von midl.exe auf `NT100` (oder höher) festgelegt werden.

## <a name="examples"></a>Beispiele

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
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

[Registrierung](../sysinfo/registry.md)
</dt> <dt>

[Sicherheit und Zugriffsrechte für Registrierungsschlüssel](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[**RegOpenKeyEx-Funktion**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
