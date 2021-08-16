---
title: CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT-Klasse (D3dx12.h)
description: Eine Hilfsklasse zum Erstellen eines Unterobjekts, das die allgemeinen Eigenschaften eines Zustandsobjekts definiert.
keywords:
- CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT-Klasse
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/05/2021
ms.openlocfilehash: 294dda04f9550e437f91f6f5595206a4113a975ee182ac900b6c4804b3100fb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346560"
---
# <a name="cd3dx12_state_object_config_subobject-class"></a>CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT-Klasse

Eine Hilfsklasse zum Erstellen eines Unterobjekts, das die allgemeinen Eigenschaften eines Zustandsobjekts definiert.

Weitere Informationen zu den D3DX12 State Object Creation Helpers finden Sie unter [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Syntax

```cpp
class CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT
{
public:
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT() noexcept;
    CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetFlags(D3D12_STATE_OBJECT_FLAGS Flags) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_STATE_OBJECT_CONFIG& () const noexcept;
};
```

## <a name="members"></a>Member

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT`

Standardkonstruktor Erstellt eine neue, standardmäßig initialisierte Instanz eines **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT**.

`CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Konstruktor, der eine neue Instanz eines **CD3DX12_STATE_OBJECT_CONFIG_SUBOBJECT** mit dem Inhalt eines [**CD3DX12_STATE_OBJECT_DESC-Objekts**](cd3dx12-state-object-desc.md) initialisiert.

`SetFlags(D3D12_STATE_OBJECT_FLAGS)`

Funktion zum Angeben der Anforderungen für [](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_flags) das Zustandsobjekt über ein D3D12_STATE_OBJECT_FLAGS-Objekt.

`Type`

Ruft den Typ des Unterobjekts ab, das durch die [D3D12_STATE_SUBOBJECT_TYPE_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) Konstante dargestellt wird.

`operator const D3D12_STATE_SUBOBJECT&`

Konvertierungsoperator, der einen Verweis auf eine Konstante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) Objekt zurückgibt, das das Zustandsobjekt beschreibt.

`operator const D3D12_STATE_OBJECT_CONFIG&`

Konvertierungsoperator, der einen Verweis auf eine Konstante [D3D12_STATE_OBJECT_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_config) Objekt zurückgibt, das das Zustandsobjekt beschreibt.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Weitere Informationen

* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
