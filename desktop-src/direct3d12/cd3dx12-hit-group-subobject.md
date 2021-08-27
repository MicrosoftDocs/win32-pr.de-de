---
title: CD3DX12_HIT_GROUP_SUBOBJECT-Klasse (D3dx12.h)
description: Eine Hilfsklasse zum Erstellen eines Teilobjekts für den Status einer Treffergruppe.
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
ms.openlocfilehash: dd2b396e1305d2cf21cb2121aaa6a186c47d7677
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813100"
---
# <a name="cd3dx12_hit_group_subobject-class"></a>CD3DX12_HIT_GROUP_SUBOBJECT-Klasse

Eine Hilfsklasse zum Erstellen eines Teilobjekts für den Status einer Treffergruppe.

Weitere Informationen zu den D3DX12 State Object Creation Helpers finden Sie unter [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

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

Standardkonstruktor Erstellt eine neue, standardmäßig initialisierte Instanz eines **CD3DX12_HIT_GROUP_SUBOBJECT**.

`CD3DX12_HIT_GROUP_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Konstruktor, der eine neue Instanz eines **CD3DX12_HIT_GROUP_SUBOBJECT** mit dem Inhalt eines [**CD3DX12_STATE_OBJECT_DESC-Objekts**](cd3dx12-state-object-desc.md) initialisiert.

`SetHitGroupExport(LPCWSTR)`

Funktion zum Festlegen des Namens der Treffergruppe.

`SetHitGroupType(D3D12_HIT_GROUP_TYPE)`

Funktion zum Festlegen eines Werts aus der [D3D12_HIT_GROUP_TYPE](/windows/win32/api/d3d12/ne-d3d12-d3d12_hit_group_type) Enumeration, die den Typ der Treffergruppe angibt.

`SetAnyHitShaderImport(LPCWSTR)`

Funktion zum optionalen Festlegen des Namens des beliebigen Treffer-Shaders, der der Treffergruppe zugeordnet ist.

`SetClosestHitShaderImport(LPCWSTR)`

Funktion zum optionalen Festlegen des Namens des Shaders, der der Treffergruppe am nächsten liegt.

`SetIntersectionShaderImport(LPCWSTR)`

Funktion zum optionalen Festlegen des Namens des optionalen Namens des Schnittmengen-Shaders, der der Treffergruppe zugeordnet ist.

`Type`

Ruft den Typ des Unterobjekts ab, das durch die [D3D12_STATE_SUBOBJECT_TYPE_HIT_GROUP](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) Konstante dargestellt wird.

`operator const D3D12_STATE_SUBOBJECT&`

Konvertierungsoperator, der einen Verweis auf eine Konstante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) Objekt zurückgibt, das das Zustandsobjekt beschreibt.

`operator const D3D12_HIT_GROUP_DESC&`

Konvertierungsoperator, der einen Verweis auf eine Konstante [D3D12_HIT_GROUP_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_hit_group_desc) Objekt zurückgibt, das das Zustandsobjekt beschreibt.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Siehe auch

* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
