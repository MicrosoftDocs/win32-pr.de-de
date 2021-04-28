---
description: 'D3DX10CreateSkinInfo-Funktion: Erstellt mithilfe eines Deklarators ein leeres Skin mesh-Objekt.'
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: D3DX10CreateSkinInfo-Funktion (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 17d6ec99d3f43c41d56deebef81a021c81ec1d69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103598"
---
# <a name="d3dx10createskininfo-function"></a>D3DX10CreateSkinInfo-Funktion

Erstellt ein leeres Skin mesh-Objekt mithilfe eines Deklarators.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppSkinInfo* \[ out\]
</dt> <dd>

Typ: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***

Adresse eines Zeigers auf eine [**ID3DX10SkinInfo-Schnittstelle,**](id3dx10skininfo.md)die das erstellte Skin mesh-Objekt darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert E \_ OUTOFMEMORY sein.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie [**ID3DX10SkinInfo::SetBoneInfluence,**](id3dx10skininfo-setboneinfluence.md) um das leere Skin mesh-Objekt, das von dieser Methode zurückgegeben wird, zu füllen.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Mesh-Funktionen](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[D3DX-Funktionen](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




