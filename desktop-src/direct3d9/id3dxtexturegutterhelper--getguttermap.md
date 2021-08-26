---
description: Empfängt einen Texelklassenwert, der die Texelklasse entsprechend dem Standort jedes Texels angibt.
ms.assetid: 450739a8-e30c-4e56-9560-8cb705a75672
title: ID3DXTextureGutterHelper::GetGutterMap-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ef2ed7b088e54dd82b1cc99422e1488139199ffe034e810de8e0a0bdb242f46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095690"
---
# <a name="id3dxtexturegutterhelpergetguttermap-method"></a>ID3DXTextureGutterHelper::GetGutterMap-Methode

Empfängt einen Texelklassenwert, der die Texelklasse entsprechend dem Standort jedes Texels angibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetGutterMap(
  [in, out] BYTE *pGutterData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGutterData* \[ in, out\]
</dt> <dd>

Typ: **[ **BYTE**](../winprog/windows-data-types.md)\***

Zeiger auf die Texelklasse. Folgende Texelklassen sind möglich. Es gibt keine Texelklasse 3.



| Texel-Klasse | Texel-Standort                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Ungültiger Punkt; Texel wird nicht verwendet.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Innerhalb des Dreiecks.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Innerhalb des Bundstegs.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Innerhalb des Bundstegs; texel wird als vollständiges Beispiel in den Methoden [**ID3DXTextureGutterHelper::ApplyGuttersFloat,**](id3dxtexturegutterhelper--applyguttersfloat.md) [**ID3DXTextureGutterHelper::ApplyGuttersTex**](id3dxtexturegutterhelper--applygutterstex.md)oder [**ID3DXTextureGutterHelper::ApplyGuttersPRT**](id3dxtexturegutterhelper--applyguttersprt.md) ausgewertet. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Hinweise

Die Anwendung muss pGutterData zuordnen und verwalten, wobei die Größe wie folgt angegeben ist:


```
texture width * texture height * sizeof(BYTE)
```



Texturbreite und -höhe werden von [**ID3DXTextureGutterHelper::GetWidth**](id3dxtexturegutterhelper--getwidth.md) und [**ID3DXTextureGutterHelper::GetHeight**](id3dxtexturegutterhelper--getheight.md)zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
