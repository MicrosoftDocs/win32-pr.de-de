---
description: Zuweisen von Speicherplatz für weitere Scheitel Punkte.
ms.assetid: dd6445ea-4754-4ba3-a264-59295325ee08
title: 'ID3DX10SkinInfo:: addvertices-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.AddVertices
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8f126b31c375e4e3463133960c5a1bcfbd995b62
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357284"
---
# <a name="id3dx10skininfoaddvertices-method"></a>ID3DX10SkinInfo:: addvertices-Methode

Zuweisen von Speicherplatz für weitere Scheitel Punkte.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddVertices(
  [in] UINT Count
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Anzahl* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Anzahl der hinzu zufügenden Vertices.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn diese Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ outo-Memory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
