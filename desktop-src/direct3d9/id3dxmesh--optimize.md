---
description: Generiert ein neues Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.
ms.assetid: 6a9bf7b9-2cb9-4b42-92d9-2a121ff79284
title: 'ID3DXMesh:: optimiert-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7752e08236094d7038a5e77ac1a679f787305022
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961770"
---
# <a name="id3dxmeshoptimize-method"></a>ID3DXMesh:: optimiert-Methode

Generiert ein neues Mesh mit neu bestellten Gesichtern und Scheitel Punkten, um die Zeichnungs Leistung zu optimieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT Optimize(
  [in]            DWORD        Flags,
  [in]      const DWORD        *pAdjacencyIn,
  [in, out]       DWORD        *pAdjacencyOut,
  [in, out]       DWORD        *pFaceRemap,
  [out]           LPD3DXBUFFER *ppVertexRemap,
  [out]           LPD3DXMESH   *ppOptMesh
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

Gibt den Typ der auszuführenden Optimierung an. Dieser Parameter kann auf eine Kombination aus einem oder mehreren Flags aus [**D3DXMESHOPT**](./d3dxmeshopt.md) und [**D3DXMESH**](./d3dxmesh.md) festgelegt werden (mit Ausnahme von D3DXMESH \_ 32 Bit, D3DXMESH \_ IB \_ Write only und D3DXMESH \_ Write).

</dd> <dt>

*padjackocyin* \[ in\]
</dt> <dd>

Typ: Konstante **[**DWORD**](../winprog/windows-data-types.md) \***

Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im quellmesh angibt. Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF. Siehe Hinweise.

</dd> <dt>

*padjacumcyout* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im optimierten Mesh angibt. Wenn der Rand keine angrenzenden Gesichter hat, ist der Wert 0xFFFFFFFF.

</dd> <dt>

*pfakeremap* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Ein Array von DWords, eines pro Gesicht, das die ursprüngliche Gitterfläche angibt, die den einzelnen Flächen im optimierten Mesh entspricht. Wenn der für dieses Argument angegebene Wert **null** ist, werden keine Gesichts Umwandlungs Daten zurückgegeben.

</dd> <dt>

*ppvertexremap* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Adresse eines Zeigers auf eine [**ID3DXBuffer**](id3dxbuffer.md) -Schnittstelle, die ein DWORD für jeden Scheitelpunkt enthält, der angibt, wie die neuen Scheitel Punkten den alten Scheitel Punkten zugeordnet werden. Diese Neuzuordnung ist nützlich, wenn Sie externe Daten basierend auf der neuen Scheitelpunkt Zuordnung ändern müssen.

</dd> <dt>

*ppoptmesh* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Adresse eines Zeigers auf eine [**ID3DXMesh**](id3dxmesh.md) -Schnittstelle, die das optimierte Mesh darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ invalidcall, E \_ outo fmemory.

## <a name="remarks"></a>Bemerkungen

Diese Methode generiert ein neues Mesh. Bevor Sie optimieren ausführen, muss eine Anwendung durch Aufrufen von [**ID3DXBaseMesh:: generateency**](id3dxbasemesh--generateadjacency.md)einen Ereignis Puffer generieren. Der zutreffende Puffer enthält Informationen zu den Daten, z. b. eine Liste der Kanten und die Gesichter, die nebeneinander angeordnet sind.

Diese Methode ähnelt der [**ID3DXBaseMesh:: clonemesh**](id3dxbasemesh--clonemesh.md) -Methode, mit der Ausnahme, dass Sie beim Erzeugen des neuen Klon des Netzes eine Optimierung durchführen kann. Das Ausgabe Mesh erbt alle Erstellungs Parameter des eingabemesh.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMesh](id3dxmesh.md)
</dt> <dt>

[**ID3DXMesh:: optimizeingeplace**](id3dxmesh--optimizeinplace.md)
</dt> </dl>

 

 
