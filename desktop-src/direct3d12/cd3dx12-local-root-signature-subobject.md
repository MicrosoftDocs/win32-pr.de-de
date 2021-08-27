---
title: CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT -Klasse (D3dx12.h)
description: Eine Hilfsklasse zum Erstellen eines Subjektivs für den lokalen Stammsignaturzustand.
keywords:
- CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT-Klasse
topic_type:
- apiref
api_name:
- CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 85aee6a1697bdbcf01a741437da076f705731947
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813068"
---
# <a name="cd3dx12_local_root_signature_subobject-class"></a>CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT-Klasse

Eine Hilfsklasse zum Erstellen eines Subjektivs für den lokalen Stammsignaturzustand.

Weitere Informationen zu den D3DX12 State Object Creation Helpers finden Sie [unter CD3DX12_STATE_OBJECT_DESC.](cd3dx12-state-object-desc.md)

## <a name="syntax"></a>Syntax

```cpp
class CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT
{
    CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT() noexcept;
    CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void SetRootSignature(ID3D12RootSignature* pRootSig) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept { return *m_pSubobject; }
    operator ID3D12RootSignature* () const noexcept { return D3DX12_COM_PTR_GET(m_pRootSig); }
};
```

## <a name="members"></a>Member

`CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT`

Standardkonstruktor Erstellt eine neue, standardmäßig initialisierte Instanz eines **CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT.**

`CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Konstruktor, der eine neue Instanz eines -Objekts **CD3DX12_LOCAL_ROOT_SIGNATURE_SUBOBJECT** mit dem Inhalt eines CD3DX12_STATE_OBJECT_DESC [**initialisiert**](cd3dx12-state-object-desc.md) wird.

`SetRootSignature(ID3D12RootSignature*)`

Funktion zum Festlegen der Stammsignatur in Form des Zeigers auf eine [ID3D12RootSignature,](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) die als Parameter übergeben wird.

`Type`

Ruft den Typ des Unterobjekts ab, dargestellt durch [die](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) D3D12_STATE_SUBOBJECT_TYPE_LOCAL_ROOT_SIGNATURE Konstante.

`operator const D3D12_STATE_SUBOBJECT&`

Konvertierungsoperator, der einen Verweis auf eine Konstante D3D12_STATE_SUBOBJECT [objekt](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) zurückgibt, die das Zustandsobjekt beschreibt.

`operator ID3D12RootSignature*`

Konvertierungsoperator, der die Stammsignatur in Form eines Zeigers auf eine [ID3D12RootSignature zurückgibt.](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature)

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Siehe auch

* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
