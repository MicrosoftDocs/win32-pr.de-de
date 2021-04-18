---
description: Beschreibt einen Rückruf Schlüssel zur Verwendung in Keyframe-Animationen.
ms.assetid: aca034f5-6961-49f1-ba7c-addcf016af2b
title: D3DXKEY_CALLBACK-Struktur (D3dx9anim. h)
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
ms.openlocfilehash: 5c2c4dc90cbb95218268bf673204867f5b5d6636
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355008"
---
# <a name="d3dxkey_callback-structure"></a>D3DXKEY- \_ Rückruf Struktur

Beschreibt einen Rückruf Schlüssel zur Verwendung in Keyframe-Animationen.

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

Typ: **[ **float**](../winprog/windows-data-types.md)**

</dd> <dd>

Der Keyframe-Zeitstempel.

</dd> <dt>

**pcallbackdata**
</dt> <dd>

Typ: **[ **LPVOID**](../winprog/windows-data-types.md)**

</dd> <dd>

Zeiger auf Benutzer Rückruf Daten.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Strukturen](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
