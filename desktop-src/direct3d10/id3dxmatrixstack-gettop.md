---
description: 'ID3DXMATRIXStack::GetTop-Methode (D3DX10.h): Ruft die aktuelle Matrix oben im Stapel ab.'
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: ID3DXMATRIXStack::GetTop-Methode (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.GetTop
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 340ea7ed85e05795dbc3949a29c5384871dfe840aa25ed4f9b2f07e1d4264de1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852230"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a>ID3DXMATRIXStack::GetTop-Methode (D3DX10.h)

Ruft die aktuelle Matrix am oberen Rand des Stapels ab.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Diese Methode gibt einen Zeiger auf eine D3DXMATRIX-Struktur zurück, die die aktuelle Matrix darstellt.

## <a name="remarks"></a>Hinweise

Der von dieser Methode zurückgegebene D3DXMATRIX-Zeiger ist nach nachfolgenden Stapelvorgängen nicht garantiert gültig.

Beachten Sie, dass diese Methode die aktuelle Matrix nicht vom Anfang des Stapels entfernt. stattdessen wird nur die aktuelle Matrix zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
