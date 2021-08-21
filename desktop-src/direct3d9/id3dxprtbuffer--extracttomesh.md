---
description: Extrahiert Koeffizientsdaten aus einem Einkanalpuffer und fügt die Daten einem ID3DXMesh-Objekt hinzu.
ms.assetid: 4fada987-ddd7-4c02-a177-dd81f3790588
title: ID3DXPRTBuffer::ExtractToMesh-Methode (D3DX9Mesh.h)
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
ms.openlocfilehash: c838a146a390aa72ac24781ca6f136b028ad41a6ee94fb4210ec4bd3f557acdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120614"
---
# <a name="id3dxprtbufferextracttomesh-method"></a>ID3DXPRTBuffer::ExtractToMesh-Methode

Extrahiert Koeffizientsdaten aus einem Einkanalpuffer und fügt die Daten einem [**ID3DXMesh-Objekt**](id3dxmesh.md) hinzu.

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

*NumCoefficients* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Anzahl der aus dem Puffer zu extrahierenden Koeffizienten. Bei Verwendung der vorberechnten Bogenmaßübertragung (PRT) der spherischen Durchlässigkeit sollte die Anzahl der Koeffizienten "Order bli" sein. Die Reihenfolge muss im Bereich von [D3DXSH \_ MINORDER](other-d3dx-constants.md) bis D3DXSH \_ MAXORDER (einschließlich) liegen.

</dd> <dt>

*Nutzung* \[ In\]
</dt> <dd>

Typ: **[ **D3DDECLUSAGE**](./d3ddeclusage.md)**

Vertexverwendungsbeschreibungen des Gitternetzes. Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).

</dd> <dt>

*UsageIndexStart* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Startindex für Koeffizienten, die im Netz gespeichert werden sollen.

</dd> <dt>

*pScene* \[ In\]
</dt> <dd>

Typ: **[ **LPD3DXMESH**](id3dxmesh.md)**

Zeiger auf ein [**ID3DXMesh-Meshobjekt,**](id3dxmesh.md) das Koeffizienten speichert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert S \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert einer der folgenden Werte sein: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 
