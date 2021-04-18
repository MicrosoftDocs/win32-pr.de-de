---
description: Greifen Sie auf den zutreffungspuffer des Mesh zu.
ms.assetid: 42b13f14-4edf-4b56-9198-60a548855542
title: 'ID3DX10Mesh:: getaccessdencybuffer-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAdjacencyBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 80dd5c6e6d9b12cb1c648c42a4758d215d3810c7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355036"
---
# <a name="id3dx10meshgetadjacencybuffer-method"></a>ID3DX10Mesh:: getaccessdencybuffer-Methode

Greifen Sie auf den zutreffungspuffer des Mesh zu.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAdjacencyBuffer(
  [out] ID3DX10MeshBuffer **ppAdjacency
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppency* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3DX10MeshBuffer**](id3dx10meshbuffer.md)\*\***

Der annäherungspuffer. Siehe [**ID3DX10MeshBuffer**](id3dx10meshbuffer.md).

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

 

 




