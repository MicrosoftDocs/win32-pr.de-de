---
description: Extrahiert Koeffizientsdaten aus einem Farbkanal des Puffers für einen angegebenen Bereich von Koeffizienten und fügt die Daten einem IDirect3DTexture9-Objekt hinzu.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: ID3DXPRTBuffer::ExtractTexture-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6f91186a15aa166928103073fdaca30d79809ad8c0a522abf3b136cb20a1d43a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120624"
---
# <a name="id3dxprtbufferextracttexture-method"></a>ID3DXPRTBuffer::ExtractTexture-Methode

Extrahiert Koeffizientsdaten aus einem Farbkanal des Puffers für einen angegebenen Bereich von Koeffizienten und fügt die Daten einem [**IDirect3DTexture9-Objekt**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kanal* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Pufferfarbkanal, aus dem Texturdaten extrahiert werden sollen.

</dd> <dt>

*StartCoefficient* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Startwert des Pufferkoeffizienten, aus dem Texturdaten extrahiert werden sollen.

</dd> <dt>

*NumCoefficients* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der Skalar, beginnend bei StartCoefficient, aus der Texturdaten extrahiert werden sollen.

</dd> <dt>

*pTexture* \[ In\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf ein [**IDirect3DTexture9-Texturobjekt,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) das Koeffizienten speichert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
