---
description: Aufheben der Zuordnung eines Puffers.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: 'ID3DX10MeshBuffer:: unmap-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Unmap
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0c3b382e0cfd01a51d89ddacb51ad390446315a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370478"
---
# <a name="id3dx10meshbufferunmap-method"></a>ID3DX10MeshBuffer:: unmap-Methode

Aufheben der Zuordnung eines Puffers.

## <a name="syntax"></a>Syntax


```C++
HRESULT Unmap();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen



|                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> Unmap () in Direct3D 10 entspricht der Ressourcen Sperre () in Direct3D 9.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10MeshBuffer](id3dx10meshbuffer.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




