---
description: Suchen Sie nach dem Index, der angibt, wo sich ein bestimmter Scheitelpunkt in der Liste der beeinflussten Scheitel Punkte eines bestimmten Knotens befindet.
ms.assetid: vs|directx_sdk|~\id3dx10skininfo_findboneinfluenceindex.htm
title: 'ID3DX10SkinInfo:: findboneinfludenceindex-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.FindBoneInfluenceIndex
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1468fed3c0cf999e7635ba0f5ae53cee72fe70c6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219607"
---
# <a name="id3dx10skininfofindboneinfluenceindex-method"></a>ID3DX10SkinInfo:: findboneinfludenceindex-Methode

Suchen Sie nach dem Index, der angibt, wo sich ein bestimmter Scheitelpunkt in der Liste der beeinflussten Scheitel Punkte eines bestimmten Knotens befindet.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindBoneInfluenceIndex(
  [in] UINT BoneIndex,
  [in] UINT VertexIndex,
  [in] UINT *pInfluenceIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Boneingedex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Ein Index, der einen vorhandenen Knochen Wert angibt. Muss zwischen 0 und dem von [**ID3DX10SkinInfo:: getnumbones**](id3dx10skininfo-getnumbones.md)zurückgegebenen Wert liegen.

</dd> <dt>

*Vertexindex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Index des Scheitel Punkts im Scheitelpunkt Puffer.

</dd> <dt>

*pinfluendceindex* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Der Index des Scheitel Punkts in der Liste der von ihm beeinflussten Vertices in der Liste.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: E \_ invalidArg.

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

 

 
