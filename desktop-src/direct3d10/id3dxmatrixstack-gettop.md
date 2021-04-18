---
description: Ruft die aktuelle Matrix am Anfang des Stapels ab.
ms.assetid: cf379742-3e7d-4309-a7af-b97348428682
title: 'ID3DXMATRIXStack:: GetTop-Methode (d3dx10. h)'
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
ms.openlocfilehash: c545287ff3a4e7f9bfdccf21b9351fef06367433
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106364400"
---
# <a name="id3dxmatrixstackgettop-method-d3dx10h"></a>ID3DXMATRIXStack:: GetTop-Methode (d3dx10. h)

Ruft die aktuelle Matrix am Anfang des Stapels ab.

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

Der von dieser Methode zurückgegebene D3DXMATRIX-Zeiger ist nach nachfolgenden Stapel Vorgängen nicht garantiert gültig.

Beachten Sie, dass diese Methode nicht die aktuelle Matrix von der obersten Position des Stapels entfernt. Stattdessen wird nur die aktuelle Matrix zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DXMatrixStack](d3d10-id3dxmatrixstack.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
