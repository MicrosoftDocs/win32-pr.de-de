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
ms.openlocfilehash: d1d96cfe8124b47a9b6ce546379af1313a02ea26
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108038"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a>ID3DXMATRIXStack::GetTop-Methode (D3DX10.h)

Ruft die aktuelle Matrix oben im Stapel ab.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***

Diese Methode gibt einen Zeiger auf eine D3DXMATRIX-Struktur zurück, die die aktuelle Matrix darstellt.

## <a name="remarks"></a>Bemerkungen

Der von dieser Methode zurückgegebene D3DXMATRIX-Zeiger ist nach nachfolgenden Stapelvorgängen nicht garantiert gültig.

Beachten Sie, dass diese Methode die aktuelle Matrix nicht vom anfang des Stapels entfernt. stattdessen wird nur die aktuelle Matrix zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
