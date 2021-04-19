---
description: Enthält rote, grüne und blaue Daten.
ms.assetid: c596f47a-6c09-4b97-ab2f-b1da3d851aa4
title: D3DGAMMARAMP-Struktur (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DGAMMARAMP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 496885b8267d339c7617ec24b884fa193f8d9945
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370440"
---
# <a name="d3dgammaramp-structure"></a>D3DGAMMARAMP-Struktur

Enthält rote, grüne und blaue Daten.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DGAMMARAMP {
  WORD red[256];
  WORD green[256];
  WORD blue[256];
} D3DGAMMARAMP, *LPD3DGAMMARAMP;
```



## <a name="members"></a>Member

<dl> <dt>

**Red**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Ein Array von 256 Word-Elementen, das die rote Gamma-Rampe beschreibt.

</dd> <dt>

**Grünbuchs**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Ein Array von 256 Word-Elementen, das die grüne Gamma-Rampe beschreibt.

</dd> <dt>

**blauen**
</dt> <dd>

Typ: **[ **Word**](../winprog/windows-data-types.md)**

</dd> <dd>

Ein Array von 256 Word-Elementen, das die blaue Gamma-Rampe beschreibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**Getgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp)
</dt> <dt>

[**Setgammaramp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp)
</dt> </dl>

 

 
