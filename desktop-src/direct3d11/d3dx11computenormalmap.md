---
title: D3DX11ComputeNormalMap-Funktion (D3DX11tex. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Beachten Sie, dass Sie anstelle dieser Funktion die directxtex-Bibliothek, "computenormalmap", verwenden.
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
ms.openlocfilehash: 4399282c325fde0ea46679da9e9b84331b8c125b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219630"
---
# <a name="d3dx11computenormalmap-function"></a>D3DX11ComputeNormalMap-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, empfiehlt es sich, die [directxtex](https://github.com/Microsoft/DirectXTex) -Bibliothek " **computenormalmap**" zu verwenden.

 

Konvertiert eine Höhen Zuordnung in eine normale Karte. Die Komponenten (x, y, z) der einzelnen normalen werden den Kanälen (r, g, b) der Ausgabe Textur zugeordnet.

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

*pContext* \[ in\]
</dt> <dd>

Typ: **[ **Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Ein Zeiger auf eine [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Schnittstelle, die die Textur der Quell Höhe darstellt.

</dd> <dt>

*psrctexture* \[ in\]
</dt> <dd>

Typ: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Ein Zeiger auf eine [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) -Schnittstelle, die die Textur der Quell Höhe darstellt.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Ein oder mehrere D3DX \_ normalmap-Flags, die die Generierung normaler Karten steuern.

</dd> <dt>

*Channel* \[ in\]
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Ein D3DX- \_ kanalflag, das die Quelle der Höheninformationen angibt.

</dd> <dt>

*Amplitude* \[ in\]
</dt> <dd>

Typ: **[ **float**](/windows/desktop/WinProg/windows-data-types)**

Konstanter Wert Multiplikator, der die Werte in der normalen Zuordnung vergrößert (oder verringert). Höhere Werte machen in der Regel zu Leistungseinbußen, niedrigere Werte werden in der Regel weniger sichtbar.

</dd> <dt>

*pdesttexture* \[ in\]
</dt> <dd>

Typ: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Zeiger auf eine [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) -Schnittstelle, die die Ziel Textur darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert der folgende Wert sein: D3DERR \_ invalidcall.

## <a name="remarks"></a>Bemerkungen

Diese Methode berechnet die normale, indem der zentrale Unterschied mit einer Kernel Größe von 3X3 verwendet wird. RGB-Kanäle im Ziel enthalten unausgewogene (x, y, z) Komponenten der normalen. Der zentrale Differenzierungs Nenner ist hart codiert in 2,0.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

