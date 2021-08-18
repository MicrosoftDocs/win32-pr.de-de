---
description: Sucht den untergeordneten Frame eines Stammrahmens.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: D3DXFrameFind-Funktion (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFrameFind
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4f62cacabbf020d1fe9ff9e83c47acc6c58e52c4ab6be031586bda365745f595
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027660"
---
# <a name="d3dxframefind-function"></a>D3DXFrameFind-Funktion

Sucht den untergeordneten Frame eines Stammrahmens.

## <a name="syntax"></a>Syntax


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pFrameRoot* \[ In\]
</dt> <dd>

Typ: **const [**D3DXFRAME**](d3dxframe.md) \***

Zeiger auf den Stammrahmen. Siehe [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*Name* \[ In\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Name des zu suchenden untergeordneten Frames.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**

Gibt den untergeordneten Frame zurück, wenn er gefunden wird, **andernfalls NULL.** Siehe [**D3DXFRAME**](d3dxframe.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Animationsfunktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
