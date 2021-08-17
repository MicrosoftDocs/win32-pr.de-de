---
description: Aufheben der Zuordnung eines Puffers.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: ID3DX10MeshBuffer::Unmap-Methode (D3DX10.h)
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
ms.openlocfilehash: 62b056b80b5722ce9173a7ca30200ba208cf88cf51c18d52b2a895d975121671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736039"
---
# <a name="id3dx10meshbufferunmap-method"></a>ID3DX10MeshBuffer::Unmap-Methode

Aufheben der Zuordnung eines Puffers.

## <a name="syntax"></a>Syntax


```C++
HRESULT Unmap();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise



Unterschiede zwischen Direct3D 9 und Direct3D 10:

- Unmap() in Direct3D 10 entspricht der Ressource Unlock() in Direct3D 9.



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX10MeshBuffer](id3dx10meshbuffer.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




