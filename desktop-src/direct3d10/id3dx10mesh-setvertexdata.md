---
description: Legen Sie Scheitelpunktdaten in einen der Scheitelpunktpuffer des Gitters fest.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: ID3DX10Mesh::SetVertexData-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59dc5292d5d5dfc269f97f2a8d19ce9a19ea95ceefda47eaf89ac77f81838f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990330"
---
# <a name="id3dx10meshsetvertexdata-method"></a>ID3DX10Mesh::SetVertexData-Methode

Legen Sie Scheitelpunktdaten in einen der Scheitelpunktpuffer des Gitters fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*iBuffer* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Der Scheitelpunktpuffer, der mit pData gefüllt werden soll.

</dd> <dt>

*pData* \[ In\]
</dt> <dd>

Typ: **const \* void**

Die zu setzenden Scheitelpunktdaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
