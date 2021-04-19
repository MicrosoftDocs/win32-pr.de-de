---
description: Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten ID3DXPRTCompBuffer-Datenpuffer und fügt die Daten einem ID3DXMesh-Objekt hinzu.
ms.assetid: 0680d626-f07a-43d3-acb9-e8db82b5e933
title: 'ID3DXPRTCompBuffer:: extracttomesh-Methode (D3DX9Mesh. h)'
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
ms.openlocfilehash: 607b583b89358d2d28030a4187b1608174d849c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370409"
---
# <a name="id3dxprtcompbufferextracttomesh-method"></a>ID3DXPRTCompBuffer:: extracttomesh-Methode

Extrahiert die pro-Beispiel-PCA-Projektions Koeffizienten (Principal Component Analysis) aus einem komprimierten [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) -Datenpuffer und fügt die Daten einem [**ID3DXMesh**](id3dxmesh.md) -Objekt hinzu.

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

*Numpca* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der PCA-Koeffizienten, die aus dem Puffer extrahiert werden sollen.

</dd> <dt>

*Verwendung* \[ in\]
</dt> <dd>

Typ: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Vertex-Verwendungs Beschreibungen des Netzes. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

" *Startwert* \[ " in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Start Index für die PCA-Koeffizienten, die im Mesh gespeichert werden sollen.

</dd> <dt>

*pscene* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekt, in dem die PCA-Koeffizienten gespeichert werden.

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

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
