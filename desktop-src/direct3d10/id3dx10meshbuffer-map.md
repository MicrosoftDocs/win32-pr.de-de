---
description: Sie erhalten einen Zeiger auf den Gitternetzpufferspeicher, um dessen Inhalt zu ändern.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: ID3DX10MeshBuffer::Map-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4a71aaaffe7ed11429efa67b6065f94ecd154d0
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335354"
---
# <a name="id3dx10meshbuffermap-method"></a>ID3DX10MeshBuffer::Map-Methode

Sie erhalten einen Zeiger auf den Gitternetzpufferspeicher, um dessen Inhalt zu ändern.

## <a name="syntax"></a>Syntax


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppData* \[ out\]
</dt> <dd>

Typ: **\* \* void**

Zeiger auf die Pufferdaten.

</dd> <dt>

*pSize* \[ out\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Größe des Puffers in Byte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Unter [Direct3D 10-Rückgabecodes aufgeführten Werte.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise



 Unterschiede zwischen Direct3D 9 und Direct3D 10:

- Map() in Direct3D 10 entspricht der Ressourcenzuordnung () in Direct3D 9.



 

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

 

 
