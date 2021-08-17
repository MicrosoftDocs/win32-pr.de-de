---
description: Extrahiert die PcA-Projektionskoeffizienten (Principal Component Analysis, Prinzipalkomponentenanalyse) pro Beispiel aus einem komprimierten ID3DXPRTCompBuffer-Datenpuffer und fügt die Daten einem ID3DXMesh-Objekt hinzu.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: ID3DXPRTCompBuffer::ExtractToMesh-Methode (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 410ec268da89ad4033c88a90c2b37bfa8e78a7b9c229cab72c8ad07e666fce42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117730036"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a>ID3DXPRTCompBuffer::ExtractToMesh-Methode

Extrahiert die PcA-Projektionskoeffizienten (Principal Component Analysis, Prinzipalkomponentenanalyse) pro Beispiel aus einem komprimierten [**ID3DXPRTCompBuffer-Datenpuffer**](id3dxprtcompbuffer.md) und fügt die Daten einem [**ID3DXMesh-Objekt**](id3dxmesh.md) hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumPCA,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*NumPCA* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der PCA-Koeffizienten, die aus dem Puffer extrahiert werden.

</dd> <dt>

*Verwendung* \[ In\]
</dt> <dd>

Typ: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Scheitelpunkt-Verwendungsbeschreibungen des Gitters. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndexStart* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Startindex für PCA-Koeffizienten, die im Netz gespeichert werden sollen.

</dd> <dt>

*pScene* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein [**ID3DXMesh-Gittermodellobjekt,**](id3dxmesh.md) in dem PCA-Koeffizienten gespeichert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, ist der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
