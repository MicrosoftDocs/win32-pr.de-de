---
description: 'ID3DXMATRIXStack::GetTop-Methode (D3dx9math.h): Ruft die aktuelle Matrix oben im Stapel ab.'
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: ID3DXMATRIXStack::GetTop-Methode (D3dx9math.h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7e596551682805d13704e9ea85f82784a57b333e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093578"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a>ID3DXMATRIXStack::GetTop-Methode (D3dx9math.h)

Ruft die aktuelle Matrix am oberen Rand des Stapels ab.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Diese Methode gibt einen Zeiger auf eine [**D3DXMATRIX-Struktur**](d3dxmatrix.md) zurück, die die aktuelle Matrix darstellt.

## <a name="remarks"></a>Bemerkungen

Der von dieser Methode [**zurückgegebene D3DXMATRIX-Zeiger**](d3dxmatrix.md) ist nach nachfolgenden Stapelvorgängen nicht garantiert gültig.

Beachten Sie, dass diese Methode die aktuelle Matrix nicht vom Anfang des Stapels entfernt. stattdessen wird nur die aktuelle Matrix zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P ush**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




