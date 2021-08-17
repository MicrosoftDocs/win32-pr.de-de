---
description: Extrahiert die PcA-Projektionskoeffizienten (Principal Component Analysis, Prinzipalkomponentenanalyse) pro Beispiel aus einem komprimierten ID3DXPRTCompBuffer-Datenpuffer und fügt die Daten einem IDirect3DTexture9-Objekt hinzu.
ms.assetid: 2159e57d-b8e5-421f-b20a-ac58b29e3c45
title: ID3DXPRTCompBuffer::ExtractTexture-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6b6dd2f0a366cf371347d1f8f7289e1ad3c782e069dcd9f7007abbd7c1a5c33d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985650"
---
# <a name="id3dxprtcompbufferextracttexture-method"></a>ID3DXPRTCompBuffer::ExtractTexture-Methode

Extrahiert die PcA-Projektionskoeffizienten (Principal Component Analysis, Prinzipalkomponentenanalyse) pro Beispiel aus einem komprimierten [**ID3DXPRTCompBuffer-Datenpuffer**](id3dxprtcompbuffer.md) und fügt die Daten einem [**IDirect3DTexture9-Objekt**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExtractTexture(
  [in] UINT               StartPCA,
  [in] UINT               NumPCA,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartPCA* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Startwert des Pufferkoeffizienten, aus dem Texturdaten extrahiert werden.

</dd> <dt>

*NumPCA* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der PCA-Koeffizienten, die aus dem Puffer extrahiert werden.

</dd> <dt>

*pTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf ein [**IDirect3DTexture9-Texturobjekt,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) in dem PCA-Koeffizienten gespeichert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn bei der Methode ein Fehler auftritt, wird der folgende Wert zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
