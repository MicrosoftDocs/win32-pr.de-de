---
title: CD3DX12_STATE_OBJECT_DESC -Klasse (D3dx12.h)
description: Die zentrale Klasse der D3DX12 State Object Creation Helpers, die Hilfsklassen zum Erstellen von Zustandsobjekten aus einem beliebigen Satz von Unterobjekten sind.
keywords:
- CD3DX12_STATE_OBJECT_DESC-Klasse
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: cc3d65a9779c379debd94e7872717e4449a71ac8
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813076"
---
# <a name="cd3dx12_state_object_desc-class"></a>CD3DX12_STATE_OBJECT_DESC-Klasse

Die zentrale Klasse der D3DX12 State Object Creation Helpers, die Hilfsklassen zum Erstellen von Zustandsobjekten aus einem beliebigen Satz von Unterobjekten sind.

## <a name="syntax"></a>Syntax

```cpp
class CD3DX12_STATE_OBJECT_DESC
{
    CD3DX12_STATE_OBJECT_DESC() noexcept;
    CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE) noexcept;
    void SetStateObjectType(D3D12_STATE_OBJECT_TYPE) noexcept;
    operator const D3D12_STATE_OBJECT_DESC& ();
    operator const D3D12_STATE_OBJECT_DESC* ();
    template<typename T> T* CreateSubobject();
};
```

## <a name="members"></a>Member

`CD3DX12_STATE_OBJECT_DESC`

Standardkonstruktor Erstellt eine neue, standardmäßig initialisierte Instanz eines **CD3DX12_STATE_OBJECT_DESC.**

`CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE)`

Konstruktor, der eine neue Instanz eines -Objekts **erstellt, CD3DX12_STATE_OBJECT_DESC** mit einem Subjobject-Typ initialisiert wird, der dem Wert der D3D12_STATE_OBJECT_TYPE übergeben wird. [](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type)

`SetStateObjectType(D3D12_STATE_OBJECT_TYPE)`

Methode, die den Subjobject-Typ [](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) auf den Wert der übergebenen D3D12_STATE_OBJECT_TYPE legt.

`operator const D3D12_STATE_OBJECT_DESC&`

Konvertierungsoperator, der einen Verweis auf eine Konstante D3D12_STATE_OBJECT_DESC [**objekt**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) zurückgibt, die das Zustandsobjekt beschreibt.

`operator const D3D12_STATE_OBJECT_DESC*`

Konvertierungsoperator, der einen Zeiger auf eine Konstante D3D12_STATE_OBJECT_DESC [**Objekt**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) zurückgibt, das das Zustandsobjekt beschreibt.

`CreateSubobject`

Eine Funktionsvorlage, die ein Untergeordnetes Hilfsprojekt erstellt, dessen Lebensdauer im Besitz dieser Klasse ist.

Der Vorlagenparameter *T* gibt den Hilfstyp eines Unterobjekts an, z. B. [CD3DX12_HIT_GROUP_SUBOBJECT](cd3dx12-hit-group-subobject.md).

## <a name="remarks"></a>Hinweise

Um die D3DX12 State Object Creation Helpers zu verwenden, instanziieren Sie zunächst ein **CD3DX12_STATE_OBJECT_DESC-Objekt,** und rufen Sie dessen **CreateSubobject-Funktion** auf, um Unterobjekte zu erstellen. Die Unterobjekt-Hilfsobjekte verfügen jeweils über spezifische Methoden für dieses Unterobjekt zum Konfigurieren des Inhalts.

```cpp
CD3DX12_STATE_OBJECT_DESC Collection1(D3D12_STATE_OBJECT_TYPE_COLLECTION);
auto Lib0 = Collection1.CreateSubobject<CD3DX12_DXIL_LIBRARY_SUBOBJECT>();
Lib0->SetDXILLibrary(&pMyAppDxilLibs[0]);
Lib0->DefineExport(L"rayGenShader0");
// In practice, these export listings might be data/engine-driven.
...
```

Alternativ können Sie Hilfsobjekte für Unterobjekte explizit instanziieren, z. B. über lokale Variablen, indem Sie stattdessen das Zustandsobjekt desc (das darauf verweisen sollte) an den Hilfskonstruktor übergeben (oder `mySubobjectHelper.AddToStateObject(Collection1)` aufrufen).

In diesem alternativen Szenario müssen Sie das Unterobjekt so lange am Leben behalten, wie das Zustandsobjekt, dem es zugeordnet ist, leblos ist. Andernfalls sind die Zeigerverweise veraltet.

```cpp
CD3DX12_STATE_OBJECT_DESC RaytracingState2(D3D12_STATE_OBJECT_TYPE_RAYTRACING_PIPELINE);
CD3DX12_DXIL_LIBRARY_SUBOBJECT LibA(RaytracingState2);
LibA.SetDXILLibrary(&pMyAppDxilLibs[4]);
// Not manually specifying exports; meaning that all exports in the libraries are exported.
...
```

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Siehe auch

* [Hilfsstrukturen für Direct3D 12](helper-structures-for-d3d12.md)
