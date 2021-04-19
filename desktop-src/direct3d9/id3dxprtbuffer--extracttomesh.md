---
description: Extrahiert Koeffizienten-Daten aus einem Puffer mit einem einzelnen Kanal und fügt die Daten einem ID3DXMesh-Objekt hinzu.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: 'ID3DXPRTBuffer:: extracttomesh-Methode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractToMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e6dfe545a934f541938d6030cdc3814f451d93c8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367501"
---
# <a name="id3dxprtbufferextracttomesh-method"></a>ID3DXPRTBuffer:: extracttomesh-Methode

Extrahiert Koeffizienten-Daten aus einem Puffer mit einem einzelnen Kanal und fügt die Daten einem [**ID3DXMesh**](id3dxmesh.md) -Objekt hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT ExtractToMesh(
  [in] UINT         NumCoefficients,
  [in] D3DDECLUSAGE Usage,
  [in] UINT         UsageIndexStart,
  [in] LPD3DXMESH   pScene
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Numkoefficients* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Anzahl der Koeffizienten, die aus dem Puffer extrahiert werden sollen. Bei Verwendung von "sphärischen harmonisch (SH) preberechneten Radiance Transfer (PRT)" sollte die Anzahl der Koeffizienten "Order ²" lauten. Die Reihenfolge muss im Bereich von [D3DXSH \_ minorder](other-d3dx-constants.md) bis D3DXSH \_ maxorder (einschließlich) liegen.

</dd> <dt>

*Verwendung* \[ in\]
</dt> <dd>

Typ: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Vertex-Verwendungs Beschreibungen des Netzes. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

" *Startwert* \[ " in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Start Index für Koeffizienten, die im Mesh gespeichert werden sollen.

</dd> <dt>

*pscene* \[ in\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein [**ID3DXMesh**](id3dxmesh.md) Mesh-Objekt, in dem Koeffizienten gespeichert werden.

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

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
