---
title: D3DX11ComputeNormalMap-Funktion (D3DX11tex.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt. Hinweis Anstatt diese Funktion zu verwenden, wird empfohlen, die DirectXTex-Bibliothek ComputeNormalMap zu verwenden.
ms.assetid: 3ccdbd9a-669e-48ff-97d5-e5a6c7d2fb26
keywords:
- D3DX11ComputeNormalMap-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11ComputeNormalMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 747b8b01834126beb12e42d2fa26e15ea99c7471935af8ad74d078d15e9233ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124915"
---
# <a name="d3dx11computenormalmap-function"></a>D3DX11ComputeNormalMap-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, wird empfohlen, die [DirectXTex-Bibliothek](https://github.com/Microsoft/DirectXTex) **ComputeNormalMap zu** verwenden.

 

Konvertiert eine Höhenkarte in eine normale Karte. Die (x,y,z)-Komponenten jeder Normalen werden den (r,g,b)-Kanälen der Ausgabetextur zugeordnet.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11ComputeNormalMap(
  _In_ ID3D11DeviceContext *pContext,
  _In_ ID3D11Texture2D     *pSrcTexture,
  _In_ UINT                Flags,
  _In_ UINT                Channel,
  _In_ FLOAT               Amplitude,
  _In_ ID3D11Texture2D     *pDestTexture
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* \[ In\]
</dt> <dd>

Typ: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Zeiger auf eine [**ID3D11DeviceContext-Schnittstelle,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) die die Quelltextur der Höhenzuordnung darstellt.

</dd> <dt>

*pSrcTexture* \[ In\]
</dt> <dd>

Typ: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Zeiger auf eine [**ID3D11Texture2D-Schnittstelle,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) die die Quelltextur der Höhenzuordnung darstellt.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Mindestens ein D3DX \_ NORMALMAP-Flag, das die Generierung normaler Zuordnungen steuert.

</dd> <dt>

*Kanal* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Ein D3DX \_ CHANNEL-Flag, das die Quelle der Höheninformationen angibt.

</dd> <dt>

*Amplitude* \[ In\]
</dt> <dd>

Typ: **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)**

Konstanter Wertmultiplikator, der die Werte in der normalen Zuordnung erhöht (oder verringert). Höhere Werte machen Bumps in der Regel sichtbarer, niedrigere Werte machen Bumps in der Regel weniger sichtbar.

</dd> <dt>

*pDestTexture* \[ In\]
</dt> <dd>

Typ: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Zeiger auf eine [**ID3D11Texture2D-Schnittstelle,**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) die die Zieltextur darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Wert sein: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Hinweise

Diese Methode berechnet die Normalität mithilfe des zentralen Unterschieds mit einer Kernelgröße von 3x3. RGB-Kanäle im Ziel enthalten voreingenommene (x,y,z)-Komponenten der Normalen. Der zentrale differenzierende Nenner ist hartcodiert auf 2.0.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

