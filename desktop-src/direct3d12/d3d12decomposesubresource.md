---
title: D3D12DecomposeSubresource-Funktion (D3dx12.h)
description: Gibt die MIP-Slice, den Array Slice und den Ebenen-Slice aus, die dem angegebenen unter Quell Index entsprechen.
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
ms.openlocfilehash: ec147833ee94969880865f679d40a198e0b22852
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361840"
---
# <a name="d3d12decomposesubresource-function"></a>D3D12DecomposeSubresource-Funktion

Gibt die MIP-Slice, den Array Slice und den Ebenen-Slice aus, die dem angegebenen unter Quell Index entsprechen.

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

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Der Index der untergeordneten Quelle.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die maximale Anzahl von MipMap-Ebenen in der Unterstruktur.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Elemente im Array.

</dd> <dt>

*Mipslice* \[ Out, Ref\]
</dt> <dd>

Typ: **T**

Gibt den MIP-Slice aus, der dem angegebenen subresource-Index entspricht.

</dd> <dt>

*Arrayslice* \[ Out, Ref\]
</dt> <dd>

Typ: **U**

Gibt das Array Slice aus, das dem angegebenen subresource-Index entspricht.

</dd> <dt>

*Planeslice* \[ Out, Ref\]
</dt> <dd>

Typ: **V**

Gibt den flachen Slice aus, der dem angegebenen subresource-Index entspricht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion bestimmt, welches MIP-Slice, Array Slice und der flache Slice einem angegebenen unter Quell Index entsprechen. Dies ist ein nützliches Hilfsprogramm, obwohl es C++ spezifisch ist.

Diese Funktion wird wie folgt mit C++-Vorlagen-Parametern für die Typen **T**, **U** und **V** deklariert:


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
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)

[Unterressourcen](subresources.md)
