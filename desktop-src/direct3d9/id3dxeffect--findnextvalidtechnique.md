---
description: Sucht das nächste gültige Verfahren, beginnend bei der Technik nach der angegebenen Technik.
ms.assetid: 0d2f3f80-90fd-495d-acb8-075f50e9a974
title: 'ID3DXEffect:: findnextvalidtechnique-Methode (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.FindNextValidTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: adcaaa5194abeb17d110118de922811eb84af7fa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104394145"
---
# <a name="id3dxeffectfindnextvalidtechnique-method"></a>ID3DXEffect:: findnextvalidtechnique-Methode

Sucht das nächste gültige Verfahren, beginnend bei der Technik nach der angegebenen Technik.

## <a name="syntax"></a>Syntax


```C++
HRESULT FindNextValidTechnique(
  [in]  D3DXHANDLE hTechnique,
  [out] D3DXHANDLE *pTechnique
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htechnik* \[ in\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Eindeutiger Bezeichner für eine Technik. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md). Geben Sie **null** für diesen Parameter an, um das erste gültige Verfahren zu suchen.

</dd> <dt>

*ptechnique* \[ vorgenommen\]
</dt> <dd>

Typ: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)\***

Zeiger auf einen Bezeichner für die nächste Technik. **Null** wird zurückgegeben, wenn dies die letzte Methode ist. Weitere Informationen finden Sie unter [Handles (Direct3D 9)](handles.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**D3DXTECHNIQUE- \_ Abteilung**](d3dxtechnique-desc.md)
</dt> <dt>

[**ID3DXEffect:: validatetechnique**](id3dxeffect--validatetechnique.md)
</dt> </dl>

 

 




