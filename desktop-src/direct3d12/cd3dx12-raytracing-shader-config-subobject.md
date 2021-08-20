---
title: CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT-Klasse (D3dx12.h)
description: Eine Hilfsklasse zum Erstellen eines Subobjekts für den Konfigurationszustand eines Raytracing-Shaders.
keywords:
- CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT-Klasse
topic_type:
- apiref
api_name:
- CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/04/2021
ms.openlocfilehash: 69f30a3cae1eeab030c8929ccd606fb892f27dd5
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812921"
---
# <a name="cd3dx12_raytracing_shader_config_subobject-class"></a>CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT-Klasse

Eine Hilfsklasse zum Erstellen eines Subobjekts für den Konfigurationszustand eines Raytracing-Shaders.

Weitere Informationen zu den D3DX12 State Object Creation Helpers finden Sie unter [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md).

## <a name="syntax"></a>Syntax

```cpp
class CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT
{
    CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT() noexcept;
    CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC& ContainingStateObject);
    void Config(UINT MaxPayloadSizeInBytes, UINT MaxAttributeSizeInBytes) noexcept;
    D3D12_STATE_SUBOBJECT_TYPE Type() const noexcept override;
    operator const D3D12_STATE_SUBOBJECT& () const noexcept;
    operator const D3D12_RAYTRACING_SHADER_CONFIG& () const noexcept;
};
```

## <a name="members"></a>Member

`CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT`

Standardkonstruktor Erstellt eine neue, standardmäßig initialisierte Instanz eines **CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT**.

`CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT(CD3DX12_STATE_OBJECT_DESC&)`

Konstruktor, der eine neue Instanz eines **CD3DX12_RAYTRACING_SHADER_CONFIG_SUBOBJECT** mit dem Inhalt eines [**CD3DX12_STATE_OBJECT_DESC-Objekts**](cd3dx12-state-object-desc.md) initialisiert wird.

`Config(UINT, UINT)`

Funktion zum Konfigurieren der maximalen Nutzlastgröße und der maximalen Attributgröße (beide in Bytes).

`Type`

Ruft den Typ des Unterobjekts ab, das durch die [D3D12_STATE_SUBOBJECT_TYPE_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_subobject_type) Konstante dargestellt wird.

`operator const D3D12_STATE_SUBOBJECT&`

Konvertierungsoperator, der einen Verweis auf eine Konstante [D3D12_STATE_SUBOBJECT](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_subobject) Objekt zurückgibt, das das Zustandsobjekt beschreibt.

`operator const D3D12_RAYTRACING_SHADER_CONFIG&`

Konvertierungsoperator, der einen Verweis auf eine Konstante [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config) Objekt zurückgibt, das das Zustandsobjekt beschreibt.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Siehe auch

* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
* [CD3DX12_STATE_OBJECT_DESC](cd3dx12-state-object-desc.md)
