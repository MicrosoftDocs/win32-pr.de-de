---
description: Generiert ein Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren. Diese Methode ordnet das vorhandene Mesh neu an.
ms.assetid: 2cdaf627-d1d3-44f0-a5ae-9023d4b0de45
title: 'ID3DXMesh:: optimizzuplace-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.OptimizeInplace
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f889e0d3754cc1321ffa59eba294038b87991489
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762303"
---
# <a name="id3dxmeshoptimizeinplace-method"></a>ID3DXMesh:: optimizzuplace-Methode

Generiert ein Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren. Diese Methode ordnet das vorhandene Mesh neu an.

## <a name="syntax"></a>Syntax


```C++
HRESULT OptimizeInplace(
  [in]        DWORD        Flags,
  [in]  const DWORD        *pAdjacencyIn,
  [out]       DWORD        *pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Eine Kombination aus einem oder mehreren [**D3DXMESHOPT**](./d3dxmeshopt.md) -Flags, die den Typ der auszuführenden Optimierung angibt.

</dd> <dt>

*padjackocyin* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im quellmesh angibt. Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF.

</dd> <dt>

*padjacumcyout* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im optimierten Mesh angibt. Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF. Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Daten zurückgegeben.

</dd> <dt>

*pfakeremap* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Array von DWords, eines pro Gesicht, das die ursprüngliche Gitterfläche angibt, die den einzelnen Flächen im optimierten Mesh entspricht. Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Gesichts Umwandlungs Daten zurückgegeben.

</dd> <dt>

*ppvertexremap* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitel Punkten den alten Scheitel Punkten zugeordnet werden. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunkt Zuordnung ändern müssen. Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Vertex-neuumwandlungs Daten zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, D3DXERR \_ cannotattrsort, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Vor dem Ausführen von **ID3DXMesh:: OptimizeInPlace** muss eine Anwendung durch Aufrufen von [**ID3DXBaseMesh:: generateency**](id3dxbasemesh--generateadjacency.md)einen antreffenden Puffer generieren. Der zutreffende Puffer enthält Informationen zu den Daten, z. b. eine Liste der Kanten und die Gesichter, die nebeneinander angeordnet sind.

> [!Note]  
> Diese Methode schlägt fehl, wenn das Mesh den Vertex-Puffer mit einem anderen Mesh freigibt, es sei denn, die D3DXMESHOPT \_ ignoreverts werden in Flags festgelegt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: optimieren**](id3dxmesh--optimize.md)
</dt> </dl>

 

 
