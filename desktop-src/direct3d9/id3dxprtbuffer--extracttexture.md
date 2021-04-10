---
description: Extrahiert Koeffizient Daten aus einem Farbkanal des Puffers für einen angegebenen Bereich von Koeffizienten und fügt die Daten einem IDirect3DTexture9-Objekt hinzu.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: 'ID3DXPRTBuffer:: extracttexture-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 2ea6cfdc8fb6ec83f847ccf37d06972974ea4de8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961652"
---
# <a name="id3dxprtbufferextracttexture-method"></a>ID3DXPRTBuffer:: extracttexture-Methode

Extrahiert Koeffizient Daten aus einem Farbkanal des Puffers für einen angegebenen Bereich von Koeffizienten und fügt die Daten einem [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Objekt hinzu.

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

*Channel* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Puffer Farbkanal, von dem Textur Daten extrahiert werden sollen.

</dd> <dt>

*Startkoeffizienten* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Startwert des Puffer Koeffizienten, von dem Textur Daten extrahiert werden sollen.

</dd> <dt>

*Numkoefficients* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl von skalaren, beginnend bei startkoeffizienten, aus denen Textur Daten extrahiert werden sollen.

</dd> <dt>

*ptexture* \[ in\]
</dt> <dd>

Typ: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Zeiger auf ein [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) -Textur Objekt, in dem Koeffizienten gespeichert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
