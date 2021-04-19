---
description: Ändern Sie, welche Knochen welche Scheitel Punkte beeinflussen.
ms.assetid: 0955e0ba-ffc5-408b-ab38-2abd39e1c429
title: 'ID3DX10SkinInfo:: remapbones-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.RemapBones
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 238e4628740fa74e055312c82de2635316f5bde5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350690"
---
# <a name="id3dx10skininforemapbones-method"></a>ID3DX10SkinInfo:: remapbones-Methode

Ändern Sie, welche Knochen welche Scheitel Punkte beeinflussen.

## <a name="syntax"></a>Syntax


```C++
HRESULT RemapBones(
  [in] UINT NewBoneCount,
  [in] UINT *pBoneRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Newbonecount* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die neue Anzahl von Knochen.

</dd> <dt>

*pboneremap* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein Array von Bone-Indizes, die die Neuzuordnung beschreiben. Beispiel: "skininfo" enthält einige Gedanken, dass "bone0" von "v0", "bone1" und "bone2" zu "V2" und "Array mit 2, 1, 0" für "pboneremap" angegeben wird. Dies bewirkt, dass bone0 v2, bone1 zu v1 und bone2 zu v0 zugeordnet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert lauten: e \_ outo-Memory oder e \_ invalidArg.

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

 

 
