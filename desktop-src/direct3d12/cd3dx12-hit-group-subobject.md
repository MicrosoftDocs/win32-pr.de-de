---
title: CD3DX12_HIT_GROUP_SUBOBJECT -Klasse (D3dx12.h)
description: Eine Hilfsklasse zum Erstellen eines Treffergruppenzustands-Unterobjekts.
keywords:
- CD3DX12_HIT_GROUP_SUBOBJECT-Klasse
topic_type:
- apiref
api_name:
- CD3DX12_HIT_GROUP_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 68b95f15c41fd46bfaeb58943720d3b657a3208d9a0276e9ab65fe7bd6087c42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037369"
---
# <a name="cd3dx12_hit_group_subobject-class"></a>CD3DX12_HIT_GROUP_SUBOBJECT-Klasse

Eine Hilfsklasse zum Erstellen eines Treffergruppenzustands-Unterobjekts.

Weitere Informationen zu den D3DX12 State Object Creation Helpers finden Sie [unter CD3DX12_STATE_OBJECT_DESC.](cd3dx12-state-object-desc.md)

## <a name="syntax"></a>Syntax

```cpp
class CD3DX12_HIT_GROUP_SUBOBJECT
{
    CD3DX12_HIT_GROUP_SUBOBJECT() noexcept;
    CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetHitGroupExport(LPCWSTR exportName);
    void SetHitGroupType(D3D12_HIT_GROUP_TYPE Type) noexcept;
    void SetAnyHitShaderImport(LPCWSTR importName);
    void SetClosestHitShaderImport(LPCWSTR importName);
    void SetIntersectionShaderImport(LPCWSTR importName);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept { return *m_pSubobject; }
    operator const D3D12_HIT_GROUP_DESC& () const noexcept { return m_Desc; }
};
```

## <a name="members"></a>Member

`CD3DX12_HIT_GROUP_SUBOBJECT`

Standardkonstruktor Erstellt eine neue, standardmäßig initialisierte Instanz eines **CD3DX12_HIT_GROUP_SUBOBJECT.**

`CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Konstruktor, der eine neue Instanz eines -Objekts **CD3DX12_HIT_GROUP_SUBOBJECT** mit dem Inhalt eines CD3DX12_STATE_OBJECT_DESC [**initialisiert**](cd3dx12-state-object-desc.md) wird.

`SetHitGroupExport(LPCWSTR)`

Funktion zum Festlegen des Namens der Treffergruppe.

`SetHitGroupType(D3D12_HIT_GROUP_TYPE)`

Funktion zum Festlegen eines Werts aus [der](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type) D3D12_HIT_GROUP_TYPE Enumeration, die den Typ der Treffergruppe an gibt.

`SetAnyHitShaderImport(LPCWSTR)`

Funktion zum optionalen Festlegen des Namens des beliebigen Treffer-Shaders, der der Treffergruppe zugeordnet ist.

`SetClosestHitShaderImport(LPCWSTR)`

Funktion zum optionalen Festlegen des Namens des Shaders mit dem nächsten Treffer, der der Treffergruppe zugeordnet ist.

`SetIntersectionShaderImport(LPCWSTR)`

Funktion zum optionalen Festlegen des Namens des optionalen Namens des Schnittpunkt-Shaders, der der Treffergruppe zugeordnet ist.

`Type`

Ruft den Typ des Unterobjekts ab, dargestellt durch [die](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) D3D12_STATE_SUBOBJECT_TYPE_HIT_GROUP Konstante.

`operator const D3D12_STATE_SUBOBJECT&`

Konvertierungsoperator, der einen Verweis auf eine Konstante D3D12_STATE_SUBOBJECT [Objekt](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) zurückgibt, das das Zustandsobjekt beschreibt.

`operator const D3D12_HIT_GROUP_DESC&`

Konvertierungsoperator, der einen Verweis auf eine Konstante D3D12_HIT_GROUP_DESC [objekt](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) zurückgibt, die das Zustandsobjekt beschreibt.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Weitere Informationen:

* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
