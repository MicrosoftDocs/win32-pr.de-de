---
title: D3D12DecomposeSubresource-Funktion (D3dx12.h)
description: Gibt den MIP-Slice, den Arrayslice und den Ebenenslice aus, die dem angegebenen Unterressourcenindex entsprechen.
ms.assetid: 89FAD7C5-E732-4E74-AC2F-DEECD6ADDA7D
keywords:
- D3D12DecomposeSubresource-Funktion
topic_type:
- apiref
api_name:
- D3D12DecomposeSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c27089fb09c2408917be06b2f74e6d32f3e2f5aa9b96924de1ab92de190efb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045638"
---
# <a name="d3d12decomposesubresource-function"></a>D3D12DecomposeSubresource-Funktion

Gibt den MIP-Slice, den Arrayslice und den Ebenenslice aus, die dem angegebenen Unterressourcenindex entsprechen.

## <a name="syntax"></a>Syntax


```C++
void inline D3D12DecomposeSubresource(
        UINT Subresource,
        UINT MipLevels,
        UINT ArraySize,
  _Out_ T    &MipSlice,
  _Out_ U    &ArraySlice,
  _Out_ V    &PlaneSlice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Unterressource* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der Index der Unterressource.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die maximale Anzahl von Mipmapebenen in der Unterressource.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Elemente im Array.

</dd> <dt>

*MipSlice* \[ out, ref\]
</dt> <dd>

Typ: **T**

Gibt den MIP-Slice aus, der dem angegebenen Unterressourcenindex entspricht.

</dd> <dt>

*ArraySlice* \[ out, ref\]
</dt> <dd>

Typ: **U**

Gibt den Arrayslice aus, der dem angegebenen Unterressourcenindex entspricht.

</dd> <dt>

*PlaneSlice* \[ out, ref\]
</dt> <dd>

Typ: **V**

Gibt den Ebenenslice aus, der dem angegebenen Unterressourcenindex entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion bestimmt, welcher Mipslice, Arrayslice und Ebenenslice einem angegebenen Unterressourcenindex entsprechen. Dies ist ein nützliches Hilfsprogramm, obwohl es C++-spezifisch ist.

Diese Funktion wird wie folgt mit vorlagenisierten C++-Parametern für die Typen **T,** **U** und **V** deklariert:


```c++
template <typename T, typename U, typename V>
inline void D3D12DecomposeSubresource( UINT Subresource, UINT MipLevels, UINT ArraySize, _Out_ T& MipSlice, _Out_ U& ArraySlice, _Out_ V& PlaneSlice )
{
    MipSlice = static_cast<T>(Subresource % MipLevels);
    ArraySlice = static_cast<U>((Subresource / MipLevels) % ArraySize);
    PlaneSlice = static_cast<V>(Subresource / (MipLevels * ArraySize));
}
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)

[Unterressourcen](subresources.md)
