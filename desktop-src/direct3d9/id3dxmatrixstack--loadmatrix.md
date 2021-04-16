---
description: Lädt die angegebene Matrix in die aktuelle Matrix.
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: 'ID3DXMATRIXStack:: loadmatrix-Methode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.LoadMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 292b4e147dfa99023f0b4d560a4ed41e6b41b3fe
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530860"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a>ID3DXMATRIXStack:: loadmatrix-Methode (D3dx9math. h)

Lädt die angegebene Matrix in die aktuelle Matrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmat* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***

Ein Zeiger auf die [**D3DXMATRIX**](d3dxmatrix.md) -Struktur, die in die aktuelle Matrix geladen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ausgeführt wird, ist der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert "D3DERR \_ invalidcall" lauten.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass diese Methode dem Stapel kein Element hinzufügt. Stattdessen wird die aktuelle Matrix durch die angegebene Matrix ersetzt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack:: loadidentity**](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




