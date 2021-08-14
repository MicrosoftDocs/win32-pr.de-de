---
description: Wendet Entkerne auf einen FLOAT-Texturpuffer an.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: ID3DXTextureGutterHelper::ApplyGuttersFloat-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.ApplyGuttersFloat
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c0401a6d0692331adf9e80c800530690e59eeec5e6a9463b57425af1a3f9330
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118800363"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a>ID3DXTextureGutterHelper::ApplyGuttersFloat-Methode

Wendet Entkerne auf einen FLOAT-Texturpuffer an.

## <a name="syntax"></a>Syntax


```C++
HRESULT ApplyGuttersFloat(
  [in] FLOAT *pDataIn,
  [in] UINT  *NumCoeffs,
  [in] UINT  *Width,
  [in] UINT  *Height
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDataIn* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Zeiger auf einen Puffer von FLOAT-Texturdaten.

</dd> <dt>

*NumCoeffs* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Anzahl von Skalaren pro Farbkanal, die im Arbeitsspeicher zum Speichern von Stichproben verwendet werden. Jedes Texel enthält NumCoeffs FLOAT-Werte.

</dd> <dt>

*Breite* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Breite der Textur in Pixel aus [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md).

</dd> <dt>

*Höhe* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)\***

Höhe der Textur in Pixel, die aus [**ID3DXTextureGutterHelper::GetHeight ermittelt wurde.**](id3dxtexturegutterhelper--getheight.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

[**Texel der Klasse 2**](id3dxtexturegutterhelper.md) werden durch Resampling der Klassen 1 und 4 Texel generiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
