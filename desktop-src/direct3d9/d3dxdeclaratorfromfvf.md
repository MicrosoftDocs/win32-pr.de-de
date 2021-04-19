---
description: Gibt einen Deklarator aus einem flexiblen Scheitelpunkt Formatierungs Code (FVF) zurück.
ms.assetid: 0272239c-0873-4a5c-b046-541f4ba603f4
title: D3DXDeclaratorFromFVF-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDeclaratorFromFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: de5360c7f9bd28d4c97184f985f06e48ca0002d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106366466"
---
# <a name="d3dxdeclaratorfromfvf-function"></a>D3DXDeclaratorFromFVF-Funktion

Gibt einen Deklarator aus einem flexiblen Scheitelpunkt Formatierungs Code (FVF) zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXDeclaratorFromFVF(
  _In_    DWORD             FVF,
  _Inout_ D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*F-VF* \[ in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus [D3DFVF](d3dfvf.md) , die die FVF beschreibt, aus der das zurückgegebene deklaratorarray generiert werden soll.

</dd> <dt>

*Deklaration* \[ in, out\]
</dt> <dd>

Typ: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**

Ein Array von [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) -Elementen, die das Scheitelpunkt Format der Mesh-Scheitel Punkte beschreiben. Die Obergrenze dieses deklaratorarrays ist [**Max \_ \_ \_**](./max-fvf-decl-size.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DXERR \_ invalidmesh.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Mesh-Funktionen](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
