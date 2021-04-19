---
description: Wendet die-Guster auf einen float-Textur Puffer an.
ms.assetid: 822483d7-ae62-498a-bce7-3a925ab21c04
title: 'ID3DXTextureGutterHelper:: applyguttersfloat-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 00ee6eac7328ee5f6adceb5b3966c222509237b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355208"
---
# <a name="id3dxtexturegutterhelperapplyguttersfloat-method"></a>ID3DXTextureGutterHelper:: applyguttersfloat-Methode

Wendet die-Guster auf einen float-Textur Puffer an.

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

*pdatain* \[ in\]
</dt> <dd>

Typ: **[ **float**](../winprog/windows-data-types.md)\***

Zeiger auf einen Puffer von float-Textur Daten.

</dd> <dt>

*Numkoeffs* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Anzahl der skalare pro Farbkanal, die im Arbeitsspeicher zum Speichern von Beispielen verwendet werden. Jedes textelor enthält numcoeffs float-Werte.

</dd> <dt>

*Breite* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Breite der Textur in Pixel, die von [**ID3DXTextureGutterHelper:: getWidth**](id3dxtexturegutterhelper--getwidth.md)abgerufen wird.

</dd> <dt>

*Höhe* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)\***

Die Höhe der Textur in Pixel, die von [**ID3DXTextureGutterHelper:: GetHeight**](id3dxtexturegutterhelper--getheight.md)abgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, wird der folgende Wert zurückgegeben. D3DERR \_ invalidcall

## <a name="remarks"></a>Bemerkungen

[**Class 2 texeln**](id3dxtexturegutterhelper.md) werden durch das erneute Sampling von Class 1 und 4 texeln generiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
