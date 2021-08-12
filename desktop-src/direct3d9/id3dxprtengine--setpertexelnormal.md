---
description: Legt einen normalen Vektor für jedes Texel in einem Texturobjekt fest. Diese Methode wird verwendet, um vertexnormelle Vektoren aus einem Gitternetz zu speichern (oder interpolierte Scheitelpunktnormationen, wenn die pixelbasierte vorausberechnte Radianceübertragung (PRT) berechnet wird).
ms.assetid: 165a3ef6-c142-4988-b4fb-5aafd8ff11fe
title: ID3DXPRTEngine::SetPerTexelNormal-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetPerTexelNormal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 75877e8af86a22f80703742f148d5171e3a99e5c0c580bff588c27deba269b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293374"
---
# <a name="id3dxprtenginesetpertexelnormal-method"></a>ID3DXPRTEngine::SetPerTexelNormal-Methode

Legt einen normalen Vektor für jedes Texel in einem Texturobjekt fest. Diese Methode wird verwendet, um vertexnormelle Vektoren aus einem Gitternetz zu speichern (oder interpolierte Scheitelpunktnormationen, wenn die pixelbasierte vorausberechnte Radianceübertragung (PRT) berechnet wird).

## <a name="syntax"></a>Syntax


```C++
HRESULT SetPerTexelNormal(
  [in] LPDIRECT3DTEXTURE9 pNormalTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNormalTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf ein [**IDirect3DTexture9-Texturobjekt,**](/windows/desktop/api) das als Normalkarte des Objektraums dient, in der normale Vektoren gespeichert werden. Die Textur muss die gleichen Abmessungen wie [**ID3DXPRTBuffer**](id3dxprtbuffer.md) aufweisen und in der Lage sein, signierte Texturformate zu speichern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
