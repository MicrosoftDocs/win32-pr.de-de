---
description: Erstellt einen komprimierten PRT-Puffer (preberechneten Radiance Transfer) aus einem unkomprimierten ID3DXPRTBuffer-Objekt. Diese Funktion sollte mit pro-Vertex-oder volumepuffer verwendet werden.
ms.assetid: 1464d2dd-05db-4d9a-84ac-39d57b6fff4f
title: D3DXCreatePRTCompBuffer-Funktion (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTCompBuffer
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6906067c8f2b412b58c728756ecaa6415168f05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354917"
---
# <a name="d3dxcreateprtcompbuffer-function"></a>D3DXCreatePRTCompBuffer-Funktion

Erstellt einen komprimierten PRT-Puffer (preberechneten Radiance Transfer) aus einem unkomprimierten [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt. Diese Funktion sollte mit pro-Vertex-oder volumepuffer verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DXCreatePRTCompBuffer(
  _In_    D3DXSHCOMPRESSQUALITYTYPE Quality,
  _In_    UINT                      NumClusters,
  _In_    UINT                      NumPCA,
  _In_    LPD3DXSHPRTSIMCB          pCB,
  _In_    LPVOID                    lpUserContext,
  _In_    LPD3DXPRTBUFFER           pBuffer,
  _Inout_ LPD3DXPRTCOMPBUFFER       *ppBuffer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Qualität* \[ in\]
</dt> <dd>

Typ: **[ **D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md)**

Qualität der kugelförmigen Komprimierung (SH). Siehe [**D3DXSHCOMPRESSQUALITYTYPE**](./d3dxshcompressqualitytype.md).

</dd> <dt>

*Numclusters* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der für die Komprimierung zu verwendenden Cluster.

</dd> <dt>

*Numpca* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der PCA-Basis-Vektoren (Principal Component Analysis), die in jedem Cluster verwendet werden sollen.

</dd> <dt>

*Platine* \[ in\]
</dt> <dd>

Typ: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Optionaler Zeiger auf die [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) -Rückruffunktion, die verwendet wird, um den Prozentsatz der abgeschlossenen PRT-Komprimierungs Berechnungen zu berechnen. Die Rückruffunktion muss implementiert werden, damit S OK zurückgegeben wird \_ , um die Komprimierungs Routine weiterhin ausführen zu können. Bei jedem anderen Wert wird die Komprimierung angehalten. Kann **null** sein.

</dd> <dt>

*lpusercontext* \[ in\]
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

Optionaler Zeiger auf einen benutzerdefinierten Wert, der an die [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) -Rückruffunktion übermittelt wird. Wird normalerweise von einer Anwendung verwendet, um einen Zeiger auf eine Datenstruktur zu übergeben, die Kontextinformationen für die Rückruffunktion bereitstellt. Kann **null** sein.

</dd> <dt>

*pbuffer* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Adresse eines Zeigers auf das nicht komprimierte [**ID3DXPRTBuffer**](id3dxprtbuffer.md) -Objekt, das komprimiert wird.

</dd> <dt>

*ppbuffer* \[ in, out\]
</dt> <dd>

Typ: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***

Adresse eines Zeigers auf das Output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Funktion fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ oudefmemory.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Voraus berechnete Strahlungs Übertragungsfunktionen](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> <dt>

[**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md)
</dt> <dt>

[**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md)
</dt> </dl>

 

 
