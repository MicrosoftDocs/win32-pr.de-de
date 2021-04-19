---
description: Gibt an, wie die Symbol Daten von den Quell-und Ziel Oberflächen in einem Rückruf von composerects kombiniert werden.
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: D3DCOMPOSERECTSOP-Enumeration (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: cd47cb14ab129bf27a4b59ba07e0be12d144fb8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370415"
---
# <a name="d3dcomposerectsop-enumeration"></a>D3DCOMPOSERECTSOP-Enumeration

Gibt an, wie die Symbol Daten von den Quell-und Ziel Oberflächen in einem Rückruf von [**composerects**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects)kombiniert werden.

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**D3DCOMPOSERECTS \_ Kopieren**
</dt> <dd>

Kopieren Sie die Quelle in das Ziel.

</dd> <dt>

<span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ oder**
</dt> <dd>

Bitweises OR-Quelle und-Ziel.

</dd> <dt>

<span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ und**
</dt> <dd>

Bitweises und die Quelle und das Ziel.

</dd> <dt>

<span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS- \_ netzb**
</dt> <dd>

Kopieren Sie die negiert-Quelle in das Ziel (DST & ~ src).

</dd> <dt>

<span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ Erzwingen von \_ DWORD**
</dt> <dd>

Reserviert. Wird verwendet, um die Enumeration auf eine Größe von 32 Bits zu erzwingen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




