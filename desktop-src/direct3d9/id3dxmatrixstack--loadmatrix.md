---
description: 'ID3DXMATRIXStack::LoadMatrix-Methode (D3dx9math.h): Lädt die angegebene Matrix in die aktuelle Matrix.'
ms.assetid: c4c5ac50-238f-4b41-8ea9-7e48ffd03fc5
title: ID3DXMATRIXStack::LoadMatrix-Methode (D3dx9math.h)
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
ms.openlocfilehash: f2ee7e5cae4d28b81b805faa4f113d0819f1eae9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093538"
---
# <a name="id3dxmatrixstackloadmatrix-method-d3dx9mathh"></a>ID3DXMATRIXStack::LoadMatrix-Methode (D3dx9math.h)

Lädt die angegebene Matrix in die aktuelle Matrix.

## <a name="syntax"></a>Syntax


```C++
HRESULT LoadMatrix(
  [in] const D3DXMATRIX *pMat
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMat* \[ In\]
</dt> <dd>

Typ: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Zeiger auf die [**D3DXMATRIX-Struktur,**](d3dxmatrix.md) die in die aktuelle Matrix geladen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Methode erfolgreich ist, lautet der Rückgabewert D3D \_ OK. Wenn die Methode fehlschlägt, kann der Rückgabewert D3DERR \_ INVALIDCALL sein.

## <a name="remarks"></a>Bemerkungen

Beachten Sie, dass diese Methode dem Stapel kein Element hinzufüge. stattdessen wird die aktuelle Matrix durch die angegebene Matrix ersetzt.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::LoadIdentity**](id3dxmatrixstack--loadidentity.md)
</dt> </dl>

 

 




