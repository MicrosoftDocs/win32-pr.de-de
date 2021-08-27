---
title: CD3DX12_EXISTING_COLLECTION_SUBOBJECT -Klasse (D3dx12.h)
description: Eine Hilfsklasse zum Erstellen eines vorhandenen Auflistungszustands-Unterobjekts.
keywords:
- CD3DX12_EXISTING_COLLECTION_SUBOBJECT-Klasse
topic_type:
- apiref
api_name:
- CD3DX12_EXISTING_COLLECTION_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 2059bca83236ae51cbd69a9480624c3e540f18d6
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813288"
---
# <a name="cd3dx12_existing_collection_subobject-class"></a>CD3DX12_EXISTING_COLLECTION_SUBOBJECT-Klasse

Eine Hilfsklasse zum Erstellen eines vorhandenen Auflistungszustands-Unterobjekts.

Weitere Informationen zu den D3DX12 State Object Creation Helpers finden Sie [unter CD3DX12_STATE_OBJECT_DESC.](cd3dx12-state-object-desc.md)

## <a name="syntax"></a>Syntax

```cpp
class CD3DX12_EXISTING_COLLECTION_SUBOBJECT
{
    CD3DX12_EXISTING_COLLECTION_SUBOBJECT() noexcept;
    CD3DX12_EXISTING_COLLECTION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&);
    SetExistingCollection(ID3D12StateObject* pExistingCollection) noexcept;
    void DefineExport(
        LPCWSTR Name,
        LPCWSTR ExportToRename = nullptr,
        D3D12_EXPORT_FLAGS Flags = D3D12_EXPORT_FLAG_NONE);
    template<size_t N> void DefineExports(LPCWSTR(&Exports)[N]);
    void DefineExports(const LPCWSTR* Exports, UINT N);
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_EXISTING_COLLECTION_DESC& () const noexcept;
};
```

## <a name="members"></a>Member

`CD3DX12_EXISTING_COLLECTION_SUBOBJECT`

Standardkonstruktor Erstellt eine neue, standardmäßig initialisierte Instanz eines **CD3DX12_EXISTING_COLLECTION_SUBOBJECT.**

`CD3DX12_EXISTING_COLLECTION_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Konstruktor, der eine neue Instanz eines -Objekts **CD3DX12_EXISTING_COLLECTION_SUBOBJECT** mit dem Inhalt eines -Objekts [**initialisiert CD3DX12_STATE_OBJECT_DESC**](cd3dx12-state-object-desc.md) wird.

`SetExistingCollection(ID3D12StateObject*)`

Funktion zum Festlegen der vorhandenen Auflistung in Form des Zeigers auf ein [ID3D12StateObject,](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) das als Parameter übergeben wird.

`DefineExport(LPCWSTR, LPCWSTR = nullptr, D3D12_EXPORT_FLAGS)`

Definiert ein Symbol, das aus dem Unterobjekt exportiert wird. Akzeptiert einen [D3D12_EXPORT_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_export_flags) als optionalen Parameter.

`DefineExports(LPCWSTR(&)[N]);`

Definiert ein Array von Symbolen, die aus dem Unterobjekt exportiert werden. Der *Vorlagenparameter N* gibt die Anzahl der Elemente im Array an.

`DefineExports(const LPCWSTR*, UINT)`

Definiert ein Array von *N Symbolen,* die aus dem Unterobjekt exportiert werden.

`Type`

Ruft den Typ des Unterobjekts ab, dargestellt durch [die](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) D3D12_STATE_SUBOBJECT_TYPE_EXISTING_COLLECTION Konstante.

`operator const D3D12_STATE_SUBOBJECT&`

Konvertierungsoperator, der einen Verweis auf eine Konstante D3D12_STATE_SUBOBJECT [**objekt**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) zurückgibt, die das Zustandsobjekt beschreibt.

`operator const D3D12_EXISTING_COLLECTION_DESC&`

Konvertierungsoperator, der einen Verweis auf eine Konstante D3D12_EXISTING_COLLECTION_DESC [**objekt**](/windows/win32/api/d3d12/ns-d3d12-d3d12_existing_collection_desc) zurückgibt, die das Zustandsobjekt beschreibt.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Siehe auch

* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
