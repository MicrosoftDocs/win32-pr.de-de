---
description: Beschreibt einen Rückrufschlüssel für die Verwendung in der Keyframe-Animation.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: D3DXKEY_CALLBACK-Struktur (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXKEY_CALLBACK
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f488445bbb018b62445ff802abcf5a82c22b4e31c9d71618e61437efd5e36a26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123068"
---
# <a name="d3dxkey_callback-structure"></a>D3DXKEY \_ CALLBACK-Struktur

Beschreibt einen Rückrufschlüssel für die Verwendung in der Keyframe-Animation.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DXKEY_CALLBACK {
  FLOAT  Time;
  LPVOID pCallbackData;
} D3DXKEY_CALLBACK, *LPD3DXKEY_CALLBACK;
```



## <a name="members"></a>Member

<dl> <dt>

**Time**
</dt> <dd>

Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**

</dd> <dd>

Keyframe-Zeitstempel.

</dd> <dt>

**pCallbackData**
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf Benutzerrückrufdaten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
