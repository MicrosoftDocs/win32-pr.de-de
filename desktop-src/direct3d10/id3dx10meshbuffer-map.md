---
description: Einen Zeiger auf den Arbeitsspeicher des Mesh-Puffers, um seinen Inhalt zu ändern.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'ID3DX10MeshBuffer:: Map-Methode (d3dx10. h)'
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
ms.openlocfilehash: 1b8cb03e128a6673963ce2d3cde993babb03da5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354946"
---
# <a name="id3dx10meshbuffermap-method"></a>ID3DX10MeshBuffer:: Map-Methode

Einen Zeiger auf den Arbeitsspeicher des Mesh-Puffers, um seinen Inhalt zu ändern.

## <a name="syntax"></a>Syntax


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppData* \[ vorgenommen\]
</dt> <dd>

Typ: **void \* \***

Zeiger auf die Puffer Daten.

</dd> <dt>

*Psize* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)\***

Größe des Puffers in Byte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 10:<br/> Map () in Direct3D 10 entspricht der Ressourcen Zuordnung () in Direct3D 9.<br/> |



 

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

 

 
