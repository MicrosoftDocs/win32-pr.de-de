---
description: Ändern Sie, welche Scheitelpunkte von welchen Ecken beeinflusst werden.
ms.assetid: b0d71f3e-9a2d-469d-808b-2fa768cf14b0
title: ID3DX10SkinInfo::RemapVertices-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d73b9878a43ef876174561f16678f78787b15b88f423ecfb3f1765bd82c84630
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118302476"
---
# <a name="id3dx10skininforemapvertices-method"></a>ID3DX10SkinInfo::RemapVertices-Methode

Ändern Sie, welche Scheitelpunkte von welchen Ecken beeinflusst werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemapVertices(
  [in] UINT NewVertexCount,
  [in] UINT *pVertexRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NewVertexCount* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Die neue Anzahl von Scheitelpunkten.

</dd> <dt>

*pVertexRemap* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein Array von Scheitelpunktindizes, die die Neuzuordnung beschreiben. Angenommen, SkinInfo enthält einige Scheitelpunkte, sodass "skin0" v0, "1" zu "v1" und "2" zu "v2" zugeordnet ist und "array" mit "2,1,0" für pBoneRemap angegeben ist. Dies führt dazu, dass "0" v2, "1" zu "v1" und "2" zu "v0" zugeordnet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert E \_ OUTOFMEMORY oder E \_ INVALIDARG sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
