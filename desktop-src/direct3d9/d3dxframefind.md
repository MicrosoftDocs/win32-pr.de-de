---
description: Sucht den untergeordneten Rahmen eines Stamm Frames.
ms.assetid: 211e117a-9707-459a-a6a1-b3e78bdad6e2
title: D3DXFrameFind-Funktion (D3dx9anim. h)
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
ms.openlocfilehash: 82b8c56c93f19c99441b93707fac2a0c150e0c38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361206"
---
# <a name="d3dxframefind-function"></a>D3DXFrameFind-Funktion

Sucht den untergeordneten Rahmen eines Stamm Frames.

## <a name="syntax"></a>Syntax


```C++
LPD3DXFRAME D3DXFrameFind(
  _In_ const D3DXFRAME *pFrameRoot,
  _In_       LPCSTR    Name
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pframeroot* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3DXFRAME**](d3dxframe.md) \***

Zeiger auf den stammframe. Siehe [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*Name* \[ in\]
</dt> <dd>

Typ: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Der Name des zu suchenden untergeordneten Frames.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **LPD3DXFRAME**](d3dxframe.md)**

Gibt den untergeordneten Frame zurück, wenn er gefunden wird, andernfalls **null** . Siehe [**D3DXFRAME**](d3dxframe.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Animations Funktionen](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
