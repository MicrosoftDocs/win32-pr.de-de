---
title: CD3DX12_VIEW_INSTANCING_DESC -Struktur (D3dx12.h)
description: Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) ermöglicht.
keywords:
- CD3DX12_VIEW_INSTANCING_DESC-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_VIEW_INSTANCING_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 51c9f5caf5bedf9712001420993393a2dcfa6870
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813261"
---
# <a name="cd3dx12_view_instancing_desc-structure"></a>CD3DX12_VIEW_INSTANCING_DESC-Struktur

Eine Hilfsstruktur, die eine einfache Initialisierung einer [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) ermöglicht.

## <a name="syntax"></a>Syntax

```cpp
struct CD3DX12_VIEW_INSTANCING_DESC : public D3D12_VIEW_INSTANCING_DESC
{
    CD3DX12_VIEW_INSTANCING_DESC();
    explicit CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC& o) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(
        UINT InViewInstanceCount,
        const D3D12_VIEW_INSTANCE_LOCATION* InViewInstanceLocations,
        D3D12_VIEW_INSTANCING_FLAGS InFlags) noexcept;
};
```

## <a name="members"></a>Member

`CD3DX12_VIEW_INSTANCING_DESC`

Standardkonstruktor Erstellt eine neue, nicht initialisierte Instanz eines **CD3DX12_VIEW_INSTANCING_DESC.**

`CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC&)`

Konstruktor, der eine neue Instanz eines **-CD3DX12_VIEW_INSTANCING_DESC** mit dem Inhalt einer -Struktur [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) initialisiert wird.

`CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT)`

Konstruktor, der eine neue Instanz eines **-CD3DX12_VIEW_INSTANCING_DESC** mit diesen Werten initialisiert wird.

|Datenelement|Wert|
|-|-|
|ViewInstanceCount|0|
|pViewInstanceLocations|nullptr|
|Flags|D3D12_VIEW_INSTANCING_FLAG_NONE|

`CD3DX12_VIEW_INSTANCING_DESC(UINT, const D3D12_VIEW_INSTANCE_LOCATION*, D3D12_VIEW_INSTANCING_FLAGS)`

Konstruktor, der eine neue Instanz eines **-CD3DX12_VIEW_INSTANCING_DESC** mit den übergebenen Parametern initialisiert wird.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Siehe auch

* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
