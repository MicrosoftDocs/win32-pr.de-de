---
description: Ruft die Parameter der Renderoberfläche ab.
ms.assetid: 4f46a4c6-7c50-479c-b2f5-24edff590c57
title: ID3DXRenderToSurface::GetDesc-Methode (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToSurface.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7dd6787ad8a81491e92af2a5ec1a16253af4cd0a0f8cb075dde01461b0010d45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790480"
---
# <a name="id3dxrendertosurfacegetdesc-method"></a>ID3DXRenderToSurface::GetDesc-Methode

Ruft die Parameter der Renderoberfläche ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDesc(
  [out] D3DXRTS_DESC *pParameters
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pParameters* \[ out\]
</dt> <dd>

Typ: **[ **D3DXRTS \_ DESC**](d3dxrts-desc.md)\***

Zeiger auf eine [**D3DXRTS \_ DESC-Struktur,**](d3dxrts-desc.md) die die Parameter der Renderoberfläche beschreibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert D3D \_ OK. Wenn bei der Methode ein Fehler auftritt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXRenderToSurface](id3dxrendertosurface.md)
</dt> </dl>

 

 




