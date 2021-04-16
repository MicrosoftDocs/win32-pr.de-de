---
description: Beschreibt den Speicherort der Includedatei.
ms.assetid: a15d363e-0d82-44a9-816b-edf2f60540b3
title: D3DXINCLUDE_TYPE-Enumeration (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXINCLUDE_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 51a4ed41203a9f78ee5fef747f088e9def9033c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530896"
---
# <a name="d3dxinclude_type-enumeration"></a>D3DXINCLUDE- \_ Typenumeration

Beschreibt den Speicherort der Includedatei.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DXINCLUDE_TYPE { 
  D3DXINC_LOCAL        = 0,
  D3DXINC_SYSTEM       = 1,
  D3DXINC_FORCE_DWORD  = 0x7fffffff
} D3DXINCLUDE_TYPE, *LPD3DXINCLUDE_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DXINC_LOCAL"></span><span id="d3dxinc_local"></span>**D3DXINC \_ lokal**
</dt> <dd>

Suchen Sie im lokalen Projekt nach der Includedatei.

</dd> <dt>

<span id="D3DXINC_SYSTEM"></span><span id="d3dxinc_system"></span>**D3DXINC- \_ System**
</dt> <dd>

Suchen Sie im Systempfad nach der Includedatei.

</dd> <dt>

<span id="D3DXINC_FORCE_DWORD"></span><span id="d3dxinc_force_dword"></span>**D3DXINC \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[D3DX-Enumerationen](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




