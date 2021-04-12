---
description: Berechnet an einem beliebigen Punkt, der nicht in einem Mesh ist, einen Übertragungs Vektor, der Quell Strahlen (dargestellt durch eine Glanz Näherung (SH)) zum Beenden der Strahlung zuordnet.
ms.assetid: 44790465-440d-4426-b780-ed872fbf8efb
title: 'ID3DXPRTEngine:: computesurf samplesdirectsh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03adb1729a8a2e771ea681ccbdd180999d3adcbf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356046"
---
# <a name="id3dxprtenginecomputesurfsamplesdirectsh-method"></a>ID3DXPRTEngine:: computesurf samplesdirectsh-Methode

Berechnet an einem beliebigen Punkt, der nicht in einem Mesh ist, einen Übertragungs Vektor, der Quell Strahlen (dargestellt durch eine Glanz Näherung (SH)) zum Beenden der Strahlung zuordnet.

## <a name="syntax"></a>Syntax


```C++
HRESULT ComputeSurfSamplesDirectSH(
  [in]            UINT            SHOrder,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Shorder* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Die Reihenfolge der zu verwendenden SH-Näherung.

</dd> <dt>

*NumSamples* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Beispiel Speicherorte.

</dd> <dt>

*psamplelocs* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Die Position für jede Stichprobe.

</dd> <dt>

*psamplenorms* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***

Normaler Vektor für jeden Beispiel Speicherort.

</dd> <dt>

*pdataout* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Zeiger auf ein Output [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das den direkten Beleuchtungs Beitrag zu dem Punkt modelliert und dabei die sh-Näherung verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Verwenden Sie beim Aufrufen dieser Methode keinen Textur Puffer.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: computedirectlightingsh**](id3dxprtengine--computedirectlightingsh.md)
</dt> <dt>

[**ID3DXPRTEngine:: computesurf samplesbounce**](id3dxprtengine--computesurfsamplesbounce.md)
</dt> </dl>

 

 
