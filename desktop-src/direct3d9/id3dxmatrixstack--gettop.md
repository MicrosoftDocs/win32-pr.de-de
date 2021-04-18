---
description: Ruft die aktuelle Matrix am Anfang des Stapels ab.
ms.assetid: 0e20af0a-a332-4cb5-bf87-2ec75aa170ab
title: 'ID3DXMATRIXStack:: GetTop-Methode (D3dx9math. h)'
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
ms.openlocfilehash: 5e635f2a825bf73234322066910c15af636ec9d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361187"
---
# <a name="id3dxmatrixstackgettop-method-d3dx9mathh"></a>ID3DXMATRIXStack:: GetTop-Methode (D3dx9math. h)

Ruft die aktuelle Matrix am Anfang des Stapels ab.

## <a name="syntax"></a>Syntax


```C++
D3DXMATRIX* GetTop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Typ: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Diese Methode gibt einen Zeiger auf eine [**D3DXMATRIX**](d3dxmatrix.md) -Struktur zurück, die die aktuelle Matrix darstellt.

## <a name="remarks"></a>Bemerkungen

Der von dieser Methode zurückgegebene [**D3DXMATRIX**](d3dxmatrix.md) -Zeiger ist nach nachfolgenden Stapel Vorgängen nicht garantiert gültig.

Beachten Sie, dass diese Methode nicht die aktuelle Matrix von der obersten Position des Stapels entfernt. Stattdessen wird nur die aktuelle Matrix zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMATRIXStack](id3dxmatrixstack.md)
</dt> <dt>

[**ID3DXMATRIXStack::P op**](id3dxmatrixstack--pop.md)
</dt> <dt>

[**ID3DXMATRIXStack::P USH**](id3dxmatrixstack--push.md)
</dt> </dl>

 

 




