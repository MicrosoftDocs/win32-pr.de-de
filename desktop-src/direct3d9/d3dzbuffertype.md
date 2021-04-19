---
description: Definiert Konstanten, die tiefen Puffer Formate beschreiben.
ms.assetid: 5e5ce48b-8859-43e0-a9b4-5972cf6bf781
title: D3DZBUFFERTYPE-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DZBUFFERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 271a278f48c10a89fa6f552c3e1a7b4a83f274f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355811"
---
# <a name="d3dzbuffertype-enumeration"></a>D3DZBUFFERTYPE-Enumeration

Definiert Konstanten, die tiefen Puffer Formate beschreiben.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DZBUFFERTYPE { 
  D3DZB_FALSE        = 0,
  D3DZB_TRUE         = 1,
  D3DZB_USEW         = 2,
  D3DZB_FORCE_DWORD  = 0x7fffffff
} D3DZBUFFERTYPE, *LPD3DZBUFFERTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DZB_FALSE"></span><span id="d3dzb_false"></span>**D3DZB \_ false**
</dt> <dd>

Deaktivieren Sie die tiefen Pufferung.

</dd> <dt>

<span id="D3DZB_TRUE"></span><span id="d3dzb_true"></span>**D3DZB \_ true**
</dt> <dd>

Aktivieren Sie z-Pufferung.

</dd> <dt>

<span id="D3DZB_USEW"></span><span id="d3dzb_usew"></span>**D3DZB \_ usew**
</dt> <dd>

Aktivieren Sie w-Pufferung.

</dd> <dt>

<span id="D3DZB_FORCE_DWORD"></span><span id="d3dzb_force_dword"></span>**D3DZB \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Member dieses Enumerationstyps werden mit dem D3DRS \_ zenable-Rendering-Zustand verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
