---
title: CD3DX12_NODE_MASK_SUBOBJECT -Klasse (D3dx12.h)
description: Eine Hilfsklasse zum Erstellen eines Zustandsunterobjekts, das die GPU-Knoten identifiziert, auf die das Zustandsobjekt angewendet wird.
keywords:
- CD3DX12_NODE_MASK_SUBOBJECT-Klasse
topic_type:
- apiref
api_name:
- CD3DX12_NODE_MASK_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: c71a2aa97e376a03b3f77f38a3101c26930e788403f1cef9b26e2c77d4598be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752230"
---
# <a name="cd3dx12_node_mask_subobject-class"></a>CD3DX12_NODE_MASK_SUBOBJECT-Klasse

Eine Hilfsklasse zum Erstellen eines Zustandsunterobjekts, das die GPU-Knoten identifiziert, auf die das Zustandsobjekt angewendet wird.

Weitere Informationen zu den D3DX12 State Object Creation Helpers finden Sie [unter CD3DX12_STATE_OBJECT_DESC.](cd3dx12-state-object-desc.md)

## <a name="syntax"></a>Syntax

```cpp
class CD3DX12_NODE_MASK_SUBOBJECT
{
    CD3DX12_NODE_MASK_SUBOBJECT() noexcept;
    CD3DX12_NODE_MASK_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetNodeMask(UINT NodeMask) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_NODE_MASK& () const noexcept;
};
```

## <a name="members"></a>Member

`CD3DX12_NODE_MASK_SUBOBJECT`

Standardkonstruktor Erstellt eine neue, standardmäßig initialisierte Instanz eines **CD3DX12_NODE_MASK_SUBOBJECT.**

`CD3DX12_NODE_MASK_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Konstruktor, der eine neue Instanz eines -Objekts **CD3DX12_NODE_MASK_SUBOBJECT** mit dem Inhalt eines CD3DX12_STATE_OBJECT_DESC [**initialisiert**](cd3dx12-state-object-desc.md) wird.

`SetNodeMask(UINT)`

Funktion zum Festlegen der Knotenmaske.

`Type`

Ruft den Typ des Unterobjekts ab, dargestellt durch [die](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) D3D12_STATE_SUBOBJECT_TYPE_NODE_MASK Konstante.

`operator const D3D12_STATE_SUBOBJECT&`

Konvertierungsoperator, der einen Verweis auf eine Konstante D3D12_STATE_SUBOBJECT [Objekt](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) zurückgibt, das das Zustandsobjekt beschreibt.

`operator const D3D12_NODE_MASK&`

Konvertierungsoperator, der einen Verweis auf eine Konstante D3D12_NODE_MASK [Objekt](/windows/win32/api/d3d12/ns-d3d12-d3d12_node_mask) zurückgibt, das das Zustandsobjekt beschreibt.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Weitere Informationen

* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
