---
description: Legt einen Texel-Klassen Wert fest, der Texttypen entsprechend der Position jedes Texttyps angibt.
ms.assetid: cb2e6afb-4b6a-4b01-aaa8-1fd2d1f2bfa1
title: 'ID3DXTextureGutterHelper:: setguttermap-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetGutterMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8d3c0b7c7e33664f3e078eca82a6f39b1294992a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355830"
---
# <a name="id3dxtexturegutterhelpersetguttermap-method"></a>ID3DXTextureGutterHelper:: setguttermap-Methode

Legt einen Texel-Klassen Wert fest, der Texttypen entsprechend der Position jedes Texttyps angibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetGutterMap(
  [in] BYTE *pGutterData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pgutterdata* \[ in\]
</dt> <dd>

Type: **[ **Byte**](../winprog/windows-data-types.md)\***

Zeiger auf die Texel-Klasse. Mögliche Texel-Klassen: Es ist keine Texel-Klasse 3 vorhanden.



| Texel-Klasse | Textsort                                                                                                                                                                                                                                                                                                                                                                |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0           | Ungültiger Punkt; Texel wird nicht verwendet.                                                                                                                                                                                                                                                                                                                                        |
| 1           | Innerhalb des Dreiecks.                                                                                                                                                                                                                                                                                                                                                              |
| 2           | Im bundbundbereich.                                                                                                                                                                                                                                                                                                                                                                |
| 4           | Im bundbundbereich; Texel wird als vollständiges Beispiel in der [**ID3DXTextureGutterHelper:: applyguttersfloat**](id3dxtexturegutterhelper--applyguttersfloat.md), [**ID3DXTextureGutterHelper:: applygutterstex**](id3dxtexturegutterhelper--applygutterstex.md)-Methode oder der [**ID3DXTextureGutterHelper:: applyguttersprt**](id3dxtexturegutterhelper--applyguttersprt.md) -Methode ausgewertet. |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
