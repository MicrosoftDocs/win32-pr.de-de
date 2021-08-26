---
title: Symbol "D3D12SDKVersion"
description: Die Versionsnummer des Direct3D 12 SDK.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/25/2021
req.lib: ''
req.dll: d3d12core.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d12core.dll
api_name:
- D3D12SDKVersion
targetos: Windows
ms.openlocfilehash: 0bf0aa17e16a4274b69e80580c0615ed055dd97a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917921"
---
# <a name="d3d12sdkversion-symbol"></a>Symbol "D3D12SDKVersion"

Die Versionsnummer des Direct3D 12 SDK.

## <a name="syntax"></a>Syntax

```cpp
extern "C" { _declspec(dllexport) extern const UINT D3D12SDKVersion = n;}
```

## <a name="return-value"></a>Rückgabewert

Ein [UINT mit](/windows/win32/winprog/windows-data-types) der Versionsnummer des Direct3D 12 SDK.

## <a name="remarks"></a>Hinweise

**D3D12SDKVersion** ist weder einer Importbibliothek noch einer Headerdatei zugeordnet.

## <a name="requirements"></a>Requirements (Anforderungen)

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Zielplattform** | Windows |
| **Header** | – |
| **Bibliothek** | – |
| **DLL** | d3d12core.dll |

## <a name="see-also"></a>Weitere Informationen
