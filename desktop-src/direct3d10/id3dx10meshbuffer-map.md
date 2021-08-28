---
description: Abrufen eines Zeigers auf den Speicher des Gitternetzpuffers, um seinen Inhalt zu ändern.
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
ms.openlocfilehash: 38be37d9d11e40f336eab58691d18113664ff49138704ea563efe083800d7c14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096600"
---
# <a name="id3dx10meshbuffermap-method"></a>ID3DX10MeshBuffer::Map-Methode

Abrufen eines Zeigers auf den Speicher des Gitternetzpuffers, um seinen Inhalt zu ändern.

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

Der Rückgabewert ist einer der In [Direct3D 10-Rückgabecodes aufgeführten](d3d10-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise



 Unterschiede zwischen Direct3D 9 und Direct3D 10:

- Map() in Direct3D 10 entspricht der Ressource Map() in Direct3D 9.



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10MeshBuffer](id3dx10meshbuffer.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
