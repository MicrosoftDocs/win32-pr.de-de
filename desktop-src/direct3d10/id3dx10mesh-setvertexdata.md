---
description: Legen Sie Scheitelpunkt Daten auf einen der Vertex-Puffer des Netzes fest.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: 'ID3DX10Mesh:: setvertexdata-Methode (d3dx10. h)'
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
ms.openlocfilehash: 68d54c6868e44517d42e0b53159f7a23ef45a05a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106367467"
---
# <a name="id3dx10meshsetvertexdata-method"></a>ID3DX10Mesh:: setvertexdata-Methode

Legen Sie Scheitelpunkt Daten auf einen der Vertex-Puffer des Netzes fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ibuffer* \[ in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Der Vertex-Puffer, der mit pData aufgefüllt werden soll.

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Typ: Konstante **void \***

Die festzulegenden Vertex-Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
