---
description: Konvertiert Mesh-Adjazenzinformationen in ein Array von Punktmitarbeitern.
ms.assetid: b8914f9c-8550-498d-813d-bb1afe0fb5b2
title: ID3DXBaseMesh::ConvertAdjaencyToPointReps-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.ConvertAdjacencyToPointReps
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 729e6b67c68f5a9560cbf0aeab5d8f28b72854be49ebc00fb0f0924a5afa4b38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096030"
---
# <a name="id3dxbasemeshconvertadjacencytopointreps-method"></a>ID3DXBaseMesh::ConvertAdjaencyToPointReps-Methode

Konvertiert Mesh-Adjazenzinformationen in ein Array von Punktmitarbeitern.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConvertAdjacencyToPointReps(
  [in]      const DWORD *pAdjacency,
  [in, out]       DWORD *pPRep
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAdencyency* \[ In\]
</dt> <dd>

Typ: **const [**DWORD**](../winprog/windows-data-types.md) \***

Zeiger auf ein Array von drei DWORDs pro Gesicht, das die drei Nachbarn für jedes Gesicht im Gitternetz angibt. Die Anzahl der Bytes in diesem Array muss mindestens \* [**3 ID3DXBaseMesh::GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof(DWORD) betragen.

</dd> <dt>

*pPRep* \[ in, out\]
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)\***

Zeiger auf ein Array von einem DWORD pro Scheitelpunkt des Gitternetzes, das mit punktrepräsentanten Daten gefüllt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
